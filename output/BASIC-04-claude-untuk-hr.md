# Claude untuk HR Professionals - Use Cases Harian

> **Level**: Basic
> **Estimasi Waktu**: 35 menit
> **Prasyarat**: BASIC-03 (Cara Menulis Prompt yang Efektif)

---

## Tujuan Pembelajaran

- Menggunakan Claude untuk 6 use case HR paling umum
- Memahami workflow rekrutmen end-to-end dengan Claude
- Mengetahui batasan penggunaan yang aman terkait data karyawan
- Mengaplikasikan Claude langsung dalam pekerjaan HR sehari-hari

---

## 1. Menulis Job Description

Job description yang baik menarik kandidat yang tepat dan menjadi dasar evaluasi kinerja.

**Cara menggunakan Claude:**

```
Saya HR di perusahaan [industri] dengan [jumlah] karyawan.
Buatkan job description untuk posisi [nama posisi] dengan detail:
- Departemen: [nama departemen]
- Melaporkan kepada: [jabatan atasan]
- Pengalaman minimal: [X tahun]
- Skills utama yang dibutuhkan: [list skills]
- Lokasi: [kota/remote/hybrid]

Format: ringkasan posisi (2-3 kalimat), tanggung jawab utama (7-8 poin),
kualifikasi wajib (5 poin), kualifikasi tambahan/nice-to-have (3 poin),
apa yang kami tawarkan (3-4 poin benefit utama).
```

**Tips:**
- Minta Claude untuk membuat 2-3 versi dengan nada berbeda (formal vs casual)
- Minta Claude review JD yang sudah ada untuk bias gender atau inklusi
- Gunakan Claude untuk menerjemahkan JD ke bahasa Inggris jika perlu

---

## 2. Menyusun Pertanyaan Interview

Pertanyaan yang tepat membantu menilai kandidat secara objektif dan terstruktur.

**Contoh prompt:**

```
Buatkan panduan interview terstruktur untuk posisi Marketing Manager.
Sertakan:
- 3 pertanyaan pembuka (rapport building)
- 3 pertanyaan behavioral (gunakan format STAR)
- 3 pertanyaan tentang kompetensi teknis marketing digital
- 2 pertanyaan situasional tentang kepemimpinan tim
- 2 pertanyaan penutup (motivasi dan ekspektasi)

Untuk setiap pertanyaan, tambahkan:
- Kompetensi yang dinilai
- Indikator jawaban yang baik (1-2 poin)
```

**Cara lanjutan:**
- Minta Claude membuat rubrik penilaian untuk setiap pertanyaan
- Minta Claude membuat versi pertanyaan follow-up untuk setiap pertanyaan utama

---

## 3. Membuat Template Email HR

Claude sangat efektif untuk membuat email HR yang profesional, konsisten, dan empatik.

**Jenis email yang bisa dibuat Claude:**

| Jenis Email | Keterangan |
|-------------|-----------|
| Undangan interview | Jadwal, lokasi, format interview, dokumen yang dibawa |
| Penolakan lamaran | Profesional, encouraging, buka peluang masa depan |
| Offer letter | Posisi, kompensasi, start date, next steps |
| Email selamat datang | Onboarding info, first day schedule, kontak penting |
| Email peringatan kinerja | Formal, fact-based, tidak judgemental |
| Pengumuman internal | Perubahan kebijakan, info perusahaan, event |

**Contoh prompt untuk offer letter:**

```
Buatkan draft offer letter untuk kandidat yang akan bergabung sebagai
[posisi]. Sertakan placeholder untuk:
- Nama kandidat
- Tanggal mulai bekerja
- Gaji bulanan (gross)
- Tunjangan dan fasilitas
- Deadline konfirmasi

Nada: profesional tapi hangat dan antusias. Bahasa Indonesia.
Sertakan kalimat yang menegaskan bahwa ini adalah conditional offer
(tergantung penyelesaian background check dan administrasi).
```

---

## 4. Meringkas Dokumen Kebijakan

Claude bisa membaca dokumen panjang dan menghasilkan ringkasan yang mudah dipahami.

**Cara penggunaan:**

1. Upload PDF atau paste teks dokumen
2. Minta Claude untuk meringkas dengan format tertentu

**Contoh prompt:**

```
[Setelah upload dokumen kebijakan]

Tolong bantu saya memproses dokumen kebijakan ini:
1. Buatkan ringkasan eksekutif (maks 200 kata)
2. Daftar 10 poin paling penting yang perlu diketahui karyawan
3. FAQ: 5 pertanyaan yang kemungkinan besar akan ditanyakan karyawan
   beserta jawabannya berdasarkan dokumen ini
4. Tandai jika ada bagian yang ambigu atau perlu klarifikasi lebih lanjut
```

**Use cases populer:**
- Meringkas peraturan pemerintah terbaru (UU Ketenagakerjaan, PP, dll.)
- Membuat versi "easy read" dari kebijakan HR yang panjang
- Mengekstrak action items dari notulen rapat

---

## 5. Membuat Materi Training Sederhana

Claude bisa membantu merancang struktur dan konten materi training.

**Contoh prompt:**

