# Memulai Menggunakan Claude - Setup dan Antarmuka

> **Level**: Basic
> **Estimasi Waktu**: 25 menit
> **Prasyarat**: BASIC-01 (Mengenal Claude)

---

## Tujuan Pembelajaran

- Membuat akun di claude.ai
- Mengenal setiap bagian antarmuka claude.ai
- Memilih model Claude yang tepat untuk tugas yang berbeda
- Menggunakan shortcuts dan fitur navigasi dasar
- Memulai percakapan pertama dengan Claude

---

## 1. Membuat Akun di claude.ai

**Langkah-langkah:**

1. Buka browser dan kunjungi `https://claude.ai`
2. Klik tombol **"Sign up"** di halaman awal
3. Pilih metode daftar:
   - Email (masukkan email dan buat password)
   - Google account (klik "Continue with Google")
4. Verifikasi email jika mendaftar via email (cek inbox)
5. Isi nama dan informasi dasar yang diminta
6. Setujui Terms of Service dan Privacy Policy
7. Akun siap digunakan

**Pilihan paket:**

| Paket | Harga | Batas Penggunaan | Cocok Untuk |
|-------|-------|-----------------|-------------|
| Free | Gratis | Terbatas per hari | Coba-coba, penggunaan ringan |
| Pro | ~$20/bulan | Lebih banyak + prioritas | Penggunaan harian intensif |
| Team | ~$25/user/bulan | Lebih banyak + fitur tim | Kolaborasi antar rekan kerja |

> **Tips:** Mulai dengan Free dulu untuk membiasakan diri. Upgrade ke Pro jika sering menemui pesan "limit reached".

---

## 2. Mengenal Antarmuka claude.ai

Setelah login, kamu akan melihat tampilan utama dengan beberapa area:

**Panel Kiri (Sidebar):**
- **New Chat** - tombol untuk memulai percakapan baru
- **Daftar percakapan** - riwayat semua chat sebelumnya (dalam sesi yang sama)
- **Projects** - folder khusus dengan konteks persisten (dibahas di INTERMEDIATE-01)
- **Tombol profile** - pengaturan akun, billing, preferensi

**Area Tengah (Chat Area):**
- Tempat percakapan dengan Claude berlangsung
- Pesan kamu muncul di kanan, respons Claude di kiri
- Scroll ke atas untuk melihat riwayat percakapan dalam sesi ini

**Area Input (Bawah):**
- **Kotak teks** - tempat mengetik prompt
- **Tombol attachment (klip kertas)** - upload file (gambar, PDF, teks, kode)
- **Tombol kirim** - atau tekan `Enter` untuk mengirim
- **Model selector** - pilih versi Claude (pojok kanan bawah atau atas)

**Panel Kanan (Artifacts):**
- Muncul saat Claude menghasilkan dokumen, kode, atau diagram
- Bisa diedit dan di-copy langsung dari panel ini
- Dibahas lebih lanjut di INTERMEDIATE-02

---

## 3. Memilih Model yang Tepat

Claude tersedia dalam beberapa versi (model). Pilihan muncul di selector model di antarmuka.

| Model | Kecepatan | Kualitas | Kapan Digunakan |
|-------|-----------|----------|-----------------|
| **Claude Haiku** | Sangat cepat | Baik | Tugas cepat: ringkasan singkat, pertanyaan sederhana |
| **Claude Sonnet** | Sedang | Sangat baik | Sebagian besar pekerjaan sehari-hari (default terbaik) |
| **Claude Opus** | Lebih lambat | Terbaik | Analisis kompleks, penulisan panjang, tugas kritis |

**Rekomendasi harian:**
- Default ke **Sonnet** untuk hampir semua pekerjaan
- Pakai **Haiku** jika butuh jawaban cepat dan sederhana
- Pakai **Opus** untuk dokumen atau analisis yang sangat penting

