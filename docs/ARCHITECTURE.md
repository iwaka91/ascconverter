# Arsitektur ASC Converter

## 1. Bentuk aplikasi

ASC Converter dibangun sebagai aplikasi browser-first dengan source utama berupa satu file HTML besar yang memuat UI, state aplikasi, parser XML, render jadwal, pengaturan, project persistence, export, dan utilitas lain.

Pendekatan single-file dipilih untuk distribusi sederhana, pengujian lintas perangkat, dan jalur portable/offline di masa depan.

## 2. Alur data

```text
XML aSc Timetables
        ↓
Parser ASC
        ↓
AppState / data terstruktur
        ↓
Lapisan pascaproses
  - waktu manual
  - istirahat
  - kegiatan manual
  - JP tambahan
  - edit slot jadwal
        ↓
Renderer
  - Dashboard
  - Jadwal Induk
  - Jadwal Guru
  - Jadwal Kelas
  - Beban Mengajar
        ↓
Export / Project
  - Excel
  - PNG
  - .asccv
```

## 3. Parser invariant

Fungsi inti berikut diperlakukan sebagai bagian sensitif dan sebisa mungkin tidak diubah pada patch UI/UX:

- `parseASCXML()`
- `applyDaysConfig()`
- `processData()`

Riwayat pengembangan menunjukkan perubahan terlalu ketat pada parser dapat mengurangi kompatibilitas XML. Karena itu perubahan baru lebih diarahkan ke lapisan pascaparsing.

## 4. Timeline

Timeline menggabungkan JP hasil XML, konfigurasi waktu default/manual, istirahat, kegiatan sekolah, kegiatan manual, dan JP tambahan.

Prinsip penting:

- `Catatan saja` tidak menggeser timeline.
- `Sisipkan ke jadwal` memengaruhi waktu setelah titik penyisipan sesuai konteks.
- Kegiatan khusus kelas tidak boleh menggeser kelas lain.
- Kegiatan paralel pada waktu identik perlu ditampilkan sejajar pada Jadwal Induk.

## 5. Editor Jadwal Induk

Jadwal Induk berfungsi sebagai editor melalui ikon pensil per sel.

Edit manual disimpan sebagai lapisan override, bukan perubahan raw XML. Ini memungkinkan reset ke data ASC asli, sinkronisasi ke Jadwal Guru/Kelas, penyimpanan melalui `.asccv`, dan penggunaan hasil edit pada export.

## 6. JP Tambahan

JP Tambahan dipakai untuk menambahkan period setelah JP terakhir pada hari tertentu dan bersifat global untuk semua kelas pada hari terpilih.

## 7. Bilingual system

UI mendukung Indonesia dan English. Data asli dari XML seperti nama guru, mata pelajaran, kode, dan kelas tidak diterjemahkan secara paksa.

Export Excel mengikuti bahasa UI untuk label dan struktur yang dibuat aplikasi.

## 8. Export

### Excel

Untuk output yang masih dapat diedit dan diolah kembali.

### PNG

Untuk jadwal yang cukup ringkas, terutama Jadwal Guru dan Jadwal Kelas. Jadwal Induk tidak dianjurkan sebagai PNG karena kepadatan datanya terlalu tinggi.

Prompt Builder menghasilkan prompt English untuk mempercantik PNG melalui image generator eksternal tanpa mengubah fakta jadwal.
