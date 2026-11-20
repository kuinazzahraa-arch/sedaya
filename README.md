# SEDAYA — Setara dan Berdaya

Prototipe web responsif untuk membantu perempuan berusia 40 tahun ke atas menemukan peluang kerja berdasarkan keterampilan, pengalaman, dan preferensi kerja.

## Fitur

- Pilihan peran: mencari kerja atau membuka lowongan, dengan navigasi dan onboarding terpisah.
- Onboarding pencari kerja: identitas, usia, domisili bebas, unggah foto, keterampilan, dan preferensi kerja.
- Beranda dengan pencocokan berdasarkan kata kunci profil dan domisili.
- 16 contoh lowongan, pencarian, filter jenis/lokasi/waktu kerja, serta simpan lowongan.
- Katalog program mitra dan simulasi hasil sertifikasi.
- Pelacakan lamaran sampai tahap penawaran.
- Komunitas dengan unggahan, reaksi, dan laporan.
- Profil profesional dan unduhan draf CV dalam format teks.
- Alur pemberi kerja: identitas usaha, pengajuan lowongan, pemeriksaan kelengkapan, kandidat, jadwal seleksi, penawaran, dan hasil rekrutmen.

## Menjalankan secara lokal

Tidak memerlukan instalasi dependensi atau proses build. Dengan Python 3 terpasang, jalankan dari folder proyek:

```sh
python3 -m http.server 8000
```

Buka `http://localhost:8000` di browser.

## Struktur proyek

```text
index.html       Kerangka halaman
style.css        Tampilan responsif dan Poppins
app.js           Alur dasar dan penyimpanan lokal
experience.js    Onboarding, fotografi, katalog, dan penyempurnaan interaksi
roles.js         Peran pengguna, usia, dan alur rekrutmen pemberi kerja
assets/          Foto, logo, ikon referensi, font, dan lisensi font
.nojekyll        Menyajikan berkas statis di GitHub Pages
```

`experience.js` dimuat setelah `app.js` dan menyempurnakan fungsi dasarnya. `roles.js` dimuat terakhir. Pertahankan urutan ketiga skrip saat melakukan perubahan.

## Mengunggah ke GitHub

1. Buat repository baru, misalnya `sedaya-prototype`.
2. Unggah **isi folder ini**, bukan ZIP atau folder pembungkusnya. `index.html` harus berada di direktori utama repository.
3. Sertakan direktori `assets` beserta seluruh isinya.
4. Simpan perubahan pada branch `main`.

Alternatif melalui Git, setelah membuat repository kosong:

```sh
git init
git add .
git commit -m "Add SEDAYA interactive prototype"
git branch -M main
git remote add origin https://github.com/USERNAME/sedaya-prototype.git
git push -u origin main
```

Ganti `USERNAME` dengan akun GitHub pemilik repository. Jangan menaruh token akses di berkas proyek atau alamat remote.

## GitHub Pages

Proyek sudah disusun sebagai situs statis: gunakan branch `main` dan direktori root sebagai sumber GitHub Pages. Tidak membutuhkan workflow build. Alamat situs mengikuti nama akun dan repository yang digunakan. Seluruh rute memakai hash sehingga tetap bekerja saat halaman dimuat ulang.

## Batasan prototipe

Seluruh perusahaan, mitra, lowongan, hasil asesmen, dan proses rekrutmen merupakan demonstrasi. Tidak ada lamaran, laporan, atau pendaftaran yang dikirim ke pihak lain. Pencocokan menggunakan aturan sederhana, bukan layanan AI aktif. Tidak ada server, autentikasi pengguna, pembayaran, maupun sertifikasi resmi.

Data dan foto profil disimpan di `localStorage` pada browser yang digunakan. Gunakan data contoh saat demonstrasi. Untuk mengulang onboarding gunakan tombol di panel samping; untuk menghapus seluruh data demonstrasi, hapus data situs melalui pengaturan browser.

## Aset

Foto dan identitas visual berasal dari aset yang diberikan untuk proyek SEDAYA. Lisensi Poppins disertakan dalam `assets/OFL-Poppins.txt`. Paket ini tidak menetapkan lisensi terbuka untuk kode, foto, atau merek SEDAYA; pemilik proyek dapat menambahkan lisensi sesuai kebutuhan.

Pemeriksaan identitas di prototipe hanya memeriksa kelengkapan input dan nama berkas, bukan autentisitas dokumen. Status publikasi, kandidat, undangan, dan hasil rekrutmen berada di browser, tanpa pengiriman ke pihak luar. Penyajian UI disederhanakan untuk presentasi; batasan ini tetap berlaku.
