# Cara Menulis Prompt yang Efektif

> **Level**: Basic
> **Estimasi Waktu**: 30 menit
> **Prasyarat**: BASIC-02 (Setup dan Antarmuka)

---

## Tujuan Pembelajaran

- Memahami anatomi prompt yang baik
- Mengenali kesalahan umum dalam menulis prompt
- Menggunakan teknik role prompting dan few-shot prompting
- Menggunakan 10 template prompt siap pakai untuk HR
- Memperbaiki prompt yang kurang efektif

---

## 1. Anatomi Prompt yang Baik

Prompt yang efektif terdiri dari 4 elemen kunci:

```
[KONTEKS] + [TUGAS] + [FORMAT] + [BATASAN]
```

**Penjelasan tiap elemen:**

| Elemen | Penjelasan | Contoh |
|--------|-----------|--------|
| **Konteks** | Siapa kamu, situasi apa, untuk siapa | "Saya HR Manager di perusahaan retail dengan 200 karyawan" |
| **Tugas** | Apa yang harus Claude lakukan | "Buatkan template email penolakan lamaran kerja" |
| **Format** | Bagaimana bentuk outputnya | "Format: subjek email, isi email, penutup. Panjang: maks 150 kata" |
| **Batasan** | Hal yang perlu dihindari atau diperhatikan | "Gunakan bahasa formal tapi tetap hangat dan tidak terkesan dingin" |

**Contoh prompt lengkap:**

```
Saya HR Manager di perusahaan teknologi startup dengan 80 karyawan.
Buatkan template email untuk memberitahu kandidat bahwa mereka tidak
lolos tahap interview akhir.

Format yang diinginkan:
- Subjek email
- Paragraf pembuka (apresiasi)
- Alasan penolakan (umum, tidak spesifik)
- Paragraf penutup (encouragement)
- Tanda tangan

Ketentuan: bahasa Indonesia formal tapi hangat, maksimal 200 kata,
hindari bahasa yang terkesan judgemental atau merendahkan.
```

---

## 2. Kesalahan Umum Pemula

**Kesalahan #1: Terlalu singkat tanpa konteks**

❌ Buruk:
```
Buatkan job description.
```

✅ Baik:
```
Buatkan job description untuk posisi HR Generalist di perusahaan
manufaktur skala menengah (500 karyawan). Pengalaman minimal 3 tahun.
Format standar: ringkasan posisi, tanggung jawab (bullet), kualifikasi
wajib, kualifikasi tambahan.
```

---

**Kesalahan #2: Tidak menyebutkan format output**

❌ Buruk:
```
Apa saja manfaat program Employee Assistance Program (EAP)?
```

✅ Baik:
```
Apa saja manfaat program Employee Assistance Program (EAP)?
Sajikan dalam format:
1. Manfaat bagi karyawan (5 poin)
2. Manfaat bagi perusahaan (5 poin)
3. Cara mengkomunikasikan EAP ke karyawan (3 poin praktis)
```

---

**Kesalahan #3: Tidak memberikan batasan yang penting**

❌ Buruk:
```
Buatkan pertanyaan interview untuk posisi Finance Manager.
```

✅ Baik:
```
Buatkan 8 pertanyaan interview untuk posisi Finance Manager di
perusahaan FMCG. Fokus pada: kemampuan analitis, pengalaman budgeting,
dan kepemimpinan tim. Hindari pertanyaan yang terlalu teknis akuntansi
karena itu akan diuji via tes tertulis terpisah. Sertakan tujuan
setiap pertanyaan dalam satu kalimat singkat.
```

---

## 3. Teknik Role Prompting

Role prompting = meminta Claude untuk berperan sebagai seseorang dengan keahlian tertentu.

**Template:**
```
Kamu adalah [peran/jabatan] dengan [pengalaman/keahlian] di bidang [area].
[Lanjutkan dengan tugas]
```

**Contoh penggunaan:**

