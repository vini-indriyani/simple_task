# Rapor Online
Di sekolah teman saya tidak boleh ada ranking namun, murid yang wali kelasnya teman saya ingin mengetahui ranking mereka.
Sehingga teman saya meminta bantuan saya untuk membuar rapor <i>online</i>.

Cara kerja lapor <i>online</i> yang saya buat sangat sederhana, ketika siswa melakukan <i>input</i> NISN dan kode yang telah diberikan maka akan muncul
nama, nilai dan ranking sesuai dengan NISN mereka.

## Rumus yang digunakan
- IMPORTRANGE
  Saya menggunakan IMPORTRANGE karena basis data nilai siswa dibuat di file terpisah yang hanya bisa diakses oleh saya dan teman saya. Siswa hanya bisa melihat nilai mereka masing-masing.
  
- INDEX MATCH
  <p>Saya menggunakan rumus INDEX MATCH untuk mencari nama siswa dengan melakukan <i>input</i> dua kritesia yaitu: NISN dan kode, seperti pada gambar di bawah ini:</p>
  <img src="imgs/01 img.PNG" alt="Input">
  <p>Nama siswa akan muncul setelah siswa melakukan <i>input</i> NISN dan kode dengan benar, seperti pada gambar di bawah ini:</p>
  <img src="imgs/02 img.PNG" alt="Input">
  
- VLOOKUP
  <p> Saya mengggunakan VLOOKUP untuk mengambil nilai mata pelajaran dan ranking berdasarkan nama siswa, tabel nilai akan error jika nama siswa kosong seperti pada gambar di bawah ini</p>
  <img src="imgs/03 img.PNG" alt="Input">
  <p>Jika nama siswa muncul karena siswa telah melakukan <i>input</i> NISN dan kode dengan benar maka akan muncul seluruh nilai rapor pada semester 3 dan 4 seperti pada gambar di bawah ini</p>
  <img src="imgs/04 img.PNG" alt="Input">

## File Spreadsheet
Berikut file spreadsheet sebagai bahan ajar, untuk melakukan input silahkan <i>copy</i> file https://docs.google.com/spreadsheets/d/1tQGCtxroiJ8uJxKISAouNyYF_vff8GJY33ngKhLp-JU/edit?gid=0#gid=0
<br><b>Terima kasih</b>
