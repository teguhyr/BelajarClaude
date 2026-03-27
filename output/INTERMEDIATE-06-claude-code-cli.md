# Claude Code CLI - Asisten Coding di Terminal

> **Level**: Intermediate - Code Track (Modul 3 dari 3)
> **Estimasi Waktu**: 45 menit
> **Prasyarat**: INTERMEDIATE-04 dan INTERMEDIATE-05 (Code Track)

---

## Tujuan Pembelajaran

- Memahami apa itu Claude Code CLI dan perbedaannya dari claude.ai
- Mengetahui kapan menggunakan Claude Code vs claude.ai web
- Menginstall Claude Code di komputer
- Menggunakan perintah dasar Claude Code
- Bekerja dengan file lokal menggunakan Claude Code
- Memahami aspek keamanan dan permission Claude Code

---

## Prasyarat Sebelum Mulai

> **Cek dulu sebelum lanjut:** Modul ini membutuhkan akses ke terminal (command prompt/terminal/PowerShell) dan kenyamanan dasar mengetik perintah. Jika belum pernah membuka terminal sama sekali, luangkan 10 menit dulu untuk membiasakan diri membuka dan mengetik di terminal.

**Apa yang dibutuhkan:**
- [ ] Komputer dengan akses terminal (Windows/Mac/Linux)
- [ ] Koneksi internet
- [ ] Akun claude.ai (sudah punya dari BASIC-02)
- [ ] Node.js terinstall (cek dengan mengetik `node --version` di terminal)

**Jika Node.js belum terinstall:**
- Kunjungi `nodejs.org` dan download versi LTS
- Ikuti proses instalasi standar
- Restart terminal setelah instalasi

---

## 1. Apa itu Claude Code CLI?

Claude Code CLI adalah **versi terminal dari Claude** yang dirancang khusus untuk bekerja langsung dengan file dan folder di komputer.

**Perbedaan utama:**

| Aspek | claude.ai (Web) | Claude Code CLI |
|-------|----------------|----------------|
| Antarmuka | Browser, tampilan chat | Terminal/command prompt |
| Akses file | Upload manual, satu per satu | Bisa baca/edit langsung di komputer |
| Konteks folder | Tidak ada | Tahu isi seluruh folder project |
| Otomasi | Terbatas | Bisa menjalankan perintah dan script |
| Cocok untuk | Chat, dokumen, analisis | Bekerja dengan kode dan file langsung |

**Analogi sederhana:**
- claude.ai = asisten yang kamu WhatsApp dari jarak jauh
- Claude Code CLI = asisten yang duduk di meja kerjamu dan bisa langsung pegang komputermu

---

## 2. Kapan Gunakan Claude Code vs claude.ai?

| Situasi | Gunakan |
|---------|---------|
| Menulis email, dokumen, kebijakan HR | claude.ai web |
| Analisis teks, brainstorming, riset | claude.ai web |
| Bertanya tentang konsep atau penjelasan | claude.ai web |
| Bekerja dengan folder file di komputer | Claude Code CLI |
| Membuat dan menjalankan script otomasi | Claude Code CLI |
| Memproses banyak file sekaligus | Claude Code CLI |
| Bekerja di lingkungan developer | Claude Code CLI |
| Upload dan analisis 1-2 dokumen | claude.ai web |

---

## 3. Instalasi Claude Code

### macOS

**Langkah-langkah:**

1. Buka Terminal (tekan `Cmd + Space`, ketik "Terminal", Enter)
2. Jalankan perintah instalasi:
   ```bash
   npm install -g @anthropic-ai/claude-code
   ```
3. Tunggu proses instalasi selesai
4. Verifikasi instalasi berhasil:
   ```bash
   claude --version
   ```
5. Jika muncul nomor versi, instalasi berhasil

### Windows

**Langkah-langkah:**

1. Buka PowerShell sebagai Administrator (klik kanan → "Run as Administrator")
2. Jalankan perintah instalasi:
   ```powershell
   npm install -g @anthropic-ai/claude-code
   ```
3. Verifikasi:
   ```powershell
   claude --version
   ```

> **Catatan Windows:** Beberapa fitur Claude Code lebih optimal di WSL (Windows Subsystem for Linux). Jika mengalami masalah, pertimbangkan menggunakan WSL.

### Linux

