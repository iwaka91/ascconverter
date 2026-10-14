# Changelog ASC Converter

Dokumen ini merangkum milestone pengembangan utama.

## V2.5 Build 27.2.9 — Current Source

- Export Excel bilingual Indonesia / English
- Export PNG terintegrasi untuk tampilan yang sesuai
- PNG Jadwal Induk dihapus karena kepadatan data terlalu tinggi
- Prompt Builder memakai alur PNG-only untuk image generator eksternal
- Editor Jadwal Induk berbasis ikon pensil
- Lapisan edit manual tanpa memodifikasi raw XML
- JP Tambahan setelah JP terakhir per hari
- Perbaikan timeline kegiatan paralel antar kelas
- Kegiatan `Catatan saja` tidak menggeser timeline
- Kegiatan `Sisipkan ke jadwal` mengikuti timeline
- Penyempurnaan bilingual UI

## Build 27.2.8 — Manual Time Input Fix

- Perbaikan keyboard virtual pada input waktu manual
- Mengurangi render ulang saat pengguna sedang mengetik pada Android/tablet

## Build 27.2.7 — Branding Identity Patch

- Branding resmi: **ASC Converter by Toto Gutomo**
- Identitas About dan copyright diperbarui
- Footer aplikasi disederhanakan

## Build 27.2.6 — Schedule Timeline & Language Fix

- Perbaikan nama hari bilingual pada jadwal
- Pilihan hari mengikuti hari aktif dari XML
- Perbaikan posisi kegiatan sebelum JP 1
- Mode catatan tidak mengubah timeline
- Prompt Builder menggunakan istilah English yang konsisten

## Build 27.2.5 — Mobile Input & Language UX Fix

- Perbaikan keyboard virtual untuk input Istirahat dan Kegiatan Manual
- Validasi form hanya muncul saat tindakan Simpan
- Toggle cepat `ID / EN` pada header

## Build 27.2.4 — Project & Schedule Micro Polish

- Penyederhanaan Riwayat Proyek
- Informasi hari pada kartu kegiatan/istirahat
- Penyempurnaan warna otomatis guru
- Perbaikan teks English pada Teacher List / Teacher Schedule
- Nama guru pada Jadwal Induk tidak lagi menjadi tautan navigasi

## Build 27.2.3 — Project Menu UX Polish

- Menu Proyek dipindahkan dari header ke sidebar
- Halaman Proyek khusus
- Header dibuat lebih bersih

## Build 27.2.x — Language System

- Fondasi bilingual Indonesia / English
- Penerjemahan UI statis dan dinamis
- Deep Language Render Fix
- About, Settings, Dashboard, Project, Prompt Builder, toast, dan form diperluas cakupan terjemahannya

## Build 27.1.x — Stability, Timeline & Project Polish

- Penguatan save/load project `.asccv`
- Riwayat proyek
- Timeline dinamis
- Istirahat dan kegiatan manual
- Dashboard compact summary

## Versi 1.x

Tahap awal mencakup parser XML aSc Timetables, Jadwal Induk, Jadwal Guru, Jadwal Kelas, export Excel, dan penyempurnaan kompatibilitas parser/layout.

Parser stabil dari fase awal dipertahankan sebagai fondasi dan sebisa mungkin tidak disentuh pada patch UI/UX berikutnya.
