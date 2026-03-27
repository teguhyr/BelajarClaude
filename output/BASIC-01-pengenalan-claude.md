# Mengenal Claude - AI Assistant dari Anthropic

> **Level**: Basic
> **Estimasi Waktu**: 20 menit
> **Prasyarat**: Tidak ada

---

## Tujuan Pembelajaran

- Memahami apa itu Claude dan siapa yang membuatnya
- Membedakan Claude dari AI assistant lain di pasaran
- Mengetahui di mana dan bagaimana cara mengakses Claude
- Memahami batasan Claude yang perlu diperhatikan
- Menerapkan etika penggunaan AI di tempat kerja

---

## 1. Apa itu Claude?

Claude adalah AI assistant (asisten kecerdasan buatan) yang dibuat oleh **Anthropic**, perusahaan riset AI yang berfokus pada keamanan dan keandalan sistem AI.

**Kemampuan utama Claude:**
- Menulis dan mengedit teks (email, laporan, artikel, SOP)
- Merangkum dokumen panjang
- Menjawab pertanyaan dan menjelaskan konsep
- Menganalisis data dan memberikan insight
- Menulis dan menjelaskan kode program
- Berdiskusi dan brainstorming ide
- Menerjemahkan teks antar bahasa

**Cara kerja Claude (ringkas):**
- Claude dilatih dengan miliaran teks dari internet dan buku
- Claude memahami konteks percakapan dalam satu sesi
- Claude merespons berdasarkan instruksi yang diberikan (prompt)
- Claude **tidak** mengakses internet secara real-time

---

## 2. Perbandingan Claude vs AI Assistant Lain

| Fitur | Claude | ChatGPT (OpenAI) | Gemini (Google) |
|-------|--------|------------------|-----------------|
| Pembuat | Anthropic | OpenAI | Google |
| Akses gratis | Ya (terbatas) | Ya (terbatas) | Ya (terbatas) |
| Panjang konteks | Sangat panjang (200K token) | Sedang-panjang | Panjang |
| Kemampuan analisis dokumen | Sangat baik | Baik | Baik |
| Fokus keamanan AI | Tinggi | Sedang | Sedang |
| Integrasi Google Workspace | Tidak langsung | Tidak langsung | Ya (native) |
| Bahasa Indonesia | Baik | Sangat baik | Baik |

**Kapan pilih Claude?**
- Analisis dokumen panjang (kebijakan, laporan, kontrak)
- Tugas yang butuh instruksi kompleks dan bertahap
- Pekerjaan yang membutuhkan nuansa bahasa yang baik
- Proyek tim yang butuh konteks konsisten (fitur Projects)

---

## 3. Di Mana Claude Bisa Diakses?

**A. claude.ai (Web)**
- Akses via browser: `https://claude.ai`
- Tersedia dalam versi Free, Pro, dan Team
- Fitur: chat, Projects, Artifacts, upload file
- Rekomendasi untuk: pekerjaan sehari-hari, penulisan, analisis

**B. Claude Code (CLI - Command Line Interface)**
- Akses via terminal/command prompt di komputer
- Tools untuk developer dan pengguna teknis
- Rekomendasi untuk: bekerja langsung dengan file dan kode di komputer
- Dibahas lebih lanjut di Modul INTERMEDIATE-06

**C. Claude via API (Application Programming Interface)**
- Untuk developer yang ingin mengintegrasikan Claude ke aplikasi
- Membutuhkan pengetahuan pemrograman
- Tidak dibahas dalam training ini

**D. Aplikasi Pihak Ketiga**
- Beberapa aplikasi (Notion AI, dll.) menggunakan Claude di belakang layar
- Pengalaman mungkin berbeda dari claude.ai langsung

---

## 4. Batasan Claude yang Perlu Diketahui

> **Penting:** Memahami batasan Claude membantu kita menggunakannya dengan tepat dan menghindari kesalahan.

**Batasan pengetahuan:**
- Knowledge cutoff: Claude tidak mengetahui kejadian setelah tanggal training terakhirnya
- Tidak bisa browsing internet secara real-time (kecuali ada fitur khusus yang diaktifkan)
- Tidak mengetahui informasi internal perusahaan kecuali kita berikan

**Batasan memori:**
- Claude **tidak mengingat** percakapan sebelumnya secara default
- Setiap chat baru = memori bersih
- Solusi: gunakan fitur Projects untuk konteks yang persisten

**Batasan akurasi:**
- Claude bisa salah - ini disebut "hallucination" (mengada-ada informasi)
- Selalu verifikasi fakta penting, angka, dan data spesifik
- Jangan gunakan Claude sebagai satu-satunya sumber kebenaran

**Batasan lain:**
- Tidak bisa mengakses sistem internal perusahaan
- Tidak bisa mengirim email atau melakukan aksi di luar percakapan (kecuali integrasi khusus)
- File yang diupload hanya tersedia dalam sesi tersebut

---

## 5. Etika Penggunaan AI di Tempat Kerja

**Yang boleh dilakukan:**
- Menggunakan Claude untuk draf pertama dokumen (tetap review manual)
- Meminta bantuan analisis data yang sudah dianonimkan
- Brainstorming ide dan struktur konten
- Mempercepat pekerjaan rutin seperti formatting dan editing

**Yang perlu hati-hati:**
- Jangan paste data karyawan yang bisa mengidentifikasi individu (nama, NIK, gaji spesifik)
- Jangan paste informasi rahasia perusahaan yang sensitif
- Selalu review output Claude sebelum digunakan secara resmi
- Beri atribusi jika konten Claude digunakan dalam publikasi

> **Prinsip utama:** Claude adalah *asisten*, bukan *pengganti* judgment profesional kamu.

**Checklist sebelum paste ke Claude:**
- [ ] Apakah data ini sudah dianonimkan?
- [ ] Apakah data ini boleh dibagikan ke pihak ketiga?
- [ ] Apakah ada kebijakan perusahaan tentang penggunaan AI?
- [ ] Apakah saya akan review output sebelum digunakan?

---

## Rangkuman

- Claude adalah AI assistant dari Anthropic, unggul dalam analisis dokumen panjang dan instruksi kompleks
- Dapat diakses via claude.ai (web) atau Claude Code (terminal)
- Claude tidak mengingat percakapan sebelumnya - gunakan Projects untuk konteks persisten
- Claude bisa salah - selalu verifikasi informasi penting
- Jangan paste data karyawan atau informasi rahasia yang bisa mengidentifikasi individu

---

## Langkah Selanjutnya

- Lanjut ke **BASIC-02**: Setup akun dan mengenal antarmuka claude.ai
- Latihan hari ini: Buka claude.ai dan coba ajukan 3 pertanyaan berbeda untuk merasakan kemampuan Claude
