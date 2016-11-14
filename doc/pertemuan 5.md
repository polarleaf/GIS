#Shapefile

<p align="center">
  <img src="/img/GIS1.jpg" width="400px">
</p>

Shapefile merupakan sebuah format dari data geospasial atau topologi tersebut yang menyimpan data geografis suatu lokasi dan informasi. Dimana kita juga bisa menggunakannya pada phyton.

Data Shape file berbentuk .shp ada juga .dbf

Cara Membaca shp 
-          import shapefile
-          sf = shapefile.Reader(“namafile.shp”)
-          sf.shapes()
-          a = sf.shapes()
-          print len(a)

Cara Membaca dbf

-          import shapefile
-          sf.records()
-          sf.records(n)

Shape file yang merupakan standar file Vektor geospasila adalah data yang dikeluarkan secara resmi oleh ESRI.

Data Geometri adalah Data koordinat yang membentuk bangun datar/ruang diantaranya
1. Point/titik, yang memiliki nomor standar 
2.  Line/polyline/garis, yang memiliki nomor standar 
3. Polygon, yang memiliki nomor standar

Cara menambahka record pada shapefile
-  Pada Point = ‘a.point(x,y)’ atau ‘a.point(x,y,0,0)’ dengan domain x dan y adalah koordinat
-  Pada Polyline = ‘a.poly(shapefile=3,parts=[[[x1,y1,z1,w1],[ x2,y2,z2,w2],[……]]])’
-  Pada Polygon = ‘a.poly)shapefile=5,parts=[[[…….],[…….]]])’


Link scan plagiarism : https://drive.google.com/file/d/0B9frXx67PauPRHo4TE9qUU9XUmc/view?usp=drive_web