```bash
npm install -g @anthropic-ai/claude-code
claude --version
```

---

## 4. Login ke Claude Code

Setelah instalasi, kamu perlu login dengan akun Anthropic:

```bash
claude
```

Pertama kali dijalankan, Claude Code akan meminta autentikasi. Ikuti instruksi yang muncul (biasanya akan membuka browser untuk login). Setelah login berhasil, Claude Code siap digunakan.

---

## 5. Perintah Dasar Claude Code

### Mode Interaktif (Interactive Mode)

```bash
claude
```
Membuka sesi percakapan interaktif dengan Claude di terminal. Seperti chat, tapi di terminal.

Untuk keluar dari mode interaktif:
```
/exit
```
atau tekan `Ctrl+C`

### Mode One-Shot

```bash
claude "pertanyaan atau instruksi kamu di sini"
```

Contoh:
```bash
claude "Jelaskan apa yang dilakukan file Python ini" < script.py
```

### Menampilkan Bantuan

```bash
claude --help
```

### Perintah Berguna dalam Sesi Interaktif

| Perintah | Fungsi |
|---------|--------|
| `/help` | Tampilkan daftar perintah yang tersedia |
| `/clear` | Bersihkan layar terminal |
| `/exit` | Keluar dari Claude Code |
| `/compact` | Ringkas riwayat percakapan untuk menghemat konteks |

---

## 6. Membaca dan Menganalisis File dengan Claude Code

Salah satu keunggulan Claude Code: bisa membaca file langsung dari komputer.

**Cara memulai di folder project:**

1. Buka terminal
2. Navigasi ke folder yang ingin dikerjakan:
   ```bash
   cd /path/to/folder-kamu
   ```
   Contoh: `cd Documents/HR-Data`
3. Jalankan Claude Code:
   ```bash
   claude
   ```
4. Claude Code kini "tahu" isi folder tersebut

**Contoh interaksi:**

```
Kamu (di terminal):
> Baca file karyawan.csv dan buat ringkasan: berapa baris data,
  kolom apa saja yang ada, dan apakah ada nilai kosong yang perlu
  diperhatikan?

Claude:
[Claude akan membaca file dan memberikan analisis]
```

**Contoh lain:**
```
> Lihat semua file .py di folder ini dan jelaskan fungsi masing-masing
  dalam satu kalimat
```

```
> Baca README.md dan buat checklist dari langkah-langkah yang disebutkan
```

---

## 7. Mengedit File dengan Claude Code

Claude Code bisa membuat perubahan langsung pada file di komputermu.

> **Perhatian:** Sebelum mengizinkan Claude Code mengedit file penting, pastikan kamu sudah membuat backup atau menggunakan version control (git).

**Cara kerja:**

Claude Code akan meminta konfirmasi sebelum melakukan perubahan pada file. Kamu bisa:
- Approve (setuju): perubahan dilakukan
- Reject (tolak): perubahan dibatalkan
- Review: lihat dulu perubahan yang akan dilakukan

**Contoh interaksi:**

```
> Di file rekap.py, ubah separator CSV dari koma menjadi titik koma
  karena file akan dibuka di Excel Indonesia

Claude:
[Claude menampilkan perubahan yang akan dilakukan]
Mau saya lakukan perubahan ini? (y/n)

Kamu:
y

Claude:
File berhasil diperbarui.
```

**Tips aman:**
- Selalu review perubahan sebelum approve
- Gunakan `git` untuk version control jika bekerja dengan kode
- Mulai dengan file yang tidak penting untuk berlatih

---

## 8. Use Case: Analisis File CSV Karyawan

> ⚠️ **PERINGATAN PRIVASI DATA:** Untuk latihan, gunakan file CSV dengan data dummy. Jangan gunakan data karyawan asli.

**Contoh workflow:**

**Langkah 1:** Buat file CSV dummy dulu
```bash
claude "Buatkan file CSV dummy karyawan dengan 20 baris data fiktif.
Kolom: NIK, Nama, Departemen, Posisi, Tanggal_Masuk, Status.
Simpan sebagai karyawan_dummy.csv"
```

**Langkah 2:** Analisis file
```bash
claude "Analisis file karyawan_dummy.csv dan berikan:
1. Distribusi karyawan per departemen (tabel)
2. Rata-rata masa kerja dalam tahun
3. Berapa karyawan dengan status Aktif vs Tidak Aktif"
```

