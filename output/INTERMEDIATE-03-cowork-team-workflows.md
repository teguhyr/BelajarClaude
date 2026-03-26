# Claude dalam Workflow Tim - Kolaborasi dan Sharing

> **Level**: Intermediate - Co-work Track (Modul 3 dari 3)
> **Estimasi Waktu**: 35 menit
> **Prasyarat**: INTERMEDIATE-01 (Projects), INTERMEDIATE-02 (Artifacts)

---

## Tujuan Pembelajaran

- Berbagi percakapan Claude dengan rekan tim
- Membangun workflow berulang menggunakan template percakapan
- Mengintegrasikan Claude ke dalam alat kerja yang sudah ada
- Membangun knowledge base tim dengan bantuan Claude
- Merancang governance penggunaan AI di tim HR

---

## 1. Sharing Conversation: Berbagi Percakapan ke Rekan Tim

Claude memungkinkan kamu berbagi link percakapan yang sudah dilakukan.

**Cara share percakapan:**

1. Buka percakapan yang ingin dibagikan
2. Klik ikon **share** (ikon panah keluar atau rantai link) di pojok kanan atas
3. Pilih **"Share this conversation"**
4. Salin link yang dihasilkan
5. Kirim link ke rekan tim via chat, email, atau Slack

**Yang perlu diketahui tentang shared conversation:**
- Penerima link bisa melihat seluruh isi percakapan (read-only)
- Penerima tidak bisa melanjutkan percakapan yang sama
- Penerima bisa membuat percakapan baru berdasarkan apa yang mereka baca
- Link bisa dibatalkan/dicabut kapan saja oleh pemilik percakapan

**Kapan gunakan fitur ini:**
- Berbagi hasil riset atau analisis Claude ke atasan atau tim
- Menunjukkan prompt yang efektif ke rekan kerja sebagai referensi
- Dokumentasi proses berpikir atau brainstorming
- Handover pekerjaan ke kolega

---

## 2. Membangun Workflow Berulang dengan Template Percakapan

Banyak pekerjaan HR bersifat berulang. Claude bisa dimanfaatkan lebih efisien dengan menyiapkan template prompt standar.

**Cara membuat "template percakapan":**

Simpan prompt standar di dokumen Word, Notion, atau teks file. Ketika butuh, salin dan sesuaikan bagian yang berubah.

**Contoh template yang bisa dibuat tim HR:**

---

**Template A: Screening Kandidat**
```
Saya akan share data kandidat untuk posisi [NAMA POSISI].
Analisis profil kandidat berikut dan berikan:
1. Kesesuaian dengan requirement posisi (skala 1-5 dengan justifikasi)
2. Kekuatan utama kandidat (3 poin)
3. Gap atau area yang perlu diverifikasi saat interview (2-3 poin)
4. Rekomendasi: lanjut ke interview / tidak lanjut / perlu informasi tambahan

Data kandidat:
[PASTE INFORMASI KANDIDAT DI SINI - TANPA DATA SENSITIF]
```

---

**Template B: Feedback Meeting 1-on-1**
```
Bantu saya menyiapkan pertanyaan untuk sesi 1-on-1 dengan karyawan.
Konteks karyawan:
- Posisi: [POSISI]
- Lama bekerja: [DURASI]
- Situasi saat ini: [JELASKAN KONDISI/KONTEKS]

Buatkan:
- 5 pertanyaan check-in (how are you doing, wellbeing)
- 3 pertanyaan tentang progress dan tantangan pekerjaan
- 2 pertanyaan tentang development dan karir
- 1 pertanyaan penutup yang open-ended
```

---

**Template C: Draft Kebijakan Baru**
```
Bantu saya membuat draft awal kebijakan HR tentang [TOPIK KEBIJAKAN].
Konteks:
- Latar belakang mengapa kebijakan ini dibuat: [JELASKAN]
- Siapa yang terdampak: [KELOMPOK KARYAWAN]
- Hal-hal yang sudah pasti (tidak bisa diganggu gugat): [LIST JIKA ADA]

Buat dalam format dokumen kebijakan standar:
tujuan, ruang lingkup, definisi, ketentuan, sanksi, tanggal berlaku.
```

---

**Tips mengelola template:**
- Simpan template di Notion, Google Doc, atau file teks yang mudah diakses tim
- Beri nama yang jelas: "Template_Screening_Kandidat_v2.txt"
- Review dan update template secara berkala (tiap 3-6 bulan)
- Tambahkan instruksi cara penggunaan di atas tiap template

---

## 3. Integrasi Claude ke Workflow yang Sudah Ada

Claude paling efektif jika diintegrasikan ke dalam cara kerja yang sudah ada, bukan menggantikan alat yang sudah berjalan.