```
Kamu adalah seorang HR Consultant berpengalaman 15 tahun yang spesialis
dalam Change Management. Klienku adalah perusahaan manufaktur yang akan
melakukan restrukturisasi besar-besaran dan mengurangi 20% headcount.

Berikan rekomendasi: apa saja langkah komunikasi yang perlu disiapkan
HR sebelum pengumuman resmi dilakukan? Buat dalam format checklist.
```

**Kapan gunakan role prompting:**
- Butuh perspektif spesifik dari suatu profesi
- Ingin output yang lebih fokus dan profesional
- Topik yang membutuhkan sudut pandang ahli

---

## 4. Teknik Few-Shot Prompting

Few-shot prompting = memberikan contoh format output yang diinginkan sebelum meminta Claude mengerjakan tugasnya.

**Template:**
```
Saya butuh [tugas]. Berikut contoh format yang saya inginkan:

CONTOH INPUT: [contoh 1]
CONTOH OUTPUT: [output yang diinginkan 1]

CONTOH INPUT: [contoh 2]
CONTOH OUTPUT: [output yang diinginkan 2]

Sekarang, tolong kerjakan untuk:
INPUT: [input aktual kamu]
```

**Contoh praktis:**

```
Saya butuh mengubah feedback kinerja yang kasar menjadi bahasa yang
konstruktif. Berikut contoh:

INPUT: "Karyawan ini lambat dan sering bikin kesalahan"
OUTPUT: "Karyawan perlu meningkatkan kecepatan kerja dan akurasi.
Disarankan untuk membuat checklist tugas harian dan mendapat coaching
dari senior untuk area yang sering terjadi kesalahan."

INPUT: "Dia tidak bisa kerja sama dengan tim sama sekali"
OUTPUT: "Karyawan perlu mengembangkan kemampuan kolaborasi. Disarankan
mengikuti program team building dan coaching tentang komunikasi efektif."

Sekarang ubah feedback ini:
INPUT: "Presentasinya membosankan dan tidak ada yang ngerti"
```

---

## 5. Teknik Lanjutan: Iterasi Bertahap

Claude bekerja paling baik dalam percakapan bertahap, bukan satu prompt raksasa.

**Pola yang efektif:**

```
Langkah 1 → Minta draft awal
Langkah 2 → Minta revisi spesifik
Langkah 3 → Minta versi final atau variasi
```

**Contoh iterasi:**

```
[Pesan 1]
Buatkan draft kebijakan WFH (Work From Home) untuk perusahaan kami.
Fokus dulu pada: eligibilitas karyawan dan jam kerja yang berlaku.

[Setelah menerima draft]
[Pesan 2]
Bagus. Sekarang tambahkan bagian tentang: peralatan kerja,
keamanan data, dan cara monitoring produktivitas.

[Setelah menerima tambahan]
[Pesan 3]
Sekarang susun semua bagian menjadi dokumen kebijakan yang rapi
dengan header dan format profesional. Tambahkan bagian "Tanggal Berlaku"
dan "Review Berikutnya".
```

---

## 6. Template Prompt Siap Pakai untuk HR

Salin dan sesuaikan template berikut dengan kebutuhan kamu:

---

**Template 1: Job Description**
```
Buatkan job description untuk posisi [nama posisi] di perusahaan kami.
Industri: [industri]. Ukuran perusahaan: [jumlah karyawan].
Pengalaman yang dibutuhkan: [X tahun].
Skills utama: [skill 1], [skill 2], [skill 3].
Format: ringkasan posisi, tanggung jawab utama (6-8 poin),
kualifikasi wajib (5 poin), kualifikasi tambahan (3 poin).
Bahasa: Indonesia formal.
```

**Template 2: Email Penolakan Lamaran**
```
Buatkan email penolakan lamaran yang profesional dan empatik.
Posisi: [nama posisi]. Tahap seleksi: [tahap mana ditolak].
Nada: hangat dan encouraging, bukan dingin atau judgemental.
Maksimal 150 kata. Sertakan kemungkinan untuk melamar di masa depan.
```

