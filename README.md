# ASC Converter by Toto Gutomo

ASC Converter adalah aplikasi berbasis HTML/JavaScript untuk membaca file XML hasil aSc Timetables, menyajikannya kembali sebagai jadwal sekolah yang lebih mudah digunakan, melakukan penyesuaian pascaproses, lalu mengekspor hasil ke Excel dan PNG.

## Status

- **Versi aplikasi:** V2.5
- **Build:** 27.2.9
- **Status:** public release / active development
- **Bahasa UI:** Indonesia & English
- **Platform utama:** browser modern pada tablet Android, desktop, dan laptop
- **Pengembang:** Toto Gutomo

## Fitur utama

- Import XML aSc Timetables
- Dashboard statistik jadwal
- Jadwal Induk / Master Schedule
- Jadwal Guru / Teacher Schedule
- Jadwal Kelas / Class Schedule
- Rekap Beban Mengajar / Teaching Load
- Pengaturan waktu manual
- Istirahat dan kegiatan sekolah
- JP tambahan setelah JP terakhir pada hari tertentu
- Editor Jadwal Induk berbasis ikon pensil
- Penyimpanan dan pembukaan proyek `.asccv`
- Bahasa Indonesia / English
- Dark / Light mode
- Export Excel bilingual
- Export PNG untuk jadwal yang sesuai
- Prompt Builder untuk peningkatan visual PNG melalui image generator eksternal

## Struktur repository

```text
/
├── README.md
├── CHANGELOG.md
├── docs/
│   ├── ARCHITECTURE.md
│   ├── DEVELOPMENT_NOTES.md
│   ├── TESTING_AND_RELEASE.md
│   └── OFFLINE_PORTABLE_PLAN.md
├── src/
│   └── ASC_Converter_V2.5_Build_27.2.9.html
└── site/
    └── landing-page.html
```

## Cara menjalankan source

Buka file:

```text
src/ASC_Converter_V2.5_Build_27.2.9.html
```

## Prinsip data

ASC Converter dirancang agar data XML asli tetap menjadi sumber dasar. Perubahan lanjutan seperti kegiatan manual, JP tambahan, dan edit slot jadwal disimpan sebagai lapisan pascaproses dan tidak dimaksudkan untuk mengubah file XML asli.

## Offline / Portable

Eksperimen versi offline/portable sedang dilakukan. Rencana teknisnya didokumentasikan di `docs/OFFLINE_PORTABLE_PLAN.md`.

## Hak cipta

© 2026 Toto Gutomo. Hak Cipta Dilindungi.

Repository ini dipublikasikan untuk dokumentasi, portofolio, transparansi pengembangan, dan pengarsipan source. Belum ada lisensi open-source terpisah yang diberikan melalui repository ini.