**Integrasi dengan Notion:**
- Buat dokumen di Notion, copy ke Claude untuk di-review atau dikembangkan
- Minta Claude buat konten, copy hasilnya ke Notion
- Buat Project Claude dengan knowledge dari dokumen Notion

**Integrasi dengan Email:**
- Copy draft email ke Claude untuk dipoles sebelum dikirim
- Minta Claude buat balasan email yang sensitif dengan nada yang tepat
- Buat template email standar HR dengan Claude, simpan di email client

**Integrasi dengan Excel/Google Sheets:**
- Paste data mentah (yang sudah dianonimkan) ke Claude untuk analisis
- Minta Claude buat formula Excel (lihat INTERMEDIATE-04)
- Minta Claude interpretasikan data dan buat narasi insight

**Integrasi dengan Slack/Teams:**
- Copy percakapan Slack yang perlu ditindaklanjuti ke Claude untuk ringkasan
- Minta Claude draft pesan Slack yang profesional untuk situasi sulit
- Buat pesan pengumuman tim yang engaging

**Pola kerja yang efektif:**
```
Kerjakan di alat utama → Copy ke Claude untuk improvement → Copy kembali ke alat utama
```

---

## 4. Mendelegasikan Riset ke Claude

Claude bisa melakukan riset yang biasanya memakan banyak waktu HR.

**Jenis riset yang bisa didelegasikan:**

| Topik Riset | Cara Mendelegasikan |
|-------------|-------------------|
| Best practice HR | "Apa saja best practice global untuk program [topik]?" |
| Benchmark industri | "Apa struktur kompensasi umum untuk posisi [X] di industri [Y] di Indonesia?" |
| Framework dan metodologi | "Jelaskan framework OKR vs KPI beserta kelebihan dan kekurangannya" |
| Regulasi ketenagakerjaan | "Ringkaskan ketentuan cuti melahirkan menurut UU Ketenagakerjaan Indonesia" |
| Tren HR | "Apa tren L&D yang relevan untuk tahun 2025 di Asia Tenggara?" |

**Cara mendelegasikan riset dengan efektif:**

```
Lakukan riset tentang [TOPIK] untuk kebutuhan saya sebagai HR professional.
Yang saya butuhkan:
- Penjelasan konsep dasar (untuk saya yang sudah familiar dengan HR)
- 3-5 best practice yang bisa langsung diaplikasikan
- Contoh konkret implementasi di perusahaan (bisa fiktif tapi realistis)
- Hal-hal yang sering menjadi kendala dan cara mengatasinya
- Referensi atau sumber lebih lanjut (framework, buku, metodologi)

Format: ringkas, bullet points, gunakan heading yang jelas.
```

> **Peringatan:** Selalu verifikasi informasi regulasi dan hukum ketenagakerjaan dari sumber resmi. Claude bisa salah atau memiliki informasi yang tidak ter-update.

---

## 5. Membangun Knowledge Base Tim dengan Claude

Claude bisa membantu membangun dan mengorganisir pengetahuan tim HR.

**Cara membangun knowledge base:**

**Langkah 1: Identifikasi knowledge yang perlu didokumentasikan**
```
Bantu saya mengidentifikasi knowledge penting yang perlu
didokumentasikan oleh tim HR kami. Kami adalah tim HR 5 orang
di perusahaan manufaktur 800 karyawan.
Buat daftar dalam kategori: proses, kebijakan, kontak penting, template.
```

**Langkah 2: Buat template dokumentasi**
```
Buatkan template dokumentasi untuk proses HR yang bisa digunakan
konsisten oleh seluruh tim. Template harus mencakup:
nama proses, tujuan, penanggung jawab, langkah-langkah,
dokumen terkait, tanggal update terakhir.
```

**Langkah 3: Review dan enrichment dokumen yang sudah ada**
```
[Upload dokumen SOP yang sudah ada]
Review dokumen ini dan identifikasi:
1. Informasi yang sudah outdated atau perlu diverifikasi
2. Bagian yang ambigu atau perlu penjelasan lebih
3. Gap informasi yang penting tapi belum ada
4. Saran perbaikan format agar lebih mudah dipahami
```

---

## 6. Governance: Panduan Penggunaan Claude di Tim

Penggunaan AI di tim perlu diatur agar konsisten, aman, dan efektif.

**Hal yang perlu diputuskan dan dikomunikasikan ke tim:**

**A. Apa yang boleh dan tidak boleh:**
- Data apa yang boleh di-paste ke Claude (lihat BASIC-04 bagian Do's and Don'ts)
- Jenis keputusan yang boleh dipengaruhi oleh Claude (vs yang harus murni keputusan manusia)
- Konten apa yang perlu di-review sebelum digunakan secara resmi

