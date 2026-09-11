# BAGIAN A: Algoritma Pendaftaran dan Otentikasi Pengguna Baru di Aplikasi

1. **Mulai**
2. Tekan pilihan pendaftaran akun baru.
3. masukkan `email` dam `password`. 
4. Periksa `email` dan panjang `password` (minimal 8 karakter)
5. **kalau** format `email` atau `password` tidak sesuai, **maka**:
- Muncul tampilan notifikasi "format email atau password salah".
- Kembali ke langkah 3
6. **kalau** format benar, **maka**:
- Muncul Tampilan 6 digit kode OTP secara acak.
- Kirim kode OTP ke `email`.
- batas percobaan input OTP = 3 kali.
7. verifikasi OTP dan masukkan kode OTP
8. **selama** sisa percobaan > 0:
- **jika** kode OTP sama dengan kode OTP yang dikirim:
- Muncul tampilan notifikasi "pembuatan akun berhasil".
- Lanjut ke langkah 9 (selesai)
9. **Selesai**

  #### pemenuhan 5 Karakteristik Utama Algoritma:
  - **Input:** Data `email`, `password`, dan Kode OTP yang dimasukkan.
  - **Output:** Notifikasi akun berhasil dibuat (serta data tersimpan) atau pesan pendaftaran gagal.
  - **Definiteness:** Validasi email secara rinci, serta pengecekan OTP dengan kesamaan karakter OTP yang dikirim.
  - **Finiteness:** Algoritma memiliki titik henti yang jelas, yaitu saat pendaftaran sukses atau saat sisa percobaan OTP habis.
  - **Efectiveness:** Langkah-Langkahnya logis dan dapat dijalankan oleh sistem tanpa kendala yang serius.

  # BAGIAN B: Analisis Pemilihan Struktur Data
  #### 1. Skenario 1 (Fitur undo / Redo pada text editor)
  ##### sebuah aplikasi pengolah kata (Text Editor) Membutuhkan fitur untuk membatalkan ketikan terakhhir pengguna (Undo) dan mengembalikannya lagi (Redo)
- Struktur data terpilih: Stack 
- Alasan: Berdasarkan yang saya baca pada artikel <https://ids.ac.id/struktur-data-stack-dalam-pembangunan-perangkat-lunak/>, menurut saya stack cocok untuk fitur undo/redo ini karna cara kerja stack adalah elemen yang saya masukkan terakhir adalah yang pertama dikeluarkan, jadi segala suatu perubahan dapat disimpan pada stack, dan perubahan terakhir dapat di undo.

#### 2. Skenario 2 (Peta Navigasi Rute Perjalanan)
##### Sebuah aplikasi GPS membutuhkan cara untuk memodelkan lokasi-lokasi kota beserta jalan penghubungnya guna mencari rute tercepat.
- Struktur data terpilih: Graph
- Alasan: Berdasarkan yang saya baca pada artikel <https://journal.arimsi.or.id/index.php/Algoritma/article/download/923/922/4973>, menurut saya cara kerja stack yang berurutan dan saling berhubungan dalam suatu arah, sangat cocok untuk ini karena peta navigasi rute perjalanan pun saling terhubung antara satu sama lain,sehingga dapat menghubungkan dari satu titik ke titik lainnya dengan mudah.

#### 3. Skenario 3 (Sistem login pengguna berbasis username)
##### Sistem butuh mencari data akun dari jutaan user secara instan berdasarkan Username saat proses login.
- Struktur data terpilih: Hash table
- karna cara kerja hash table yang meenyimpan serta mengambil data secara efisien, yaitu seperti kunci hotel yang sudah di simpan dan dapat diambil dengan sangat mudah dan efisien, maka hash table cocok untuk skenario ini, karna sistem dapat mengelompokkan dan menemukan data akun dalam pencarian dengan sangat mudah.

  # Bagian C: Eksplorasi analogi mandiri
  
- Struktur data dipilih: Hash Table
- Nama Analogi: Kartu nomor berbahan kertas penyitaan barang terlarang yang dibawa pada suatu event turnament futsal.
- Cara Kerja: Pada saat ada barang sitaan, Petugas menandai barang tersebut dengan nomor, dan nomor tersebut diberikan kepada pelanggar, dan ketika pelanggar ingin mengambilnya kembali pada saat event telah selesai, pelanggar memberikan nomor yang diberikan di awal kepada petugas, dan petugas mengambil barang tersebut dengan nomor yang sudah ditandai pada saat awal penyitaan.
- Mencerminkan kekurangan / kelebihan: Kelebihannya, yaitu Proses pencarian barang yang mudah, karena lewat nomor yang diberikan oleh pelanggar kepada petugas. Kekurangannya, Jika Nomor yang diberikan kepada pelanggar hilang, atau rusak, petugas sulit untuk menemukan barang yang ingin diambil oleh pelanggar.
