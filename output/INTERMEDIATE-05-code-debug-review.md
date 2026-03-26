# Debugging dan Code Review dengan Claude

> **Level**: Intermediate - Code Track (Modul 2 dari 3)
> **Estimasi Waktu**: 30 menit
> **Prasyarat**: INTERMEDIATE-04 (Fitur Code Dasar Claude)

---

## Tujuan Pembelajaran

- Memahami apa itu debugging dan mengapa perlu dilakukan
- Mengirimkan request debug yang efektif ke Claude
- Menggunakan Claude untuk code review sederhana
- Men-debug formula Excel yang tidak berfungsi
- Mengenal prinsip keamanan data saat debug

---

## 1. Apa itu Debugging?

**Debugging** = proses menemukan dan memperbaiki kesalahan (bug) dalam kode atau formula.

**Analogi sederhana:**
Bayangkan kamu punya resep masak yang salah satu langkahnya membuat masakan jadi gagal. Debugging adalah proses:
1. Menemukan langkah mana yang salah
2. Memahami *mengapa* langkah itu salah
3. Memperbaikinya agar resep bekerja dengan benar

**Jenis kesalahan yang umum:**
- **Syntax error**: Penulisan yang salah (tanda kurung kurang, typo nama fungsi)
- **Logic error**: Kode berjalan tapi hasilnya salah (formula menghitung dengan cara yang keliru)
- **Reference error**: Merujuk ke sel atau data yang tidak ada atau salah
- **Type error**: Salah tipe data (angka dianggap teks, atau sebaliknya)

---

## 2. Cara Meminta Claude Debug Kode

Kunci debug yang efektif: berikan **3 informasi** sekaligus.

**Template request debug:**
```
Tolong debug [formula/script/kode] ini.

KODE/FORMULA:
[paste kode yang bermasalah]

PESAN ERROR (jika ada):
[copy paste pesan error persis seperti yang muncul]

YANG DIHARAPKAN:
[deskripsikan hasil yang seharusnya muncul]

YANG TERJADI:
[deskripsikan apa yang sebenarnya terjadi / hasil yang salah]

KONTEKS TAMBAHAN (jika perlu):
[informasi lain yang relevan: versi Excel, struktur data, dll.]
```

**Mengapa 3 informasi ini penting:**
- Tanpa kode: Claude tidak tahu apa yang salah
- Tanpa pesan error: Claude harus menebak-nebak
- Tanpa ekspektasi: Claude tidak tahu apakah sudah benar atau belum

---

## 3. Contoh Debug: Formula Excel

**Situasi:** Formula SUMIF untuk menghitung total gaji per departemen tidak bekerja.

**Request debug yang buruk:**
```
Formula SUMIF saya tidak bekerja. Tolong perbaiki.
```

**Request debug yang baik:**
```
Tolong debug formula SUMIF ini yang tidak menghasilkan nilai yang benar.

FORMULA (di cell F2):
=SUMIF(B:B,"Finance",D:D)

STRUKTUR DATA:
- Kolom A: NIK karyawan
- Kolom B: Departemen (teks, contoh: "Finance", "Marketing")
- Kolom C: Nama karyawan
- Kolom D: Gaji (angka, format Currency)

YANG DIHARAPKAN:
Total gaji semua karyawan di departemen Finance.

YANG TERJADI:
Hasilnya selalu 0 padahal ada 15 karyawan Finance.

INFO TAMBAHAN:
Menggunakan Excel 2019. Data ada di Sheet1, formula di Sheet2.
```

**Kemungkinan penyebab yang akan ditemukan Claude:**
- Formula di Sheet2 tidak menyebutkan Sheet1! sebelum range kolom
- Ada spasi tersembunyi di data departemen ("Finance " bukan "Finance")
- Format kolom D bukan angka tapi teks

---

## 4. Contoh Debug: Script Python

**Situasi:** Script Python error saat dijalankan.