```
Buatkan outline materi training untuk topik "Pencegahan Kecelakaan Kerja"
Target peserta: operator pabrik, pendidikan SMA/SMK.
Durasi training: 2 jam.

Format outline:
- Tujuan pembelajaran (3-4 poin)
- Agenda (dengan alokasi waktu tiap sesi)
- Konten tiap sesi (poin-poin utama)
- Aktivitas dan diskusi yang bisa dilakukan
- Cara evaluasi pemahaman peserta
- Materi visual/slide yang direkomendasikan
```

**Tips penggunaan lebih lanjut:**
- Minta Claude membuat konten slide per slide
- Minta Claude membuat kuis evaluasi (pilihan ganda atau essay)
- Minta Claude membuat handout ringkasan untuk peserta

---

## 6. Analisis Data Survei Karyawan

Claude bisa membantu menganalisis data survei dan mengidentifikasi insight penting.

> ⚠️ **PERINGATAN PRIVASI DATA:** Sebelum paste data survei ke Claude, pastikan data sudah dianonimkan. Hapus nama, NIK, departemen kecil yang bisa mengidentifikasi individu. Gunakan data agregat atau generalisasi.

**Format yang aman untuk dipaste:**

```
Saya punya hasil survei engagement karyawan. Data sudah dianonimkan.
Berikut hasil per pertanyaan (skala 1-5):

Q1 "Saya merasa pekerjaan saya bermakna": Rata-rata 3.8, SD 0.9
Q2 "Atasan saya memberikan feedback yang berguna": Rata-rata 2.9, SD 1.2
Q3 "Saya memiliki peluang berkembang di perusahaan": Rata-rata 2.7, SD 1.1
[dst...]

Responden: 150 karyawan, response rate 78%.

Tolong analisis dan berikan:
1. Temuan utama (3-5 poin)
2. Area yang paling perlu perhatian (prioritas tinggi)
3. Kemungkinan root cause untuk skor rendah
4. Rekomendasi program HR (konkret dan actionable)
5. Pertanyaan lanjutan yang perlu diinvestigasi
```

---

## 7. Workflow Rekrutmen End-to-End dengan Claude

Berikut contoh bagaimana Claude bisa membantu di setiap tahap rekrutmen:

```
TAHAP 1: PERSIAPAN
├── Buat/update job description → Prompt Template 1 (BASIC-03)
├── Buat pertanyaan interview → Prompt Template 3 (BASIC-03)
└── Siapkan rubrik penilaian → Minta Claude buat scoring guide

TAHAP 2: SOURCING & SCREENING
├── Buat posting iklan lowongan (LinkedIn, jobboard) → Claude
├── Buat template screening call → Claude
└── Rangkum CV kandidat (paste teks CV) → Claude

TAHAP 3: INTERVIEW
├── Cetak panduan interview dari Claude
├── Minta Claude buat catatan template evaluasi
└── Setelah interview: minta Claude bantu strukturkan catatan evaluasi

TAHAP 4: SELEKSI & OFFER
├── Minta Claude bantu komparasi kandidat berdasarkan catatan kamu
├── Buat draft offer letter → Prompt Template 5 (BASIC-03)
└── Buat email penolakan untuk kandidat yang tidak terpilih

TAHAP 5: ONBOARDING
├── Buat rencana onboarding 30-60-90 hari → Prompt Template 6 (BASIC-03)
├── Buat email selamat datang → Claude
└── Buat checklist dokumen yang perlu disiapkan karyawan baru
```

---

## 8. Do's and Don'ts: Privasi Data Karyawan

**DO (Boleh dilakukan):**
- Paste data yang sudah dianonimkan (tanpa nama, NIK, info pribadi)
- Gunakan data agregat (rata-rata, persentase, tren)
- Buat contoh/template dengan nama fiktif
- Paste kebijakan atau dokumen umum perusahaan (bukan confidential)
- Paste CV kandidat untuk dianalisis (dengan izin kandidat, idealnya)

**DON'T (Jangan dilakukan):**
- Paste data gaji spesifik per individu dengan nama
- Paste catatan disiplin yang bisa mengidentifikasi karyawan tertentu
- Paste data kesehatan atau informasi sensitif karyawan
- Paste informasi trade secret atau strategi bisnis sangat rahasia
- Paste data login, password, atau informasi keamanan sistem

> **Prinsip panduan:** Tanya pada diri sendiri: "Apakah saya nyaman jika orang lain membaca data ini?" Jika tidak, jangan paste ke Claude.

---

## Rangkuman

- Claude bisa membantu hampir semua tugas HR harian: JD, interview, email, ringkasan dokumen, training, survei
- Gunakan prompt dengan konteks yang jelas untuk hasil yang lebih relevan
- Workflow rekrutmen end-to-end bisa dipercepat signifikan dengan Claude
- Selalu anonimkan data sebelum paste ke Claude
- Review semua output Claude sebelum digunakan secara resmi

---

## Langkah Selanjutnya

- Kamu telah menyelesaikan **Level Basic**!
- Lanjut ke **Level Intermediate** berdasarkan kebutuhanmu:
  - **Path Co-work**: INTERMEDIATE-01 (Projects & Shared Context)
  - **Path Code**: INTERMEDIATE-04 (Code Dasar untuk HR)
  - **Path Lengkap**: Mulai dari INTERMEDIATE-01
