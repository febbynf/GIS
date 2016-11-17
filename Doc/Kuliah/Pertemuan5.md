#Membuat Data Geospasial

Latar Belakang

              File .shp merupakan file berekstensi shapefile yang dapat digunakan untuk membuat file peta pada ESRI. Cara pembacaan, penghitungan dan pencarian telah kita lakukan pada tutorial sebelumnya (link). Disini kita akan belajar bagaimana cara membuat file berekstensi .shp.

Pembahasan

Method pada writer :
Point(x,y) yaitu m
emasukan data berbentuk point kedalam shp dan seluruh data harus format ESRI = 1
Poly[[[a,b],[c,d]]] yaitu m
emasukan data geospasial berbentuk polygon (kembali ke titik awal) dan polyline tidak kembali ke titik awal
Field(‘kota’,’c’,’40’) yaitu m
embuat atribut table bernama budaya dengan tipe data varchar dengan panjang 40 karakter, jika ingin tambah field. Contoh : field(‘budaya’,’c’,’40’)
Record(‘Bandung’) yaitu m
engisi table yang hanya 1 field dengan value = Bandung. Jika ada 2 field maka record(‘Bandung’,’kota’)
Save(‘nama file’) yaitu m
enyimpan file shapefile di computer
       Kita mulai bagaimana cara membuatnya perlangkah dengan perintah python yang digunakan untuk membuat sebuah shapefile:

      Import Shapefile
            febby = shapefile.Writer(param)

h           Param dalam writer ini menunjukan shapetype apa yang akan kita buat contohnya polygon, polyline, dan point.
POINT :
           Import.shapefile
           a=shapefile.Writer()
           a.point(10,12)

POLYLINE:
           Import.shapefile
           a=shapefile.Writer()
           a.poly(parts[(1,5),(5,5),(3,3)])
           shapetype=shapefile.POLYLINE

POLIGON
           Import.shapefile
           a=shapefile.Writer()
           a.poly(parts=[(1,5),(5,5),(3,3)])

            febby.point(x,y)
    
            Atau,

      febby.poly([x,y],[v,w])
            
          Perintah ini digunakan jika akan membuat file shp.

            febby.field(‘nama’,’typedata’,’90’)

                   Perintah ini digunakan jika akan membuat file dbf.

      febby.record(‘isi’)

               Perintah ini digunakan untuk mengisi file dbf.

            febby.shp(‘namafile.shp’)
      save(‘namafile’)

                Perintah untuk menyimpan file.


Kesimpulan
       
       Dengan menggunakan python kita bisa membuat file .shp baik berupa point, polyline atau poligon. 

