# Testing & Release Checklist

## Import dan parser

- [ ] XML dapat diimpor
- [ ] Hari terdeteksi benar
- [ ] Period/JP terdeteksi benar
- [ ] Guru, kelas, dan mata pelajaran terbaca benar
- [ ] Reload/import ulang tidak merusak state

## Tampilan

- [ ] Dashboard benar
- [ ] Jadwal Induk benar
- [ ] Jadwal Guru benar
- [ ] Jadwal Kelas benar
- [ ] Beban Mengajar benar
- [ ] Dark / Light mode
- [ ] ID / EN mode

## Input mobile/tablet

- [ ] Keyboard tidak tertutup setelah satu karakter pada Waktu Manual
- [ ] Keyboard stabil pada Istirahat
- [ ] Keyboard stabil pada Kegiatan Manual
- [ ] Validasi hanya muncul ketika Save ditekan

## Timeline

- [ ] Istirahat menggeser jadwal bila disisipkan
- [ ] Kegiatan `Catatan saja` tidak menggeser jadwal
- [ ] Kegiatan sebelum JP 1 dihitung ke arah waktu sebelum JP 1
- [ ] Kegiatan khusus kelas tidak menggeser kelas lain
- [ ] Kegiatan paralel pada waktu identik tampil sejajar
- [ ] JP Tambahan muncul setelah JP terakhir

## Editor Jadwal Induk

- [ ] Ikon pensil membuka editor
- [ ] Slot kosong dapat diisi
- [ ] Slot dapat dikosongkan
- [ ] Slot dapat di-reset ke data ASC
- [ ] Jadwal Guru/Kelas ikut sinkron

## Project

- [ ] Save `.asccv`
- [ ] Open `.asccv`
- [ ] Project terakhir dapat dibuka
- [ ] Data pengaturan ikut pulih
- [ ] Edit manual ikut pulih

## Export

- [ ] Excel Indonesia
- [ ] Excel English
- [ ] PNG Jadwal Guru
- [ ] PNG Jadwal Kelas
- [ ] PNG Beban Mengajar jika diaktifkan
- [ ] Jadwal Induk tidak menawarkan PNG
- [ ] Prompt Builder tidak menawarkan Master Schedule sebagai PNG

## Release

- [ ] Nama aplikasi konsisten
- [ ] V2.5 Build 27.2.9 konsisten
- [ ] About benar
- [ ] Copyright benar
- [ ] Tidak ada error JavaScript pada startup
- [ ] Uji Android tablet
- [ ] Uji desktop/laptop Windows
