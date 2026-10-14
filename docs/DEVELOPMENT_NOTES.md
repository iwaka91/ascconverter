# Catatan Pengembangan

## Tujuan produk

ASC Converter dikembangkan untuk membantu sekolah menggunakan hasil aSc Timetables secara lebih praktis setelah proses penyusunan jadwal selesai.

> aSc Timetables membuat jadwal, ASC Converter membantu merapikan, menyesuaikan, membaca, menyimpan, dan mengekspor hasilnya.

## Prinsip pengembangan

1. Parser kompatibel lebih penting daripada parser terlalu ketat.
2. Data XML asli tidak dimodifikasi; penyesuaian manual dibuat pada lapisan aplikasi.
3. UI harus usable di tablet Android, desktop, dan laptop. Mobile tetap responsif tetapi bukan target utama pengelolaan jadwal kompleks.
4. Bahasa Indonesia dan English harus konsisten pada UI dan export.
5. Pengguna tidak dipaksa memahami struktur XML.
6. Output Excel dan PNG memiliki fungsi berbeda.
7. Prompt Builder tidak menjalankan AI di dalam ASC Converter; pengguna mengunggah PNG ke image generator eksternal.

## Keputusan UX penting

- Menu Proyek ditempatkan di sidebar, bukan selalu di header.
- Header dijaga tetap sederhana.
- Toggle bahasa `ID / EN` tersedia di header dan pengaturan bahasa tetap dipertahankan.
- Nama guru di Jadwal Induk bukan tautan agar pengguna tidak tersesat akibat salah klik.
- Jadwal Induk dapat diedit melalui ikon pensil per sel.
- Input Android tidak boleh memicu render ulang setiap karakter karena dapat menutup keyboard virtual.

## Warna jadwal

Warna guru/mapel dihasilkan dengan penyebaran hue agar perbedaan visual lebih jelas dan mengurangi warna yang tampak sama.

## Project file

Ekstensi `.asccv` digunakan sebagai backup/transfer project. Project dimaksudkan bersifat mandiri dan menyimpan konteks yang diperlukan untuk melanjutkan pekerjaan tanpa bergantung pada lokasi file XML awal.

## Hari sekolah

Aplikasi memakai pemetaan umum hari 0–6:

```text
0 Senin
1 Selasa
2 Rabu
3 Kamis
4 Jumat
5 Sabtu
6 Minggu
```

Pilihan hari untuk Istirahat, Kegiatan Manual, dan JP Tambahan harus mengikuti hari aktif yang terdeteksi dari XML bila data tersedia.

## Branding

Nama produk resmi: **ASC Converter by Toto Gutomo**.

Footer ringkas menggunakan nama pengembang tanpa deretan gelar; informasi akademik lengkap ditempatkan pada About.
