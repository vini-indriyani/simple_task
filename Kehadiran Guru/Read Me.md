# Laporan Harian Kehadiran Guru
Teman saya meminta bantuan untuk membuat laporan kehadiran guru, terdepat beberapa kondisi yang dia inginkan yakni:
 - Kolom cell terisi dengan nama kelas
 - kolom yang terisi memiliki warna yang berbeda

## Langkah yang dilakukan 
 <b> 1. Membuat basis data yang mudah dibaca oleh formula excel </b>
     <p>Basis data yang diberikan teman saya akan sulit dibaca oleh rumus excel karena harus dibaca secara vertikal dan horizontal seperti pada gambar dibawah ini</p>
     <br><img src="imgs/01 img.PNG" alt="Input">
     <p>Saya mengubah tabel menjadi seperti di bawah ini sehingga mudah dibaca dengan arah horizontal, berikut tabel yang telah saya ubah</p>
     <br><img src="imgs/02 img.PNG" alt="Input">
 <b> 2. Mencari jadwal kelas untuk masing-masing guru </b>
     <p>Saya menggunakan rummus INDEX & MATCH karena untuk mencari nama kelas membutuhkan tiga kriteria yaitu kode guru, jam kelas dan hari. Berikut kode yang saya gunakan:</p>
     ```
     =IFERROR(INDEX(DATABASE!B:B, MATCH(1, (DATABASE!A:A=$AB$13)*(DATABASE!C:C=C14)*(DATABASE!D:D="SELASA"), 0)),"  ")
      ```
     <br>
     <br>Penjelasan
     <br> - Saya menggunakan IFERROR untuk mengantisipasi guru yang tidak memiliki jadwal sehingga tidak muncul NA namun "  "
     <br> - Saya mengggunakan <i>absolute</i> untuk <i>range</i> jam dan hari sehingga bisa di-<i>drag</i> ke bawah, sementara kriteria guru tidak bersifat <i>absolute</i> karena setiap guru memiliki kode yang berbeda sehingga ketika ditarik ke bawah cellnya akan ikut bergerak ke bawah.
    
 <b> 4. Menjumlahkan jumlah jam guru pada hari tersebut </b>
     <br>
     ```
     =COUNTA(V14:AE14)-COUNTIF(V14:AE14,"  ")
     ```
     <br>
     <br>Saya menggunakan COUNTA untuk menghitung seluruh cell kemudian menguranginya dengan cell yang berisi "  " sehingga akan muncul jumlah cell yang terisi dengan nama kelas
     <br>
     <br>
 <b> 5. Memberikan warna pada cell yang memiliki nilai dan membiarkan cell yang kosong berwarna putih </b>
     <br>
     Saya menggunakan dua konditional yaitu range jam kelas dan jumlah jam, untuk range jam kelas saya menggunakan  ``` is not equal to "  " ```, saya juga menggunakan kondisi yang sama pada jumlah jam namun untuk range jumlah jam saya menggunakan 0 sebagai kriteria
     <br>
     <br>
 <b> 6. Hasil akhir </b>
     <br><img src="imgs/03 img.PNG" alt="Input">
     <br>Berikut hasil akhirnya, anda bisa membuka filenya melalui link berikut ini https://docs.google.com/spreadsheets/d/12RZAhiKUjji1P1QdjfzFyqhPdwIZlAFbrZDvNA2FOtY/edit?usp=sharing
     <br>
     <br><b>Terima kasih</b>
 
