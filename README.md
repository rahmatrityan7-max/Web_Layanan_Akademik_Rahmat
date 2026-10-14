# Portal Layanan Akademik

Tugas Pertemuan 5 – Responsive & Accessible Web Client. Halaman statis (HTML + CSS, tanpa JavaScript).

## Struktur
```
index.html          Beranda (hero + tautan ke Layanan & Alur)
layanan.html        Daftar layanan (SAK/TRS/CTI/LGL)
alur.html           Alur pengajuan
permohonan.html     Formulir permohonan
kontak.html         Kontak bagian akademik
css/styles.css      (Bagian 1 di atas = pengaturan cepat: warna, huruf, ukuran)
img/logo.svg        (logo kampus, ganti dengan logo Anda)
img/hero.svg        (gambar Beranda, dekoratif, alt="")
PANDUAN-EDIT.md     (cara mengganti teks, gambar, dan tampilan)
evidence/           (taruh screenshot DevTools di sini)
evidence/CHECKLIST.md
```

## Keputusan desain
- **Konsep visual**: loket layanan kampus. Hero berupa tiket antrean bernomor 000 (pesan "tanpa antre"), layanan disusun sebagai papan daftar loket (kode SAK/TRS/CTI/LGL), alur pengajuan sebagai garis waktu. Palet: ultramarine, ink, mist, lime.
- **Semantik**: `header`, `nav`, `main`, `footer` di setiap halaman; satu `h1` per halaman → `h3` untuk judul layanan/langkah. Navigasi antarhalaman memakai tautan biasa, dan halaman aktif ditandai `aria-current="page"`.
- **Mobile-first**: CSS dasar satu kolom; `min-width` 40em (daftar layanan satu baris per layanan, field form 2 kolom) dan 64em (hero dan form 2 kolom, alur 4 kolom). Breakpoint dipilih saat konten mulai sempit/renggang, bukan nama perangkat.
- **Layout**: CSS Grid untuk hero, papan layanan, alur, form, dan footer; Flexbox untuk navigasi dan radio.
- **Form**: `label for` terasosiasi, `type="email"`, `pattern` pada NIM, `required`, `minlength`/`maxlength`, `fieldset`+`legend` untuk radio, tombol `<button type="submit">`. Teks bantuan dihubungkan dengan `aria-describedby`.
- **Aksesibilitas**: skip link, `:focus-visible` jelas (outline 3px), target sentuh min. 44px, kontras teks terendah 6,8:1 (AA ≥ 4,5:1), batas input 5,9:1 (≥ 3:1), `lang="id"`, elemen native lebih dulu daripada ARIA, `prefers-reduced-motion` dihormati.
- **Gambar**: `img/hero.svg` bersifat dekoratif (tidak menambah informasi di luar teks), karena itu `alt=""`.
- **Submit**: tanpa backend dan tanpa JS, form memakai `method="get" action="#form-permohonan"` sehingga hanya menguji validasi HTML bawaan browser.

## Cara menjalankan
Buka `index.html` di browser, atau `python3 -m http.server 8000` lalu buka `http://localhost:8000`.

## Bukti pengujian DevTools
Isi `evidence/CHECKLIST.md` dan simpan screenshot di folder `evidence/`.

## Pengumpulan
- URL aplikasi: _(isi, mis. GitHub Pages)_
- Repositori GitHub: _(isi)_
- Screenshot: folder `evidence/`