> **Tips:** Jika tidak yakin, pakai Sonnet. Kualitasnya sangat baik untuk 90% kebutuhan HR professional.

---

## 4. Memulai Percakapan Pertama

Cara mengirim pesan ke Claude:
1. Klik kotak teks di bagian bawah layar
2. Ketik prompt kamu
3. Tekan `Enter` atau klik tombol kirim (ikon panah)
4. Tunggu respons Claude (biasanya beberapa detik)
5. Lanjutkan percakapan dengan reply di bawahnya

**Contoh percakapan pertama yang bisa dicoba langsung:**

```
Hai Claude! Saya HR Manager di perusahaan manufaktur dengan 500 karyawan.
Tolong buatkan 5 pertanyaan icebreaker yang bisa digunakan di awal
sesi training karyawan baru. Format: nomor, pertanyaan, tujuan pertanyaan.
```

**Apa yang perlu kamu perhatikan dari respons Claude:**
- Apakah Claude mengikuti format yang diminta?
- Apakah jawabannya relevan dengan konteks yang diberikan?
- Apakah ada yang perlu diperbaiki atau dikembangkan?

---

## 5. Tips Navigasi dan Shortcuts

**Keyboard shortcuts yang berguna:**

| Shortcut | Fungsi |
|----------|--------|
| `Enter` | Kirim pesan |
| `Shift + Enter` | Baris baru dalam pesan (tanpa kirim) |
| `Ctrl/Cmd + K` | Buka percakapan baru |
| `Ctrl/Cmd + /` | Buka panel shortcuts (jika tersedia) |

**Fitur interface yang sering digunakan:**
- **Copy respons**: klik ikon copy di pojok respons Claude
- **Regenerate**: minta Claude coba jawab ulang (ikon refresh)
- **Edit pesan**: klik ikon pensil di pesan kamu untuk mengedit dan kirim ulang
- **Like/Dislike**: berikan feedback ke Anthropic tentang kualitas respons

**Mengelola riwayat percakapan:**
- Klik judul percakapan di sidebar untuk rename
- Hover percakapan di sidebar → ikon tiga titik → Delete untuk menghapus
- Claude tidak membawa memori antar percakapan yang berbeda

---

## 6. Upload File ke Claude

Claude bisa membaca dan menganalisis berbagai jenis file:

**Tipe file yang didukung:**
- Dokumen: PDF, Word (.docx), teks (.txt)
- Gambar: JPG, PNG, GIF, WebP
- Kode: hampir semua bahasa pemrograman
- Data: CSV, JSON

**Cara upload:**
1. Klik ikon klip kertas di kotak input
2. Pilih file dari komputer
3. Tambahkan instruksi apa yang harus Claude lakukan dengan file tersebut
4. Kirim

**Contoh prompt setelah upload:**
```
[setelah upload file kebijakan cuti.pdf]

Tolong baca dokumen ini dan buat ringkasan dalam 5 bullet point utama.
Fokus pada: syarat pengajuan cuti, jenis cuti yang tersedia,
dan proses approval.
```

> **Catatan:** File hanya tersedia dalam percakapan aktif. Jika mulai chat baru, perlu upload ulang. Gunakan Projects untuk konteks file yang persisten.

---

## Rangkuman

- Daftar di claude.ai via email atau Google account; mulai dengan Free plan
- Antarmuka terdiri dari: sidebar (navigasi), area chat (percakapan), input (prompt), dan panel Artifacts
- Default model: Claude Sonnet untuk hampir semua kebutuhan sehari-hari
- Tekan `Enter` untuk kirim, `Shift+Enter` untuk baris baru
- Claude bisa membaca PDF, gambar, dan berbagai format file lainnya

---

## Langkah Selanjutnya

- Lanjut ke **BASIC-03**: Cara menulis prompt yang efektif
- Latihan hari ini: Coba 3 percakapan berbeda dengan Claude menggunakan konteks pekerjaan kamu