**Request debug:**
```
Script Python ini error saat dijalankan. Tolong perbaiki.

SCRIPT:
import pandas as pd

df = pd.read_csv('karyawan.csv')
rekap = df.groupby('Departemen')['Gaji'].sum()
rekap.to_excel('rekap_gaji.xlsx')
print("Selesai!")

PESAN ERROR:
ModuleNotFoundError: No module named 'openpyxl'

YANG DIHARAPKAN:
File rekap_gaji.xlsx terbuat dengan rekap gaji per departemen.

YANG TERJADI:
Script berhenti dengan error di atas sebelum menghasilkan file apapun.
```

**Claude akan memberitahu:** Perlu install library `openpyxl` dengan perintah `pip install openpyxl`, atau alternatifnya simpan ke CSV saja.

---

## 5. Code Review: Meminta Claude Periksa Kode

Code review = meminta Claude memeriksa kode yang sudah berjalan untuk mencari masalah potensial.

**Kapan melakukan code review:**
- Sebelum menggunakan script di data produksi
- Jika tidak yakin apakah logika sudah benar
- Jika kode terasa terlalu lambat atau tidak efisien
- Jika orang lain memberikan kode dan kamu ingin memahaminya

**Template code review:**
```
Tolong review kode/formula ini dan periksa:
1. Apakah logikanya sudah benar untuk kasus [deskripsikan kasus]?
2. Adakah kondisi/input yang bisa menyebabkan error?
3. Apakah ada cara yang lebih efisien atau lebih sederhana?
4. Apakah ada masalah keamanan yang perlu diperhatikan?

KODE:
[paste kode di sini]

KONTEKS PENGGUNAAN:
[deskripsikan untuk apa kode ini digunakan]
```

---

## 6. Debugging Formula Excel yang Umum untuk HR

### Error #VALUE!
**Penyebab:** Tipe data tidak cocok (biasanya teks dianggap angka atau sebaliknya)

**Cara debug dengan Claude:**
```
Formula ini menghasilkan error #VALUE! di Excel.
Formula: =DATEDIF(A2,TODAY(),"Y") untuk menghitung usia karyawan.
Kolom A berisi tanggal lahir. Apa penyebabnya dan bagaimana memperbaikinya?
```

### Error #REF!
**Penyebab:** Formula merujuk ke sel yang sudah dihapus atau tidak ada

**Cara debug:**
```
Setelah saya menghapus kolom C, banyak formula di kolom E
menampilkan #REF!. Bagaimana cara memperbaiki semua formula ini sekaligus?
Formula sebelumnya: =B2&" - "&C2&" - "&D2
```

### Error #N/A dari VLOOKUP
**Penyebab paling umum:** Nilai yang dicari tidak ada di tabel, atau format tidak cocok

**Cara debug:**
```
VLOOKUP saya menghasilkan #N/A untuk beberapa baris.
Formula: =VLOOKUP(A2,'Data Karyawan'!A:D,3,0)
Kolom A berisi NIK karyawan. NIK di sheet ini adalah angka,
tapi di sheet 'Data Karyawan' NIK-nya adalah teks (ada nol di depan, misal "001234").
Bagaimana cara memperbaikinya?
```

### Hasil SUMIF atau COUNTIF = 0 Padahal Seharusnya Ada Nilainya
**Cara debug:**
```
Formula COUNTIF saya selalu menghasilkan 0 padahal data ada.
=COUNTIF(B:B,"Aktif")
Saya sudah cek, ada data "Aktif" di kolom B. Apa yang salah?
Kolom B di-import dari sistem HRIS kami.
```
*(Penyebab umum: spasi tersembunyi atau karakter tersembunyi dari import)*

---

## 7. Cara Minta Perbaikan Secara Iteratif

Debugging sering butuh beberapa putaran. Lakukan secara iteratif:

**Putaran 1:** Paste kode + error → Claude identifikasi masalah
**Putaran 2:** Paste kode yang sudah diperbaiki → Claude verifikasi sudah benar
**Putaran 3:** Jika masih ada masalah → paste error baru yang muncul

**Contoh percakapan iteratif:**

