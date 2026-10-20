# SECRETARY QUEST RPG — LEGENDA KOIN

Game petualangan top-down 2D untuk pengenalan akuntansi bagi siswa SMP. Game ini bekerja secara **single-player** menggunakan HTML, CSS, JavaScript dan HTML Canvas. **Tidak memerlukan npm, SQL, backend, framework CDN, atau akun game.** Semua berkas disertakan.

## Yang tersedia dalam game

- Pembuatan karakter: perempuan/laki-laki, nama, gaya rambut, warna rambut, warna kulit, pakaian.
- Tutorial 5 bagian dipandu avatar narator dengan wajah jelas yang diadaptasi dari referensi pengguna.
- Lima wilayah: Desa Akuntansi, Hutan Pengetahuan, Gua Kristal, Menara Neraca, Kastil Akhir.
- 20 level, 20 monster (termasuk bos), 40 soal akuntansi pilihan gambar.
- Pertarungan otomatis setelah jawaban benar, dengan 5 variasi animasi dipilih acak.
- XP, HP, koin, toko pedang (8 skin), guild/markas yang bisa di-upgrade.
- Papan quest, NPC, arsip progres, kemenangan setelah level 20.
- Kontrol WASD dan E/Spasi di PC; joystick dan tombol interaksi/serang di HP.
- Percobaan fullscreen + kunci landscape; jika browser tidak mengizinkan, game berusaha memutar tampilan secara visual. Browser memiliki kontrol akhir atas orientasi fisik layar.
- Progres tersimpan otomatis di localStorage browser. TIDAK sinkron lintas HP/PC.

## Cara paling mudah mengunggah ke GitHub Pages

1. Ekstrak berkas ZIP yang kamu unduh. **JANGAN** mengunggah ZIP mentah ke GitHub Pages.
2. Di GitHub, buat repository baru bernama misalnya `secretary-quest-rpg`, pilih **Public**.
3. Unggah **seluruh isi folder `ACCOUNTING_LEGENDS_WEB`** ke root repository, bukan folder luarnya sebagai subfolder. Struktur di root harus seperti berikut:

```
secretary-quest-rpg/
  index.html
  README_MULAI_DISINI.md
  assets/
    icon.svg
    narator_rambut.webp
    narator_hijab.webp
    splash.webp
  src/
    art.js
    game.js
    questions.js
    style.css
```

4. **Pastikan folder `assets` dan `src` terlihat sebagai folder terpisah** di GitHub dan masing-masing masih berisi file. Kalau drag-and-drop GitHub melalui browser meratakan foldernya, gunakan aplikasi gratis **GitHub Desktop**: pilih File → Add Local Repository/Clone repository, copy semua isi proyek ke folder clone, klik Commit to main → Push origin. Proses ini mempertahankan struktur direktori.
5. Repository → **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main → Folder: /(root) → Save**.
6. Tunggu deploy selesai. URL akan berbentuk `https://USERNAME.github.io/secretary-quest-rpg/` (ganti USERNAME dengan username GitHub milikmu).
7. Buka URL di laptop dan HP untuk tes.

## Alternatif upload yang lebih sederhana

Buka https://app.netlify.com/drop, login dengan akun gratis, lalu seret **folder proyek yang sudah diekstrak** ke halaman Netlify Drop. Kamu memperoleh alamat situs publik. Tidak perlu Git/GitHub untuk publish sederhana.

## Mencoba di laptop tanpa mengunggah

Bisa membuka `index.html` langsung, namun cara paling konsisten adalah melalui server lokal (misalnya ekstensi Live Server di VS Code). Alternatif:

```
cd ACCOUNTING_LEGENDS_WEB
python -m http.server 8080
```

Buka http://localhost:8080 di Chrome/Edge.

## Cara main

- Di komputer gunakan **WASD** untuk berjalan, **E** berbicara/interaksi, **SPASI** memulai pertarungan. Pakai mouse untuk memilih jawaban di layar.
- Di HP gunakan analog kiri, tombol 💬 untuk interaksi, tombol ⚔️ untuk menyerang. Saat pertama menekan Mulai, browser dapat meminta izin fullscreen.
- Datangi monster di jalan utama (jarak cukup dekat), serang, dan pilih ilustrasi jawaban yang benar. Setelah dua atau tiga serangan yang berhasil, monster dikalahkan dan hadiah diberikan.
- Gunakan tombol **Toko** untuk membeli skin pedang; gunakan **Guild** untuk mengembangkan bangunan dan meningkatkan bonus koin setiap monster.
- Selesaikan 4 level per wilayah, total 20 level hingga kastil.

## Masalah yang sering muncul

**Game 404 setelah publish?** Periksa `index.html` ada di root (bukan di dalam subfolder tambahan) dan GitHub Pages disetel `main /(root)`.

**Latar, narator, atau game kosong?** Pastikan `assets` dan `src` terunggah. Nama file dan kapitalisasi sama persis. Periksa browser DevTools → Console untuk error 404.

**Joystick tidak bergerak?** Pastikan membuka game di browser HP sungguhan dengan layar sentuh, bukan mode desktop. Sentuh dan geser area analog di kiri bawah; gunakan browser Chrome versi baru atau Safari terbaru.

**Rotasi layar tidak terjadi?** Sebagian browser, khususnya Safari iOS, menolak `screen.orientation.lock()`. Game mencoba fallback CSS yang memutar isi game. Jika tampilannya tidak nyaman, aktifkan rotasi otomatis perangkat dan pegang HP dalam posisi landscape.

**Progres hilang?** Mode samaran/incognito, pindah browser, hapus data situs atau aplikasi pembersih dapat menghapus localStorage. Siswa sebaiknya memakai satu perangkat dan browser selama satu sesi.

**Game lambat di HP?** Tutup tab lain, gunakan browser terbaru, matikan penghemat daya jika perlu. Grafik dibuat dengan Canvas 2D ringan, tanpa file model 3D.

## Privasi, materi pembelajaran, dan aset

- Game tidak mengirimkan nama karakter, jawaban, atau progres ke server pihak ketiga; semuanya lokal dalam browser.
- Jawaban soal ada di `src/questions.js`. Terdapat 40 soal, dua per level secara umum (level bos memerlukan satu soal pengulangan tambahan). Angka dan rumus disederhanakan untuk tingkat SMP.
- Ilustrasi lokasi, monster, karakter dibuat secara prosedural lewat Canvas 2D; tanpa dependensi gambar eksternal pada runtime.
- Dua portrait narator merupakan ilustrasi dari foto referensi yang diberikan dalam percakapan. **Pastikan memperoleh izin orang yang ada dalam foto sebelum menggunakan wajahnya di website publik.** Jika tidak, ganti dengan ilustrasi/karakter fiktif.
- Bila ingin memakai berkas di kelas, guru dapat menambahkan materi tanpa perlu memodifikasi engine. Ada juga panduan `PANDUAN_GURU.md`.

Versi 1.0 · Ditujukan untuk permainan mandiri; bukan game daring multiplayer.
