# Secretary Quest RPG 3D V3 — FIX `con is not defined`

Tanggal: 21 Oktober 2026

## Penyebab
`src/world.js`, fungsi `fence()`, memanggil `con(...)` tetapi fungsi yang tersedia di modul peta adalah `cone(...)`. Pagar desa dibuat setiap kali peta `village` dibangun sehingga initialization terhenti dengan `ReferenceError: con is not defined`.

## Yang diperbaiki
Mengganti satu panggilan `con(p,.14,.25,0xf7db99,a,1.05,b,4)` menjadi `cone(p,.14,.25,0xf7db99,a,1.05,b,4)`.
Versi `standalone/index.html` dibangun ulang menggunakan `tools/build_standalone.py` agar perbaikan masuk ke file tunggal untuk GitHub Pages.

## Tes
- Memeriksa sintaks JavaScript.
- 18 tes logika lama.
- 8 tes runtime simulasi map, Guild, karakter, dan monster tambahan.
- Batasan: rendering Three.js/WebGL di perangkat nyata masih perlu diuji setelah deploy; pengujian lokal ini tidak memverifikasi hasil visual dan kontrol sentuh.

## Cara memasang
Upload hanya file `index.html` dari ZIP versi satu-file ke root repository `secretary-quest-rpg`, menggantikan file lama, kemudian tunggu GitHub Pages deployment dan reload paksa `Ctrl+Shift+R`.
Progress `localStorage` tetap menggunakan versi save yang sama; jangan tekan reset progres.
