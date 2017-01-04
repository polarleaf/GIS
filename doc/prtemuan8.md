#MapProxy

MapProxy adalah proxy open source untuk data geospasial. Cache, mempercepat dan mengubah data dari layanan peta yang ada dan melayani setiap desktop atau web GIS klien.

Konfigurasi menggunakan format mappproxy.yaml. Setiap aspek konfigurasi memiliki akses yang berbeda.

# Service
Di sini Anda dapat mengkonfigurasi layanan harus dimulai. Konfigurasi untuk semua layanan yang dijelaskan dalam dokumentasi Layanan.
Berikut adalah contoh:

services:

  tms:

  wms:

    md:

      title: MapProxy Example WMS

      contact:
      
      # [...]

#Layers
Di sini Anda dapat mendefinisikan semua lapisan MapProxy harus menawarkan. Definisi lapisan mirip dengan WMS: setiap lapisan dapat memiliki nama dan judul dan Anda dapat lapisan sarang untuk membangun pohon lapisan. Lapisan harus dikonfigurasi sebagai daftar (- di YAML), di mana setiap konfigurasi lapisan adalah kamus (key: nilai dalam YAML).

Contoh:

layers:

  - name: mylayer

    title: My Layer

    source: [mysoruce]