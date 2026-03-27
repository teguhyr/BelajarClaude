# Projects & Shared Context - Kelola Pekerjaan Tim dengan Claude

> **Level**: Intermediate - Co-work Track (Modul 1 dari 3)
> **Estimasi Waktu**: 35 menit
> **Prasyarat**: BASIC-01 hingga BASIC-04 (semua modul Basic)

---

## Tujuan Pembelajaran

- Memahami perbedaan Projects vs chat biasa di Claude
- Membuat dan mengonfigurasi Project baru
- Menambahkan dokumen dan instruksi ke Project
- Berbagi Project dengan anggota tim
- Merancang strategi organisasi Project untuk kebutuhan HR

---

## 1. Apa itu Projects?

Projects adalah fitur di claude.ai yang memungkinkan Claude **mengingat konteks** secara persisten di seluruh percakapan dalam satu project.

**Perbedaan utama Projects vs Chat Biasa:**

| Aspek | Chat Biasa | Projects |
|-------|-----------|---------|
| Memori konteks | Hanya dalam satu sesi | Persisten di semua percakapan dalam project |
| Dokumen | Perlu upload ulang tiap sesi | Upload sekali, tersedia terus |
| Instruksi khusus | Harus diulang tiap chat | Tersimpan sebagai Project Instructions |
| Berbagi | Tidak bisa | Bisa dibagikan ke anggota tim |
| Organisasi | Semua chat tercampur | Terorganisir per project/tema |

**Kapan gunakan Projects:**
- Proyek yang berlangsung lebih dari satu percakapan
- Pekerjaan yang membutuhkan konteks konsisten (kebijakan, panduan, data perusahaan)
- Kolaborasi tim di mana beberapa orang perlu akses ke Claude dengan konteks yang sama
- Pekerjaan berulang yang butuh instruksi standar

> **Catatan:** Fitur Projects tersedia di Claude **Pro dan Team plan**. Free plan mungkin memiliki akses terbatas.

---

## 2. Membuat Project Baru

**Langkah-langkah:**

1. Login ke `claude.ai`
2. Di sidebar kiri, klik tombol **"New Project"** (atau ikon folder +)
3. Beri nama project yang deskriptif (contoh: "Rekrutmen Q1 2025" atau "HR Policy Development")
4. Klik **"Create project"**
5. Kamu akan masuk ke halaman Project dengan beberapa area:
   - **Knowledge** - tempat upload dokumen referensi
   - **Project Instructions** - instruksi/system prompt untuk project ini
   - **Conversations** - daftar semua chat dalam project ini

**Tips penamaan project:**
- Gunakan nama yang spesifik: "Rekrutmen Engineer 2025" lebih baik dari "Rekrutmen"
- Tambahkan periode jika relevan: "Annual Performance Review Q4"
- Gunakan nama departemen jika project per fungsi: "L&D Team Project"

---

## 3. Menambahkan Dokumen ke Project (Knowledge)

Dokumen yang diupload ke Project akan selalu tersedia di setiap percakapan dalam project tersebut.

**Cara upload dokumen:**

1. Buka project yang sudah dibuat
2. Klik bagian **"Knowledge"** atau tombol upload dokumen
3. Klik **"Add content"** → pilih **"Upload files"**
4. Pilih file dari komputer (atau drag & drop)
5. Tunggu proses upload selesai
6. Dokumen sekarang tersedia di semua percakapan dalam project ini

**Cara menambah konten teks langsung:**
1. Klik **"Add content"** → **"Add text"**
2. Paste atau ketik konten (cocok untuk panduan, prosedur, data referensi)
3. Beri judul yang jelas
4. Klik **"Save"**

**Dokumen yang cocok dimasukkan ke Project HR:**
- Kebijakan dan SOP HR perusahaan
- Struktur organisasi dan deskripsi jabatan
- Template dokumen yang sering digunakan
- Data benchmark industri (yang sudah diizinkan untuk digunakan)
- Panduan brand voice dan komunikasi perusahaan
- Notulen rapat penting sebagai referensi

