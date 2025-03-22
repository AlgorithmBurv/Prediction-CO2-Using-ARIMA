# ARIMA: AutoRegressive Integrated Moving Average

ARIMA adalah metode peramalan deret waktu (time series) yang digunakan untuk memprediksi data masa depan berdasarkan data historis. Metode ini sangat berguna ketika data tidak stasioner dan memiliki tren naik atau turun.

## Apa Itu ARIMA?
ARIMA adalah singkatan dari:
- **AR (AutoRegressive)**: Melihat data dari masa lalu (lag) untuk memprediksi nilai saat ini.
- **I (Integrated)**: Menghilangkan tren agar data lebih stabil (stasioner).
- **MA (Moving Average)**: Mengurangi efek fluktuasi acak.

Secara umum, model ARIMA ditulis sebagai **ARIMA(p, d, q)**, di mana:
- **p** = Jumlah lag pada komponen AutoRegressive (AR)
- **d** = Derajat differencing untuk mencapai stasioneritas
- **q** = Jumlah lag pada komponen Moving Average (MA)

---

## Mengapa Menggunakan ARIMA?
ARIMA digunakan ketika:
1. Data berubah seiring waktu (misalnya, penjualan bulanan atau suhu harian).
2. Data tidak stasioner dan memiliki tren atau pola musiman.
3. Anda ingin memprediksi nilai masa depan dengan mempertimbangkan data masa lalu.

---

## Penjelasan Parameter (p, d, q)
### 1. AutoRegressive (p)
- Mengukur seberapa banyak data sebelumnya (lag) yang digunakan untuk memprediksi nilai saat ini.
- Misalnya, jika **p = 3**, berarti model melihat 3 periode sebelumnya untuk memprediksi periode sekarang.

### 2. Integrated (d)
- Menghilangkan tren dengan menghitung perbedaan data satu kali (d = 1) atau lebih (d = 2, dst.).
- Digunakan agar data menjadi lebih stabil (stasioner).

### 3. Moving Average (q)
- Mengurangi efek fluktuasi acak dengan melihat kesalahan pada lag sebelumnya.
- Misalnya, jika **q = 2**, maka kita melihat kesalahan dari 2 periode sebelumnya.

---

## Cara Kerja ARIMA
1. **Persiapan Data:**
   - Pastikan data berbentuk deret waktu.
   - Periksa apakah data stasioner dengan metode uji statistik (ADF Test).

2. **Pilih Parameter (p, d, q):**
   - Gunakan **Autocorrelation Plot** untuk mengetahui lag terbaik (p dan q).
   - Lakukan differencing (d) untuk membuat data stasioner.

3. **Buat Model ARIMA:**
   - Tentukan parameter (p, d, q) berdasarkan analisis sebelumnya.

4. **Prediksi Data Masa Depan:**
   - Gunakan model untuk melakukan prediksi dan evaluasi hasilnya.

---

## Autocorrelation Plot
Autocorrelation Plot digunakan untuk melihat korelasi data pada lag tertentu. Jika ada korelasi kuat pada lag 1-5, itu menunjukkan adanya pengaruh kuat dari data sebelumnya. Korelasi yang cepat turun ke nol menunjukkan data sudah stasioner.

---

## Kesimpulan
- ARIMA efektif untuk memprediksi data deret waktu yang tidak stasioner.
- Parameter (p, d, q) harus dipilih secara hati-hati berdasarkan analisis data.
- Gunakan Autocorrelation Plot untuk memahami pola lag dan tren.

Selamat mencoba model ARIMA! Jika ada pertanyaan lebih lanjut, jangan ragu untuk menghubungi.

