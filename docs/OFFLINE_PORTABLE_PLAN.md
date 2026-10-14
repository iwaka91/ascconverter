# Offline & Portable Plan

## Tujuan

Menyediakan ASC Converter yang dapat digunakan 100% offline untuk sekolah dengan koneksi terbatas.

## Rencana tahap

1. Audit semua dependency eksternal.
2. Lokalkan CSS, JS, icon/font, writer Excel, renderer PNG, dan chart.
3. Uji aplikasi dari folder lokal dengan internet dimatikan.
4. Uji fungsi utama: import XML, editor, timeline, save/open project, export Excel, export PNG, bilingual.
5. Jika paket offline stabil, bungkus sebagai aplikasi Windows portable.

## Kandidat wrapper desktop

- WebView2 wrapper
- Tauri
- Electron hanya jika diperlukan untuk kompatibilitas tertentu

Prioritas adalah paket ringan yang tidak mengubah logika aplikasi.

## Prinsip distribusi

Versi web tetap menjadi distribusi utama. Portable Offline Edition disediakan untuk kebutuhan sekolah yang benar-benar memerlukan operasi tanpa koneksi internet.

Wrapper EXE tidak dianggap sebagai perlindungan source absolut. Identitas resmi, copyright, domain, versioning, dan pencatatan HKI tetap menjadi bagian penting dari perlindungan karya.
