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
- Struktur data terpilih:
- Alasaan: 
