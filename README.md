# Membedah Permintaan Maaf Jokowi

Memanfaatkan Twitter API, saya mengumpulkan data twit Presiden Joko Widodo sejak 20 Juni 2015 hingga 1 Juli 2021. Lalu menganalisisnya dengan mencari substring kata "maaf" pada twitnya, lalu menghasilkan kesimpulan berikut:

1. Selama kurang lebih 6 tahun menjadi presiden, Jokowi hanya mengunggah 10 twit dengan kata "maaf" di dalamnya.
2. 7 twit di antaranya, berkaitan dengan bulan suci Ramadan dan perayaan Idul Fitri.
3. 3 twit yang tidak berhubungan dengan Idul Fitri/Ramadan adalah sebagai berikut:
  - Permintaan maaf karena pengalihan jalan di Medan, Sumatera Utara, akibat acara pernikahan Kahiyang & Robby
  - Permintaan maaf karena tidak bisa menemui WNI dalam kunjungannya di Sydney
  - Permintaan maaf karena listrik yang sering mati, sembari menpromosikan pembangunan pembangkit listrik baru

Berikut beberapa proses dan tahapan dalam analisis data
- [Scraping data Twitter dengan Python](https://github.com/louislugas/twitter-data-jokowi/blob/main/twitter-scrape.txt)
- [Analisis menggunakan spreadsheet](#analisis-menggunakan-spreadsheet)

## Analisis menggunakan spreadsheet

1. Menentukan substring atau kata yang ingin dicari di dalam twit. Dalam hal ini, kata yang akan dicari adalah "maaf".
2. Menggunakan formula `=ISNUMBER(SEARCH(CELL 1 ,CELL 2))` di mana Cell 1 berisi kata yang akan di cari, dan Cell 2 adalah Cell konten twit. Formula ini akan menghasilkan `TRUE` atau `FALSE`.
3. Menggunakan formula `=COUNTIF(CELL 3, "TRUE")` di mana Cell 3 berisi hasil formula di nomor 2, menghasilkan jumlah twit yang mengandung kata dalam Cell 1
  

---
-[Data Twit Jokowi](https://github.com/louislugas/twitter-data-jokowi/blob/main/Jokowi_tweets.xlsx)