```
[Pesan 1]
Formula ini error #VALUE: =DATEDIF(A2,TODAY(),"Y")
Kolom A berisi tanggal lahir.

[Claude memberikan solusi: format kolom A ke Date]

[Pesan 2]
Sudah saya ubah format kolomnya ke Date, tapi sekarang hasilnya 0 atau negatif
untuk beberapa baris. Datanya: A2 = 15/07/1990. Formula masih sama.

[Claude menemukan: format tanggal mungkin DD/MM/YYYY tapi Excel membacanya MM/DD/YYYY]

[Pesan 3]
Benar! Setelah saya ubah input tanggal ke format yang benar, formula bekerja
untuk beberapa baris. Tapi ada 3 baris yang masih salah. Baris-baris itu
memiliki tanggal: 01/13/1985, 01/14/1990, 01/25/1988. Apa masalahnya?
```

---

## 8. Keamanan Data: Apa yang TIDAK Boleh Di-paste saat Debug

> ⚠️ **PERINGATAN PRIVASI DATA:** Saat meminta Claude membantu debug, kamu mungkin tergoda untuk paste data asli agar Claude bisa melihat permasalahannya secara langsung. Ini berbahaya jika data berisi informasi pribadi karyawan.

**Yang TIDAK boleh di-paste:**
- Data dengan nama asli karyawan + data sensitif lainnya
- NIK, nomor KTP, NPWP, BPJS karyawan
- Data gaji spesifik per individu
- Data kesehatan atau status medis karyawan
- Catatan disiplin yang bisa mengidentifikasi individu

**Yang BOLEH di-paste:**
- Contoh data dummy (nama fiktif, angka tidak nyata)
- Data yang sudah dianonimkan (nama dihapus, NIK diganti kode)
- Struktur/skema data tanpa data aslinya

**Cara membuat data dummy untuk debug:**

Daripada paste:
```
NIK       | Nama          | Gaji
123456    | Budi Santoso  | 8500000
654321    | Sari Dewi     | 7200000
```

Paste data dummy:
```
NIK       | Nama    | Gaji
001       | KARY001 | 8500000
002       | KARY002 | 7200000
```

Atau cukup deskripsikan struktur data tanpa isi aslinya.

---

## 9. Latihan: Debug 3 Formula Excel Ini

Coba bawa formula-formula berikut ke Claude dan minta dibantu debug:

**Formula 1:** Menghitung masa kerja dalam tahun dari tanggal masuk kerja
```
=DATEDIF(C2,TODAY(),"Y") & " tahun " & DATEDIF(C2,TODAY(),"YM") & " bulan"
```
*(Coba dengan data tanggal masuk di kolom C dan lihat apakah hasilnya masuk akal)*

**Formula 2:** VLOOKUP untuk mencari departemen karyawan berdasarkan NIK
```
=VLOOKUP(A2,MasterData!A:C,2,FALSE)
```
*(Test dengan kondisi di mana NIK tidak ditemukan di MasterData)*

**Formula 3:** Conditional IF untuk kategori masa kerja
```
=IF(E2<1,"Baru",IF(E2<3,"Junior",IF(E2<5,"Mid","Senior")))
```
*(Di mana E2 adalah masa kerja dalam tahun - apakah batas threshold sudah sesuai kebutuhan?)*

---

## Rangkuman

- Debug efektif membutuhkan 3 hal: kode yang bermasalah, pesan error, dan ekspektasi hasil
- Lakukan debug secara iteratif: satu masalah diselesaikan dulu baru ke masalah berikutnya
- Code review: minta Claude periksa logika, potensi error, dan efisiensi kode
- Error umum Excel: #VALUE! (tipe data), #REF! (referensi hilang), #N/A (data tidak ditemukan)
- Jangan paste data karyawan asli saat debug - gunakan data dummy

---

## Langkah Selanjutnya

- Lanjut ke **INTERMEDIATE-06**: Claude Code CLI - Asisten Coding di Terminal
- Latihan: Ambil satu formula Excel yang pernah kamu buat sendiri, minta Claude review apakah ada yang bisa diperbaiki
