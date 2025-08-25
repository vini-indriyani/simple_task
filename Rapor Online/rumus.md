# Rumus INDEX & MATCH
Rumus umum INDEX & MATCH
```markdown
=INDEX(array_nilai, MATCH(nilai_cari, array_cari, 0))
```
Implementasi
```markdown
=INDEX(IMPORTRANGE("link file database", "identitas!B1:B37"), 
MATCH(1, (IMPORTRANGE("link file database", "identitas!A1:A37")=$B$1)*
(IMPORTRANGE("link file database", "identitas!C1:C37")=$C$1), 0))
```
  ### Penjelasan
  - IMPORTRANGE berfungsi untuk mengambil nilai dari file lain
  - Range identitas!B1:B37 merupakan nilai hasil yang dicari
  - Range identitas!A1:A37 dan identitas!C1:C37 merupakan range kategori yang dijadikan index untuk mencari nilai

# Rumus VLOOKUP
Rumus umum VLOOKUP
```markdown
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup]).
```
Implementasi
```markdown
=VLOOKUP($B$2, IMPORTRANGE("link file database", "NILAI!B1:BJ38"), 2, FALSE)
```
  ### Penjelasan
  - IMPORTRANGE berfungsi untuk mengambil nilai dari file lain
  - $B$2 merupakan cell yang berisi nama siswa
  - Range NILAI!B1:BJ38 merukapan range nilai semua siswa
  - 2 merupakan perintah mengambil nilai 2 pada range nilai
  - False merupakan perintah untuk mengambil nilai yang sama persis
