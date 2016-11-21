##Shapefile Phyton

#Membuat data geometri shapefile
--Buka cmd kemudian python
--import shapefile
--sf = shapefile.Writer(shapeType=1)
--sf.shapeType 
--sf.field('NAMA','A','30')
--sf.field('PEMILIK','A','30')
--sf.record('TOKO','Markonah')
--sf.point(10,10,0,0) atau --sf.polygon(10,10,0,0) 
--sf.save('toko.shp') 

#Mengedit data geometri shapefile:
--Buka python
--import shapefile
--sf = shapefile.Editor(shapefile='toko.shp')
--sf.point(19,19,0,0)
--sf.record('Toko Sembako','Komariah')
--sf.save('toko')

#Menghapus data geometri shapefile:
--Buka python 
--import shapefile
--e = shapefile.Editor('toko.shp')
--e.shape(3) //untuk (3) ..pada pemilihan record
--e.delete(3)
--e.save('toko')

#Menampilkan data geometri shapefile:
--Buka python di command prompt
--import shapefile
--sf = shapefile.Reader('toko.shp')
--sf.record() // semua record
--sf.record(0) // record ke 1
--sf.record(1) // record ke 2
--sf.shapes()(0).points // menampilkan


Link Scan Plagiarism
https://drive.google.com/file/d/0B9frXx67PauPckdDV1ZzMWtLbW8/view

Referensi
https://en.wikipedia.org/wiki/Shapefile