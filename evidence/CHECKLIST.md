# Bukti Pemeriksaan Browser DevTools

Lakukan sendiri di browser (Chrome/Edge/Firefox, tekan F12), lalu simpan screenshot dengan nama yang tertera dan isi kolom Temuan.

| # | Pemeriksaan | Cara | Screenshot | Temuan (isi) |
|---|-------------|------|------------|--------------|
| 1 | Elements/Inspector: struktur landmark & heading | Tab Elements, buka `header/nav/main/footer` | `01-elements.png` | |
| 2 | CSS: box model, Grid/Flex | Pilih `.card-grid`, lihat badge grid & panel Computed | `02-css-grid.png` | |
| 3 | Responsive 360 px | Ctrl+Shift+M, lebar 360 | `03-360.png` | Ada horizontal scroll? Ya/Tidak |
| 4 | Responsive 768 px | lebar 768 | `04-768.png` | Ada horizontal scroll? Ya/Tidak |
| 5 | Responsive 1280 px | lebar 1280 | `05-1280.png` | Ada horizontal scroll? Ya/Tidak |
| 6 | Network: reload (Ctrl+R) | Tab Network, centang Disable cache | `06-network.png` | Jumlah request, status semua 200? Resource gagal? |
| 7 | Accessibility tree / Inspector | Tab Accessibility (Firefox) atau Elements → Accessibility (Chrome) | `07-a11y.png` | Role & nama kontrol form benar? |
| 8 | Keyboard & focus | Tekan Tab dari awal halaman | `08-focus.png` | Semua kontrol terjangkau? Fokus terlihat? |
| 9 | Validasi form | Kirim kosong; isi email `abc` | `09-validasi.png` | Pesan error muncul? |
| 10 | Lighthouse Accessibility (opsional) | Tab Lighthouse | `10-lighthouse.png` | Skor |

## Catatan debugging / keputusan
- (tuliskan masalah yang ditemukan dan cara memperbaikinya, 2–5 kalimat)