**B. Standar penggunaan:**
- Model Claude mana yang digunakan (Sonnet sebagai default)
- Apakah menggunakan akun personal atau akun perusahaan
- Bagaimana cara mendokumentasikan percakapan Claude yang penting

**C. Review dan quality control:**
- Siapa yang bertanggung jawab review output Claude sebelum digunakan
- Bagaimana tanda jika konten dibuat dengan bantuan Claude
- Proses jika ditemukan output Claude yang salah atau menyesatkan

**Template SOP Penggunaan Claude untuk Tim HR:**

```
SOP PENGGUNAAN AI ASSISTANT (CLAUDE) - TIM HR
[Nama Perusahaan]

1. TUJUAN
   Panduan ini mengatur cara penggunaan Claude AI secara bertanggung jawab
   di Tim HR untuk meningkatkan produktivitas sambil menjaga keamanan data.

2. YANG DIIZINKAN
   ✅ Membuat draft dokumen HR (selalu review sebelum finalisasi)
   ✅ Menganalisis data yang sudah dianonimkan
   ✅ Riset best practice dan referensi
   ✅ Brainstorming program dan inisiatif HR

3. YANG TIDAK DIIZINKAN
   ❌ Upload data karyawan yang mengidentifikasi individu
   ❌ Paste informasi gaji atau kompensasi spesifik per karyawan
   ❌ Paste data kesehatan atau catatan disiplin karyawan
   ❌ Menggunakan output Claude tanpa review manusia untuk dokumen resmi

4. STANDAR QUALITY CONTROL
   - Semua dokumen yang dibuat dengan Claude harus di-review oleh minimal 1 orang
   - Tambahkan catatan internal: "Draft awal dibuat dengan bantuan Claude,
     di-review oleh [nama] pada [tanggal]"

5. PELAPORAN MASALAH
   Jika menemukan output Claude yang salah atau berpotensi merugikan,
   laporkan ke [nama/jabatan PIC] segera.
```

---

## 7. Contoh Workflow Lengkap: Persiapan Town Hall Meeting

Berikut contoh bagaimana Claude membantu dari awal sampai akhir:

**Konteks:** HR diminta menyiapkan konten Town Hall Meeting kuartalan.

---

**Langkah 1: Brainstorming agenda**
```
Kami akan menyelenggarakan Town Hall Meeting kuartalan untuk 500 karyawan.
Durasi: 2 jam. Topik yang perlu disampaikan: update strategi perusahaan,
pencapaian Q3, program baru: flextime dan wellness.
Bantu saya susun agenda yang engaging dan tidak membosankan.
```

---

**Langkah 2: Draft pesan CEO**
```
Buatkan draft pembukaan CEO untuk Town Hall ini (3-4 menit bicara).
Nada: inspiratif, jujur tentang tantangan, optimis tentang masa depan.
Poin kunci yang harus masuk: [list poin dari brief yang diberikan CEO]
```

---

**Langkah 3: Sesi Q&A - Antisipasi pertanyaan**
```
Sesi Town Hall akan ada Q&A terbuka. Bantu kami antisipasi pertanyaan
sulit yang mungkin ditanyakan karyawan tentang topik:
- Program flextime baru
- Apakah ada PHK di tahun depan?
- Kenapa kenaikan gaji tahun ini lebih kecil dari tahun lalu?

Untuk setiap pertanyaan, berikan draft jawaban yang jujur, empatik,
dan tidak defensif. Tandai jika ada pertanyaan yang butuh konsultasi
legal sebelum dijawab.
```

---

**Langkah 4: Materi komunikasi pasca Town Hall**
```
Buatkan email follow-up yang dikirim ke seluruh karyawan setelah
Town Hall selesai. Sertakan: ringkasan poin utama, link rekaman
(placeholder), cara karyawan bisa submit pertanyaan lanjutan,
dan next steps yang perlu diketahui karyawan.
```

---

## Rangkuman

- Share conversation: bagikan link percakapan ke tim untuk referensi atau handover
- Buat dan simpan template prompt standar untuk pekerjaan berulang
- Integrasikan Claude ke dalam alat yang sudah ada (Notion, email, spreadsheet)
- Gunakan Claude untuk riset yang biasanya memakan waktu - selalu verifikasi info penting
- Buat governance sederhana tentang apa yang boleh dan tidak boleh dilakukan dengan Claude

---

## Langkah Selanjutnya

- **Co-work Track selesai!** Kamu sudah menguasai Projects, Artifacts, dan Team Workflows.
- Lanjut ke **Code Track** jika ingin belajar tentang fitur kode Claude: **INTERMEDIATE-04**
- Atau kembali ke **README-training.md** untuk melihat path lain yang tersedia
