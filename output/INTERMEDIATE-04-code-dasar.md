# Fitur Code Claude - Generasi dan Penjelasan Kode

> **Level**: Intermediate - Code Track (Modul 1 dari 3)
> **Estimasi Waktu**: 40 menit
> **Prasyarat**: BASIC-01 hingga BASIC-04 (semua modul Basic)

---

## Tujuan Pembelajaran

- Memahami mengapa fitur kode Claude relevan untuk HR professional
- Meminta Claude menulis formula Excel dan Google Sheets
- Meminta Claude menulis script Python sederhana untuk data karyawan
- Meminta Claude membuat query SQL dasar untuk database HR
- Memahami prinsip keamanan sebelum menjalankan kode dari Claude

---

## Disclaimer Penting

> **Kamu tidak perlu jadi programmer untuk modul ini.**
>
> Modul ini dirancang untuk HR professional yang bekerja dengan data di Excel,
> perlu otomasi tugas berulang, atau berinteraksi dengan sistem HRIS.
> Fokus kita adalah: **bagaimana meminta Claude membuat kode yang bisa langsung kamu gunakan**,
> bukan belajar programming dari nol.

---

## 1. Mengapa HR Professional Perlu Tahu Fitur Code Claude?

**Situasi yang sering dialami HR:**
- Formula Excel untuk kalkulasi gaji, overtime, atau cuti terlalu kompleks
- Data karyawan dari HRIS perlu diolah tapi ukurannya besar
- Perlu laporan otomatis yang sama setiap bulan
- Ada proses manual berulang yang sebenarnya bisa diotomasi

**Apa yang bisa Claude bantu:**
- Menulis formula Excel/Google Sheets yang kamu deskripsikan
- Membuat script sederhana untuk memproses file CSV atau Excel
- Membuat query untuk mengambil data dari database
- Menjelaskan kode yang sudah ada agar kamu bisa memahami dan memodifikasinya

**Yang tidak perlu kamu lakukan:**
- Tidak perlu menghafal syntax kode
- Tidak perlu install software khusus untuk formula Excel/Sheets
- Cukup bisa mendeskripsikan apa yang kamu inginkan dalam bahasa natural

---

## 2. Formula Excel dan Google Sheets

Ini adalah penggunaan paling umum dan langsung bisa dipraktikkan tanpa perlu install apapun.

### Cara Meminta Formula

**Template prompt untuk formula:**
```
Buatkan formula Excel untuk [deskripsikan apa yang ingin dihitung/dilakukan].

Data saya:
- Kolom A: [nama kolom dan tipe data]
- Kolom B: [nama kolom dan tipe data]
- [dst]

Yang saya inginkan:
- [Jelaskan logika atau hasil yang diinginkan]
- [Tambahkan kondisi khusus jika ada]

Versi: Excel [versi kamu, atau Google Sheets]
```

### Contoh 1: Kalkulasi Overtime

**Prompt:**
```
Buatkan formula Excel untuk menghitung total upah lembur karyawan.
Data:
- Kolom A: Nama karyawan
- Kolom B: Jam kerja normal per hari (8 jam)
- Kolom C: Total jam kerja aktual hari ini
- Kolom D: Upah per jam normal (dalam rupiah)

Logika:
- Jika jam kerja aktual > 8 jam, hitungan lembur berlaku
- Jam lembur pertama (jam ke-9): upah 1.5x
- Jam lembur berikutnya (jam ke-10 dst): upah 2x
- Hasil di kolom E: total upah hari ini (normal + lembur)
```

**Contoh output yang akan diberikan Claude:**
```excel
=D2*MIN(C2,8) + IF(C2>8, D2*1.5*MIN(C2-8,1), 0) + IF(C2>9, D2*2*(C2-9), 0)
```
*Dengan penjelasan cara membaca dan menggunakannya*

### Contoh 2: VLOOKUP untuk Data Karyawan

**Prompt:**
```
Saya punya 2 sheet Excel:
- Sheet "Karyawan": kolom A = NIK, kolom B = Nama, kolom C = Departemen
- Sheet "Absensi": kolom A = NIK, dan saya ingin menampilkan nama karyawan di kolom B

Buatkan formula VLOOKUP untuk mengisi nama karyawan di Sheet Absensi
berdasarkan NIK. Jika NIK tidak ditemukan, tampilkan "Tidak Ditemukan".
```

### Contoh 3: Conditional Formatting via Formula

