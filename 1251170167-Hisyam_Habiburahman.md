# A. ANALISIS KOMPONEN

### 1. Identifikasi Variabel dan Tipe Data
- `is_member` : **Boolean** (status keanggotaan pelanggan: `True` untuk member, `False` untuk non-member)
- `jumlah_buku` : **Integer** (jumlah buku yang dibeli)
- `total_awal` : **Real** (total nominal belanja sebelum diskon)
- `persen_diskon` : **Real** (persentase diskon yang didapat)
- `nominal_diskon` : **Real** (besarnya nominal potongan harga)
- `total_bayar` : **Real** (total pembayaran akhir setelah diskon)

### 2. Jenis Struktur Kontrol yang Digunakan
- **Iteration :**
  Menggunakan `REPEAT ... UNTIL` untuk memvalidasi input agar `total_awal >= 0` AND `jumlah_buku >= 1`.
- **Selection:**
  Menggunakan `IF ... ELSE` untuk menentukan diskon berdasarkan `is_member`, `total_awal`, dan `jumlah_buku`.
- **Sequence:**
  Alur proses berurutan: Input -> Validasi -> Hitung Diskon -> Hitung Total Bayar -> Output.

  # B. PENYUSUNAN PSEUDOCODE 

```

PROGRAM SistemTransaksiTokoBuku

DEKLARASI:
    is_member      : boolean
    jumlah_buku    : integer
    total_awal     : real
    persen_diskon  : real
    nominal_diskon : real
    total_bayar    : real

DESKRIPSI:
1. Validasi Input Data
    REPEAT
        OUTPUT "Masukkan status member (true/false): 
        INPUT is_member
        OUTPUT "Masukkan total belanja awal: 
        INPUT total_awal
        OUTPUT "Masukkan jumlah buku: 
        INPUT jumlah_buku

        IF (total_awal < 0 OR jumlah_buku < 1) THEN
            OUTPUT "Input tidak valid! total_awal harus >= 0 dan jumlah_buku harus >= 1."
        ENDIF
    UNTIL (total_awal >= 0 AND jumlah_buku >= 1)

2. Logika Perhitungan Diskon
    IF (is_member = true) THEN
        IF (total_awal >= 200000 AND jumlah_buku >= 3) THEN
            persen_diskon <- 0.15
        ELSE
            persen_diskon <- 0.10
        ENDIF
    ELSE
        IF (total_awal >= 300000) THEN
            persen_diskon <- 0.05
        ELSE
            persen_diskon <- 0.00
        ENDIF
    ENDIF

3. Perhitungan Nominal Diskon dan Total Bayar
    nominal_diskon,total_awaal,persen_diskon
    total_bayar,total_awal,nominal_diskon

4. Output Data

    OUTPUT "Nominal Diskon: nominal_diskon
    OUTPUT "Total Bayar   : total_bayar

```

# C. Uji Logika

**Kasus A**

input: `is_member = true`, `total_awal = 250000`, `jumlah_buku = 4`

| total_awal | jumlah_buku | is_member | nominal_diskon | total_bayar | 
| --- |---|---|---|---| 
| 250000 | 4 | true | 0 | 0 | 
| 250000 | 4 | true | 0 | 0 | 
| 250000 | 4 | true | 37500 | 212500 | 
| 250000 | 4 | true | 37500 | 212500 | 

**Kasus B**

input: `is_member = false`, `total_awal = 350000`, `jumlah_buku = 2`

| total_awal | jumlah_buku | is_member | nominal_diskon | total_bayar |
| --- |---|---|---|---| 
| 350000 | 2 | false | 0 | 0 | 
| 350000 | 2 | false | 0 | 0 | 
| 350000 | 2 | false | 17500 | 332500 | 
| 350000 | 2 | false | 17500 | 332500 | 

**Kasus C**

input: `is_member = false`, `total_awal = 100000`, `jumlah_buku = 1`

| total_awal | jumlah_buku | is_member | nominal_diskon | total_bayar |
| --- |---|---|---|---| 
| 100000 | 1 | false | 0 | 0 | 
| 100000 | 1 | false | 0 | 0 | 
| 100000 | 1 | false | 0 | 0 |
| 100000 | 1 | false | 17500 | 100000 | 
| 100000 | 1 | false | 17500 | 100000 | 