**Template 3: Pertanyaan Interview**
```
Buatkan [jumlah] pertanyaan interview untuk posisi [nama posisi].
Fokus pada: [area 1], [area 2], [area 3].
Sertakan: 2 pertanyaan behavioral (STAR method), 2 situasional,
sisanya teknis/kompetensi. Tambahkan tujuan tiap pertanyaan.
```

**Template 4: Ringkasan Dokumen**
```
[Upload dokumen atau paste teksnya]
Buatkan ringkasan dokumen ini dalam format:
- Tujuan dokumen (1 kalimat)
- Poin utama (5-7 bullet)
- Action items yang perlu dilakukan HR (jika ada)
- Pertanyaan yang mungkin muncul dari karyawan (3-5 poin)
```

**Template 5: Email Internal/Pengumuman**
```
Buatkan email pengumuman [topik] untuk seluruh karyawan.
Konteks: [jelaskan situasinya].
Nada: [formal/semi-formal], [positif/netral].
Sertakan: apa yang berubah, kapan berlaku, siapa yang terdampak,
cara mendapatkan informasi lebih lanjut.
Tanda tangan: [nama tim atau jabatan].
```

**Template 6: Rencana Onboarding**
```
Buatkan rencana onboarding 30-60-90 hari untuk karyawan baru
posisi [nama posisi] di [departemen].
Setiap fase: tujuan utama, aktivitas kunci (bullet),
milestone yang diharapkan tercapai.
```

**Template 7: Analisis Survei Karyawan**
```
[Paste hasil survei atau data mentah]
Analisis data survei karyawan ini. Berikan:
- Temuan utama (3-5 poin)
- Area yang perlu perhatian segera
- Rekomendasi program/intervensi HR (prioritas)
- Pertanyaan lanjutan yang perlu diinvestigasi
```

**Template 8: SOP atau Prosedur**
```
Buatkan SOP (Standard Operating Procedure) untuk proses [nama proses].
Departemen: HR. Target pengguna: [siapa yang akan menggunakan SOP ini].
Format: tujuan, ruang lingkup, langkah-langkah (numbered),
dokumen terkait, catatan penting.
```

**Template 9: Materi Training Singkat**
```
Buatkan modul training singkat tentang [topik] untuk [target peserta].
Durasi training: [X menit/jam].
Format: tujuan pembelajaran, konten utama (3-4 bagian),
aktivitas/diskusi yang bisa dilakukan, poin evaluasi.
```

**Template 10: Feedback Kinerja Konstruktif**
```
Bantu saya menulis feedback kinerja yang konstruktif untuk karyawan
yang [deskripsikan situasi/perilaku yang perlu diperbaiki].
Nada: jujur tapi supportive, fokus pada perbaikan bukan blame.
Format STAR jika relevan. Sertakan saran pengembangan konkret.
```

---

## 7. Latihan: Perbaiki Prompt Ini

Coba perbaiki 3 prompt berikut sebelum melihat jawabannya:

**Prompt buruk 1:**
```
Tulis kebijakan lembur.
```

**Prompt buruk 2:**
```
Saya punya masalah dengan karyawan yang sering terlambat.
```

**Prompt buruk 3:**
```
Buat presentasi tentang pentingnya L&D.
```

*(Coba tulis versi yang lebih baik, lalu bandingkan dengan template di atas.)*

---

## Rangkuman

- Prompt efektif = Konteks + Tugas + Format + Batasan
- Hindari prompt terlalu singkat tanpa konteks atau format
- Role prompting: minta Claude berperan sebagai ahli tertentu
- Few-shot prompting: beri contoh format output sebelum tugas sebenarnya
- Gunakan iterasi bertahap untuk hasil yang lebih baik daripada satu prompt panjang
- 10 template siap pakai tersedia untuk tugas HR harian

---

## Langkah Selanjutnya

- Lanjut ke **BASIC-04**: Claude untuk use cases HR sehari-hari
- Latihan: Gunakan minimal 3 template dari modul ini untuk pekerjaan nyata kamu minggu ini