**Langkah 3:** Buat script berdasarkan analisis
```bash
claude "Berdasarkan file karyawan_dummy.csv, buatkan script Python
yang menghasilkan laporan rekap departemen. Simpan script sebagai
rekap_departemen.py dan jelaskan cara menjalankannya."
```

---

## 9. Use Case: Membuat Script Otomasi Sederhana

**Contoh: Script untuk rename file bulanan**

```
> Buatkan script Python yang bisa saya jalankan setiap bulan untuk:
  - Membaca semua file .xlsx di folder "laporan_masuk/"
  - Menambahkan prefix tanggal hari ini (format YYYYMM) ke setiap nama file
  - Memindahkan file ke folder "laporan_terproses/"

  Buat juga pesan konfirmasi sebelum memindahkan file dan
  log sederhana yang mencatat file apa saja yang dipindahkan.
```

Claude Code akan:
1. Membuat file script Python
2. Menjelaskan cara kerjanya
3. Memberitahu cara menjalankannya

---

## 10. Keamanan: Permission dan Batasan Claude Code

**Apa yang bisa dilakukan Claude Code:**
- Membaca file dan folder di lokasi yang kamu tentukan
- Membuat file baru
- Mengedit file yang sudah ada (dengan konfirmasimu)
- Menjalankan perintah terminal (dengan konfirmasimu)
- Install dependencies (library Python, dll.)

**Apa yang TIDAK bisa dilakukan Claude Code tanpa izin eksplisit:**
- Mengakses folder di luar yang kamu buka
- Mengirim data ke internet (selain ke API Anthropic untuk memprosesnya)
- Menghapus file (umumnya perlu konfirmasi eksplisit)
- Mengubah pengaturan sistem

**Prinsip keamanan:**
- Selalu jalankan Claude Code di folder yang tepat (bukan root/C:\ secara keseluruhan)
- Review semua perubahan file sebelum approve
- Backup data penting sebelum membiarkan Claude Code mengedit
- Waspada jika Claude Code meminta menjalankan perintah yang tidak kamu mengerti

**Cara menolak aksi yang mencurigakan:**
- Ketik `n` atau `no` saat diminta konfirmasi
- Tekan `Ctrl+C` untuk menghentikan proses
- Tutup terminal jika perlu

---

## 11. Tips dan Perintah Berguna Sehari-Hari

**Membuka Claude Code langsung di folder project:**
```bash
cd ~/Documents/HR-Project
claude
```

**Memberikan konteks awal:**
```
> Kamu sedang membantu saya mengelola folder HR data. Ada beberapa
  file CSV rekap bulanan dan beberapa script Python. Lihat isi folder
  ini dan beri saya ringkasan apa saja yang ada.
```

**Meminta Claude Code untuk tidak mengedit (hanya analisis):**
```
> Jangan ubah file apapun. Hanya analisis dan berikan rekomendasi saja.
```

**Bekerja dengan banyak file sekaligus:**
```
> Baca semua file CSV di folder ini dan buat perbandingan:
  apakah struktur kolomnya konsisten antar file?
```

**Meminta penjelasan kode yang sudah ada:**
```
> Baca file generate_report.py dan jelaskan dalam bahasa Indonesia
  sederhana apa yang dilakukan script ini step by step.
```

---

## Rangkuman

- Claude Code CLI = versi terminal Claude yang bisa bekerja langsung dengan file di komputer
- Bedakan dari claude.ai web: Claude Code untuk file/kode, claude.ai untuk chat/dokumen
- Instalasi via npm: `npm install -g @anthropic-ai/claude-code`
- Jalankan di folder yang relevan: `cd folder-kamu && claude`
- Claude Code selalu meminta konfirmasi sebelum mengubah file - review sebelum approve
- Gunakan data dummy untuk latihan, jangan data karyawan asli

---

## Langkah Selanjutnya

- **Code Track selesai!** Kamu sudah menyelesaikan ketiga modul code.
- Jika belum, lengkapi dengan **Co-work Track**: INTERMEDIATE-01, 02, 03
- Atau kembali ke **README-training.md** untuk melihat keseluruhan materi
- Aksi: Install Claude Code dan coba analisis satu folder project kecil