> ⚠️ **PERINGATAN PRIVASI DATA:** Jangan upload dokumen yang berisi data pribadi karyawan (nama, NIK, gaji, data kesehatan) ke Project. Gunakan dokumen kebijakan atau template saja.

---

## 4. Project Instructions: System Prompt untuk Project

Project Instructions adalah instruksi permanen yang selalu aktif di setiap percakapan dalam project. Ini seperti memberitahu Claude "siapa kamu, apa konteksnya, dan bagaimana cara kerjamu" di project ini.

**Cara menulis Project Instructions:**

1. Buka project
2. Klik **"Edit project instructions"** atau ikon pengaturan
3. Tulis instruksi di kotak yang tersedia
4. Klik **"Save"**

**Template Project Instructions untuk HR:**

```
Kamu adalah asisten HR profesional untuk [Nama Perusahaan].

KONTEKS PERUSAHAAN:
- Industri: [industri]
- Jumlah karyawan: [angka]
- Lokasi: [kota/negara]
- Bahasa resmi: Indonesia

CARA KERJA:
- Selalu gunakan bahasa Indonesia yang formal tapi tidak kaku
- Referensikan dokumen yang tersedia di Knowledge jika relevan
- Berikan output dalam format bullet points atau tabel jika memungkinkan
- Tanyakan klarifikasi jika permintaan tidak jelas

AREA FOKUS PROJECT INI:
[Jelaskan fokus project: rekrutmen / L&D / employee relations / dll.]

HAL YANG TIDAK BOLEH DILAKUKAN:
- Jangan membuat keputusan final tentang karyawan (hanya rekomendasi)
- Jangan menjanjikan sesuatu atas nama perusahaan
- Tandai jika ada pertanyaan legal yang butuh konsultasi ahli hukum
```

**Contoh Project Instructions yang lebih spesifik:**

```
Kamu adalah asisten rekrutmen untuk Tim Talent Acquisition PT Maju Bersama.

KONTEKS:
- Kami adalah perusahaan teknologi B2B dengan 300 karyawan
- Sedang dalam fase growth, target hiring 50 orang tahun ini
- Mayoritas posisi: software engineer, product manager, data analyst
- Employer branding tone: inovatif, kolaboratif, growth-oriented

TUGAS UTAMAMU DI PROJECT INI:
- Bantu draft job descriptions yang menarik
- Buat pertanyaan interview yang terstruktur
- Analisis dan rangkum profil kandidat
- Buat komunikasi ke kandidat yang profesional

DOKUMEN REFERENSI:
- Lihat "Competency Framework" untuk standar kompetensi tiap level
- Lihat "Employer Brand Guidelines" untuk tone komunikasi
- Lihat "JD Template" untuk format standar job description kami
```

---

## 5. Berbagi Project dengan Tim

> **Catatan:** Fitur sharing project tersedia di **Claude Team plan**. Jika menggunakan Pro plan individual, project hanya bisa diakses oleh pemilik akun.

**Cara berbagi project (Team plan):**

1. Buka project
2. Klik ikon berbagi / **"Share"** di pojok kanan atas
3. Masukkan email anggota tim yang ingin diundang
4. Pilih level akses:
   - **Can view & chat**: bisa membuat percakapan di project, tidak bisa edit instructions/knowledge
   - **Can edit**: bisa tambah/ubah knowledge dan instructions
5. Kirim undangan
6. Anggota tim akan mendapat email untuk bergabung

**Yang perlu diketahui tentang sharing:**
- Setiap anggota punya percakapan terpisah (tidak melihat chat orang lain secara default)
- Knowledge dan Instructions dibagi bersama
- Admin project bisa mengubah level akses atau remove anggota
- Percakapan bisa di-share secara manual jika perlu

---

## 6. Strategi Organisasi Project untuk HR

**Opsi A: Project per Fungsi HR**
```
📁 Rekrutmen & Talent Acquisition
📁 Learning & Development
📁 Employee Relations & Kebijakan
📁 Performance Management
📁 Compensation & Benefits
```
- Cocok untuk: tim HR yang sudah terbagi per fungsi
- Kelebihan: konteks sangat spesifik per area
- Kekurangan: lebih banyak project yang perlu dikelola

