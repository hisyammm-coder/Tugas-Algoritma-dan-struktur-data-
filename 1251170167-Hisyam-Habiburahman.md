# BAGIAN A: Algoritma Pendaftaran dan Otentikasi Pengguna Baru di Aplikasi

1. **Mulai**
2. Tampilkan antarmuka pendaftaran akun baru.
3. memasukkan `email` dam `password`. 
4. Periksa format `email` serta panjang `password` (minimal 8 karakter)
5. **jika** format `email` atau `password` tidak sesuai, **maka**:
- Muncul tampilan notifikasi "Format email atau password salah".
- Kembali ke langkah 3
6. **jika** format benar, **maka**:
- Muncul Tampilan 6 digit kode OTP secara acak.
- Kirim kode OTP ke `email`.
- batas percobaan input OTP = 3 kali.
7. verifikasi OTP dan masukkan `kode_OTP_input`
8. **selama** sisa percobaan > 0:
- **jika** `kode_OTP_input` sama dengan kode OTP yang dikirim:
- Muncul tampilan notifikasi "pembuatan akun berhasil".
- Lanjut ke langkah 9 (selesai)
9. **Selesai**

  #### pemenuhan 5 Karakteristik Utama Algoritma:
  - **Input:** Data `email`, `password`, dan `kode_OTP_input` yang dimasukkan.
  - **Output:** Notifikasi akun berhasil dibuat (serta data tersimpan) atau pesan kegagalan pendaftaran.
  - **Definiteness:** Validasi email secara rinci mengecek simbol `@`dan `.`, serta pengecekan OTP dengan kesamaan karakter.
  - **Finiteness:** Algoritma memiliki titik henti yang jelas, yaitu saat pendaftaran sukses atau saat sisa percobaan OTP (3kali) habis.
  - **Efectiveness:** Langkah-Langkahnya logis dan dapat dijalankan oleh sistem tanpa kendala yang serius

  # BAGIAN B: Analisis Pemilihan Struktur Data
  #### 1. Skenario 1 (Fitur undo / Redo pada text editor)