**Prompt:**
```
Saya punya data absensi di Google Sheets. Kolom E berisi total hari absen
karyawan dalam sebulan. Buatkan formula untuk kolom F yang:
- Tampilkan "NORMAL" jika absen ≤ 3 hari
- Tampilkan "PERHATIAN" jika absen 4-6 hari
- Tampilkan "KRITIS" jika absen > 6 hari
```

### Tips Formula Excel dengan Claude:

- Selalu sebutkan versi: Excel atau Google Sheets (syntax bisa berbeda)
- Sebutkan data dimulai dari baris berapa (baris 1 untuk header, baris 2 untuk data pertama)
- Minta Claude jelaskan cara kerjanya agar kamu bisa modifikasi sendiri
- Jika formula error, copy pesan error dan kirim ke Claude: "Formula ini error: [pesan error]. Tolong perbaiki."

---

## 3. Script Python untuk Data Karyawan

Python berguna ketika Excel sudah tidak cukup - data terlalu besar, proses terlalu kompleks, atau perlu otomasi.

> **Catatan:** Untuk menjalankan script Python, kamu perlu Python terinstall di komputer. Jika belum, coba dulu bagian Excel dulu, atau lanjut ke INTERMEDIATE-06 untuk Claude Code CLI yang membantu menginstall dan menjalankan script.

### Cara Meminta Script Python

**Template prompt:**
```
Buatkan script Python sederhana untuk [deskripsikan tugas].

Input data:
- File: [nama file.csv atau .xlsx]
- Kolom yang relevan: [list nama kolom]
- Contoh baris data: [beri 2-3 contoh baris data - TANPA DATA NYATA]

Output yang diinginkan:
- [Deskripsikan hasil yang diinginkan]
- [Format output: file baru, print ke layar, dll.]

Tambahkan komentar di setiap langkah penting agar saya bisa memahami scriptnya.
```

### Contoh 1: Memisahkan Data Karyawan per Departemen

**Prompt:**
```
Buatkan script Python untuk memisahkan file CSV karyawan menjadi
file terpisah per departemen.

Input: file "karyawan.csv" dengan kolom: ID, Nama, Departemen, Posisi, Tanggal_Masuk
(contoh data: 001, Budi Santoso, Finance, Staff, 2022-01-15)

Output: file terpisah untuk setiap departemen, misal: "Finance.csv", "Marketing.csv", dst.

Tambahkan: print berapa karyawan di tiap departemen setelah selesai.
Script harus aman dijalankan bahkan jika file CSV tidak ada (tampilkan pesan error yang jelas).
```

**Contoh output Claude:**
```python
import pandas as pd
import os

# Baca file CSV
try:
    df = pd.read_csv('karyawan.csv')
except FileNotFoundError:
    print("Error: File 'karyawan.csv' tidak ditemukan.")
    exit()

# Buat folder output jika belum ada
os.makedirs('output_departemen', exist_ok=True)

# Pisahkan per departemen
for departemen, data in df.groupby('Departemen'):
    nama_file = f'output_departemen/{departemen}.csv'
    data.to_csv(nama_file, index=False)
    print(f"Departemen {departemen}: {len(data)} karyawan → disimpan ke {nama_file}")

print(f"\nSelesai! Total {df['Departemen'].nunique()} departemen diproses.")
```

### Contoh 2: Rekapitulasi Data Absensi

**Prompt:**
```
Buatkan script Python untuk membuat rekap absensi bulanan dari file CSV.

Input: "absensi_oktober.csv" dengan kolom: NIK, Nama, Tanggal, Status
(Status bisa: Hadir, Izin, Sakit, Alpha)

Output: file "rekap_absensi_oktober.csv" dengan kolom:
NIK, Nama, Total_Hadir, Total_Izin, Total_Sakit, Total_Alpha, Persentase_Kehadiran

Persentase kehadiran = (Hadir / Total hari kerja) x 100
Asumsikan total hari kerja sesuai jumlah baris unik per karyawan.
```

> ⚠️ **PERINGATAN PRIVASI DATA:** Gunakan data dummy atau data yang sudah dianonimkan saat meminta Claude membuat script. Jangan paste data karyawan nyata ke claude.ai.

---

## 4. Query SQL untuk Database HR

SQL (Structured Query Language) digunakan untuk mengambil dan menganalisis data dari database. Berguna jika perusahaanmu punya HRIS dengan akses database.

> **Catatan:** Modul ini membutuhkan akses ke database HR. Jika tidak ada, bagian ini bisa digunakan sebagai referensi atau untuk memahami cara kerja HRIS.

