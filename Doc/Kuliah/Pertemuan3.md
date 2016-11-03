Latar Belakang

       Natural Earth memiliki banyak data penampakan bumi dengan format data .shp. Namun file .shp (shapefile) tidak bisa kita lihat secara langsung hasilnya melainkan bisa dilihat dengan software seperti QGIS ataupun dengan bahasa Python. Disini kita akan membahas bagaimana caranya file .shp bisa diretrieve melalui bahas Python untuk memudahkan user membaca Shapefile.

Pembahasan

      Dengan menggunakan Python kita bisa memanggil file .shp dengan memanggil langsung file .shp atau membuat class terlebih dahulu. Fungsi Shapefile digunakan untuk menyimpan data dan menghitung data geospasial. Di file .shp terdapat data yaitu :
        1. Bbox atau boundary box yang berisi 4 titik koordinat (batas view pada peta).
        2. Point
        3. Shapetype yaitu standar nomor pada ESRI

 
Dengan Python kita bisa menuliskan baris perintah :
 >> import shapefile
>> sf = shapefile.Reader(“namafile.shp”)
>> sf.shapes()
>>a = sf.shapes()

>>len(a)

Cara membaca pada geospasial yaitu dengan Dbf dengan menuliskan perintah sf.records() dan Shp dengan menuliskan perintah sf.shapes()

Kesimpulan

      Cara membaca file .shp dapat menggunakan software seperti QGIS dan bahasa Python. Dalam Python dapat dilakukan dengan memanggil file .shp atau membuat class dulu. Dan cara membaca data geospasial yaitu dengan Dbf (data record) dan Shp (data geometri).