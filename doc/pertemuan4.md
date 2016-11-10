#Retrieve, Shapefile, dan shp/dbf

Retrieve merupakan salah satu bagian dari manipulasi data yang digunakan untuk melihat isi dari data geospasial yang berbentuk shapefile. dan merupakan salah satu cara untuk kita melakukan record dari file shp dimana kita bisa melakukan select maupun view.

Shapefile merupakan sebuah format dari data geospasial atau topologi tersebut yang menyimpan data geografis suatu lokasi dan informasi.

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


Link scan plagiarism : https://drive.google.com/file/d/0B9frXx67PauPRHo4TE9qUU9XUmc/view?usp=drive_web
