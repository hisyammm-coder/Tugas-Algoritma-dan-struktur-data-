# Algoritma Pendaftaran dan Otentikasi Pengguna Baru di Aplikasi

**Mulai**

1. Tampilkan antarmuka pendaftaran akun baru.
2. Minta pengguna memasukkan `email` dam `password`. 
3. Periksa format `email` serta panjang `password` (minimal 8 karakter)
4. **jika** format `email` atau `password` tidak sesuai, **maka**:
- Tampilkan notifikasi "Format email atau password salah".
- Kembali ke langkah 3
5. **jika** format valid, **maka**:
- Buat 6 digit kode OTP secara acak.
- Kirim kode OTP ke `email` pengguna.
- Set batas percobaan input OTP = 3 kali.
6. Tampilkan layar verifikasi OTP dan minta pengguna memasukkan `kode_OTP_input`
7. **selama** sisa percobaan > 0:
- **jika** `kode_OTP_input` sama dengan kode OTP yang dikirim:
