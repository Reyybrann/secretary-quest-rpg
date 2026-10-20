# PANDUAN GURU — SECRETARY QUEST RPG

## Sasaran
Siswa SMP kelas 7–9 yang belajar literasi keuangan, aritmetika sosial, dan pengenalan mata pelajaran Akuntansi di SMK.

## Rencana 1 pertemuan (40 menit)

1. **5 menit:** pengantar tujuan dan pembagian perangkat.
2. **5 menit:** pembuatan karakter dan tutorial narator.
3. **20 menit:** bermain secara mandiri, menuntaskan monster/level sebanyak mungkin.
4. **5 menit:** meminta siswa menjelaskan contoh kas masuk/keluar dan laba-rugi dari soal yang telah dijawab.
5. **5 menit:** refleksi: apa yang membuat suatu usaha memperoleh laba atau mengalami rugi?

## Materi per wilayah

| Area | Level | Materi |
|---|---:|---|
| Desa Akuntansi | 1–4 | Kalkulator, nota, kas, stok, kasir, kas masuk dan kas keluar |
| Hutan Pengetahuan | 5–8 | Harga beli-jual, omzet, laba, buku kas, modal, beban |
| Gua Kristal | 9–12 | Kembalian, diskon, arsip, stok, beban dan rugi |
| Menara Neraca | 13–16 | Aset, kewajiban, laporan, perhitungan saldo dan laba kotor |
| Kastil Akhir | 17–20 | Pengambilan keputusan, pencatatan jujur, keuntungan, persediaan |

## Catatan pedagogis

- Isi game adalah pengenalan konsep, belum pembukuan akuntansi tingkat lanjut.
- Jawaban yang salah mengurangi HP tetapi soal dapat dicoba ulang dengan petunjuk; tidak ada pemaksaan pembelian.
- Skins pedang tidak memengaruhi benar-salah jawaban. Semua penghargaan menggunakan koin fiktif.
- Tidak ada login, fitur chatting, iklan, pembayaran, atau koneksi antarsiswa.
- Guru perlu menjelaskan bahwa *laba* dan *saldo kas* bukan angka yang sama; contoh soal sudah membedakannya.
- Nilai kinerja bisa dinilai berdasarkan jumlah monster dikalahkan, jawaban benar dan penjelasan siswa di sesi refleksi, bukan semata koin yang dimiliki.

## Modifikasi soal

Buka `src/questions.js`. Setiap objek memiliki `q` pertanyaan, `a` tiga pasangan `[ikon, label]`, `c` indeks jawaban benar (0/1/2 sebelum diacak di layar), `h` petunjuk, dan `e` penjelasan. Periksa perhitungan sebelum menerbitkan perubahan. Jumlah soal disetel 40 untuk 20 level.