### Cara Meminta Query SQL

**Template prompt:**
```
Buatkan query SQL untuk [deskripsikan data yang ingin diambil].

Struktur tabel:
- Tabel [nama_tabel]: kolom1 (tipe data), kolom2 (tipe data), ...
- [tabel lain jika ada]

Yang saya inginkan:
- [Deskripsikan hasil query: kolom apa, filter apa, urutan apa]

Database: MySQL / PostgreSQL / SQL Server (sebutkan yang kamu gunakan)
```

### Contoh 1: Daftar Karyawan per Departemen

**Prompt:**
```
Buatkan query SQL untuk menampilkan daftar semua karyawan aktif
beserta departemennya, diurutkan berdasarkan departemen dan nama.

Tabel "employees": id, name, department_id, status (active/inactive), hire_date
Tabel "departments": id, department_name

Hanya tampilkan karyawan dengan status 'active'.
Kolom output: Nama Karyawan, Departemen, Tanggal Masuk
```

**Contoh output:**
```sql
SELECT
    e.name AS "Nama Karyawan",
    d.department_name AS "Departemen",
    e.hire_date AS "Tanggal Masuk"
FROM employees e
JOIN departments d ON e.department_id = d.id
WHERE e.status = 'active'
ORDER BY d.department_name, e.name;
```

### Contoh 2: Laporan Headcount per Departemen

**Prompt:**
```
Buatkan query SQL untuk laporan headcount: berapa karyawan aktif di tiap departemen,
persentasenya dari total karyawan, dan siapa manager departemennya.

Tabel "employees": id, name, department_id, status, is_manager (boolean)
Tabel "departments": id, department_name
```

---

## 5. Memahami Output Kode Sebelum Menjalankan

**Prinsip kehati-hatian saat menggunakan kode dari Claude:**

- **Baca dulu, jalankan kemudian**: Minta Claude jelaskan apa yang dilakukan setiap bagian kode
- **Test dengan data dummy**: Jangan langsung jalankan di data produksi
- **Backup data**: Buat backup file sebelum menjalankan script yang memodifikasi file
- **Mulai dari skala kecil**: Jika script memproses ribuan baris, test dulu dengan 10-20 baris

**Cara minta Claude jelaskan kode:**
```
Jelaskan kode ini baris per baris dalam bahasa sederhana.
Saya bukan programmer, jadi gunakan analogi yang mudah dipahami.
[Paste kode di sini]
```

---

## 6. Bahasa Pemrograman yang Didukung Claude

Claude mendukung hampir semua bahasa pemrograman. Yang relevan untuk HR:

| Bahasa | Kegunaan HR | Tingkat Kesulitan |
|--------|-------------|-----------------|
| **Excel Formula** | Kalkulasi, lookup, kondisi | Mudah (tidak perlu install) |
| **Google Sheets** | Sama seperti Excel, berbasis web | Mudah (tidak perlu install) |
| **Python** | Otomasi, analisis data besar, batch processing | Sedang (perlu install Python) |
| **SQL** | Query database HRIS | Sedang (butuh akses database) |
| **VBA (Excel Macro)** | Otomasi Excel yang lebih kompleks | Sedang-sulit |
| **JavaScript** | Otomasi Google Workspace (Apps Script) | Sedang-sulit |

**Rekomendasi untuk HR professional:**
- Mulai dengan **Excel/Sheets formula** - langsung pakai, tidak perlu install
- Jika butuh lebih: pelajari **Python** dasar (baca saja, biarkan Claude yang nulis)
- SQL berguna jika punya akses ke database HRIS perusahaan

---

## Rangkuman

- Claude bisa menulis formula Excel/Sheets, script Python, dan query SQL - kamu cukup mendeskripsikan apa yang diinginkan
- Formula Excel/Sheets langsung bisa dipakai tanpa install software tambahan
- Python berguna untuk data besar atau proses berulang yang kompleks
- SQL berguna jika punya akses ke database HRIS
- Selalu minta Claude jelaskan kode sebelum menjalankan, dan test dengan data dummy dulu
- Jangan paste data karyawan nyata ke Claude saat meminta bantuan kode

---

## Langkah Selanjutnya

- Lanjut ke **INTERMEDIATE-05**: Debugging dan Code Review dengan Claude
- Latihan: Buat formula Excel untuk satu kebutuhan kalkulasi HR yang sering kamu lakukan manual
