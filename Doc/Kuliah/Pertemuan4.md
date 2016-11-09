
Latar Belakang

         Bagaimana cara kita bisa mengetahui letak koordinat yang ada di bumi ini. Misalkan kita ingin mengetahui koordinat negara Indonesia. Jika kamu kesulitan bagaimana cara mengetahuinya tenang guys ada caranya. Cukup dengan unggah folder yang ada di web natural earth. Cara unggahnya bisa lihat di tutorial sebelumnya yaitu data geospasial cultural. Kemudian kita bisa menggunakan python untuk mencari letak negaranya.

Pembahasan

        Dbf dan shp adalah format data pada ESRI . Dbf merupakan data tabel, atribut data dan shp adalah data geometri (titik, garis, poligon).

Operasi pada python


sf = shapefile.Reader(‘batas.shp’)
Sf                    = variable initiati
Shapefile        = nama file/class
Reader            = method
(‘batas.shp’)   = parameter file shp

Maka var sf adalah inisiasi dari kelas shapefile kita bisa jalankan method di variabel inisiasi

Method 
·         Dbf :
-          sf.fields() : melihat atribute tabel
-          sf.field[4] : melihat atribute ke –n
-          sf.Records() : mengambil semua data
-          sf.Record(4) : mengambil data garis ke –n
-          sf.Record(4)[8] : mengambil data garis ke –n dan baris array ke –n

·         Shp :
-          sf.Shapes() : melihat (tipe data objek) semua record geometri
      example mengambil data ke -n : a = sf.shapes(0)
                                                          dir(a) 

Cara untuk melihat koordinat negara :

                                                            for a in sf.records():
                                                                  if a[0] == "Zimbabwe":
                                                                   print i
                                                                   i = i + 1


Kemudian sistem akan terotomatis memberikan letak ke berapa dari data negara yang dicari. Disini Zimbawe terletak di 253. jadi kita ketikkan :

                         sf.shape(253).points

Dan otomatis letak koordinat negara yang kita cari akan ditampilkan.


Jika diambil dari class yang telah dibuat : 

import negara
letak = negara.Negara('shp/bts_negara.shp')
letak.selectNegara('Indonesia')

Kesimpulan

      Dengan python kita dapat mengetahui letak koordinat sebuah negara. karena python memang bisa membaca file dengan format .shp

