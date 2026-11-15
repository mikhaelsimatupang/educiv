# Website EDUCIV

Website statis (HTML, CSS, JavaScript) tanpa proses build. Semua yang perlu diubah ada di bagian `EDIT DI SINI` pada `index.html`.

## Isi folder

- `index.html`: seluruh situs (beranda, artikel, tentang, tim, materi, kontak).
- `assets/educiv-wordmark.png` dan `assets/educiv-wordmark-dark.png`: logo teks untuk mode terang dan mode gelap.
- `assets/educiv-emblem-light.png` dan `assets/educiv-emblem-dark.png`: lambang kaca pembesar bergerak di beranda (latar transparan, versi terang dan gelap).
- `assets/educiv-emblem.png`: lambang untuk pratinjau saat tautan dibagikan.
- `assets/favicon.png`: ikon tab browser.
- `assets/team/`: foto anggota tim.

## Gerakan lambang

Lambang di beranda bergerak pelan (mengayun, berpendar, dan disapu kilap). Gerakan otomatis mati di perangkat yang meminta animasi dikurangi. Untuk mematikannya sendiri, hapus aturan `animation` pada `.emblem-enter`, `.emblem-sway`, dan `.emblem-sway img` di `index.html`.

## Warna identitas

- Biru EDUCIV: `#004AAD`
- Abu arang EDUCIV: `#444444`

## Pasang online lewat GitHub Pages

1. Masuk ke github.com, klik **New repository**. Beri nama, misalnya `educiv`, pilih **Public**, lalu **Create repository**.
2. Di halaman repositori yang masih kosong, klik **uploading an existing file**.
3. Buka folder `educiv-website` di komputer, pilih **isinya** (`index.html`, `README.md`, dan folder `assets`), lalu seret ke halaman GitHub. Jangan seret folder induknya, karena `index.html` harus berada di lapisan paling atas repositori.
4. Tunggu unggahan selesai, lalu klik **Commit changes**.
5. Buka **Settings → Pages**. Pada **Build and deployment**, pilih **Deploy from a branch**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
6. Tunggu 1 sampai 3 menit. Alamat situs akan muncul di halaman yang sama, berbentuk `https://NAMA-GITHUB.github.io/educiv/`.

Untuk memperbarui situs, buka file di repositori, klik ikon pensil, ubah, lalu **Commit changes**. Perubahan tampil online dalam beberapa menit.

## Cara menambah artikel

Salin satu blok artikel di `ARTICLES`, tempel di paling atas daftar, lalu ubah isinya.

```js
{
  slug: 'judul-singkat-tanpa-spasi',   // huruf kecil, angka, tanda hubung
  title: 'Judul Artikel',
  category: 'Struktur',                 // kategori baru otomatis muncul sebagai filter
  date: '2026-12-01',                   // format TAHUN-BULAN-TANGGAL
  minutes: 5,
  author: 'Nama Penulis',
  summary: 'Ringkasan satu sampai dua kalimat untuk kartu artikel.',
  body: [
    { t: 'p',  x: 'Paragraf pembuka.' },
    { t: 'h2', x: 'Subjudul' },
    { t: 'ul', items: ['Butir pertama', 'Butir kedua'] }
  ]
}
```

Tautan langsung ke sebuah artikel berbentuk `alamatsitus/#a-judul-singkat-tanpa-spasi`.

## Catatan

- Tiga artikel yang ada ditandai `sample: true` dan tampil dengan label "Artikel contoh". Ganti dengan tulisan tim, atau hapus baris `sample: true` setelah isinya disetujui.
- Email belum ditampilkan. Isi `SITE.email` bila ingin dimunculkan di bagian Kontak.
- Font dimuat dari Google Fonts. Tanpa internet, situs memakai font bawaan perangkat.
- Layanan konsultasi belum ditawarkan di situs ini. Bagian "Arah ke depan" menyebutnya sebagai rencana.