**Opsi B: Project per Program/Inisiatif**
```
📁 Rekrutmen Batch Q1 2025
📁 Program Onboarding 2025
📁 Annual Performance Review 2024
📁 Culture Transformation Project
```
- Cocok untuk: project-project dengan timeline spesifik
- Kelebihan: konteks terpusat per program
- Kekurangan: project menumpuk setelah beberapa tahun

**Opsi C: Project per Tim/Klien Internal**
```
📁 HR Ops Team Workspace
📁 Business Partner - Finance Division
📁 Business Partner - Operations Division
```
- Cocok untuk: HR Business Partner yang melayani divisi berbeda
- Kelebihan: konteks bisnis per divisi tersimpan
- Kekurangan: informasi umum HR harus diulang di tiap project

**Rekomendasi untuk mulai:**
- Buat 2-3 project dulu berdasarkan prioritas pekerjaan
- Gunakan Opsi A atau B, pilih yang paling sesuai dengan cara kerja tim
- Evaluasi setelah 1 bulan, sesuaikan jika perlu

---

## 7. Use Cases Project untuk HR

**Use Case 1: Project Rekrutmen**
- Knowledge: JD template, competency framework, employer brand guide, pertanyaan interview standar
- Instructions: fokus pada rekrutmen, tone antusias dan profesional
- Penggunaan: buat JD, siapkan interview, komunikasi kandidat

**Use Case 2: Project L&D (Learning & Development)**
- Knowledge: learning needs analysis, katalog training, template materi, feedback form
- Instructions: fokus pada adult learning principles, target peserta beragam level
- Penggunaan: buat modul training, kuis evaluasi, jadwal learning

**Use Case 3: Project Employee Relations**
- Knowledge: kebijakan HR (tanpa data karyawan individual), UU Ketenagakerjaan ringkasan, SOP penanganan kasus
- Instructions: pendekatan hati-hati, selalu rekomendasikan konsultasi legal untuk kasus serius
- Penggunaan: draft kebijakan, panduan kasus, komunikasi sensitif

---

## 8. Keterbatasan Projects yang Perlu Diketahui

- **Context window**: Project Knowledge memiliki batas ukuran. Jika terlalu banyak dokumen, Claude mungkin tidak bisa membaca semuanya sekaligus
- **Sharing terbatas di Free/Pro**: Full collaboration hanya di Team plan
- **Tidak real-time**: Jika dua orang mengedit project bersamaan, tidak ada conflict resolution otomatis
- **Tidak ada version control**: Perubahan pada Instructions/Knowledge tidak bisa di-undo
- **Privacy**: Meskipun project dibatasi akses, Anthropic tetap memproses konten sesuai Privacy Policy mereka

---

## Checklist: Setup Project yang Baik

- [ ] Nama project deskriptif dan spesifik
- [ ] Project Instructions ditulis: konteks perusahaan, cara kerja, hal yang tidak boleh dilakukan
- [ ] Dokumen Knowledge: hanya dokumen relevan, bukan dokumen berisi data pribadi karyawan
- [ ] Anggota tim yang tepat sudah diundang (jika pakai Team plan)
- [ ] Level akses sudah diatur dengan benar
- [ ] Coba buat 1 percakapan test untuk verifikasi Instructions berjalan baik

---

## Rangkuman

- Projects = konteks persisten yang tersimpan di semua percakapan dalam satu project
- Bedakan Projects (untuk pekerjaan berkelanjutan) vs Chat biasa (untuk pertanyaan ad-hoc)
- Project Instructions adalah "briefing permanen" untuk Claude - tulis dengan jelas dan spesifik
- Upload dokumen referensi ke Knowledge - hindari dokumen berisi data pribadi karyawan
- Sharing project (Team plan): anggota punya percakapan terpisah tapi berbagi Knowledge & Instructions

---

## Langkah Selanjutnya

- Lanjut ke **INTERMEDIATE-02**: Artifacts - Dokumen, Diagram, dan Output yang Bisa Langsung Digunakan
- Aksi: Buat 1 project HR pertamamu hari ini dan setup Project Instructions
