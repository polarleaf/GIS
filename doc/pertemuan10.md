#Open Layer

 

Open Layer adalah library javascript murni untuk menampilkan data peta di berbagai browser, tanpa server side dependencies. Open Layer mengimplementasikan javascript API untuk membangun rich web-based geographic application yang mirip dengan Google Maps dan MSN Virtual Earth APIS.

Overlay merupakan proses penempatan grafis suatu peta diatas grafis peta lainnya agar menghasilkan gabungan kedua peta yang memiliki informasi atribut dari kedua peta tersebut. Teknik overlay dalam sistem informasi geografis ada 2 yaitu gabungan (union) dan irisan (intersect). 

Marker atau penanda genetic merupakan penciri individu yang dilihat oleh mata atau terdeteksi dengan alat tertentu yang menunjukkan genotype suatu individu. Di dalam sebuah peta atau maps, marker adalah suatu tanda yang menjelaskan atau memberitahukan suatu tempat atau wilayah agar user mengetahui lokasi yang dimaksud

Source Web 
http://openlayers.org/en/latest/examples/overlay.html?q=overlay

#Mau yang bener, liat saja raw nya

 <!DOCTYPE html>
<html>
  <head>
    <title>Overlay</title>
    <link rel="stylesheet" href="https://openlayers.org/en/v3.20.1/css/ol.css" type="text/css">
    <!-- The line below is only needed for old environments like Internet Explorer and Android 4.x -->
    <script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=requestAnimationFrame,Element.prototype.classList,URL"></script>
    <script src="https://openlayers.org/en/v3.20.1/build/ol.js"></script>
    <script src="https://code.jquery.com/jquery-2.2.3.min.js"></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
    <style>
      #marker {
        width: 30px;
        height: 30px;
        border: 7px solid #088;
        border-radius: 60px;
        background-color: #0000CD;
        opacity: 3.0;

      }
      #bandung {
        text-decoration: none;
        color: #FF0000;
        font-size: 11pt;
        font-weight: bold;
      }
      #marker1 {
        width: 30px;
        height: 30px;
        border: 7px solid #088;
        border-radius: 60px;
        background-color: #0000CD;
        opacity: 3.0;
      }
      #pamekasan {
        text-decoration: none;
        color: #FF0000;
        font-size: 11pt;
        font-weight: bold;
      }
      .popover-content {
        min-width: 180px;
      }
    </style>
  </head>
  <body>
    <div id="map" class="map"></div>
    <div style="display: none;">
      <!-- Clickable label for Vienna -->
      <a class="overlay" id="bandung" target="_blank" href="https://id.wikipedia.org/wiki/Kota_Bandung">Bandung</a>
      <div id="marker" title="Marker"></div>
      <!-- Clickable label for Vienna -->
      <a class="overlay" id="pamekasan" target="_blank" href="https://id.wikipedia.org/wiki/Kabupaten_Pamekasan">Pamekasan</a>
      <div id="marker1" title="Marker"></div>
      <!-- Popup -->
      <div id="popup" title="Welcome to My Maps"></div>
    </div>
    <script>

      var map = new ol.Map({
        layers: [
          new ol.layer.Tile({
            source: new ol.source.XYZ({
              url: 'https://map.vas.web.id/wmts/agm/webmercator/{z}/{x}/{y}.png'
            })
          })
        ],
        target: 'map',
        view: new ol.View({
          center: ol.proj.transform([118.015776, -2.6000285], 'EPSG:4326', 'EPSG:3857'),
          zoom: 5
        })
      });

      var pos = ol.proj.fromLonLat([107.609810,-6.914744]);

      // Vienna marker
      var marker = new ol.Overlay({
        position: pos,
        positioning: 'center-center',
        element: document.getElementById('marker'),
        stopEvent: false
      });
      map.addOverlay(marker);

      // Vienna label
      var bandung = new ol.Overlay({
        position: pos,
        element: document.getElementById('bandung')
      });
      map.addOverlay(bandung);

      var pos1 = ol.proj.fromLonLat([113.4739,-7.1542]);

      // Vienna marker
      var marker1 = new ol.Overlay({
        position: pos1,
        positioning: 'center-center',
        element: document.getElementById('marker1'),
        stopEvent: false
      });
      map.addOverlay(marker1);

      // Vienna label
      var pamekasan = new ol.Overlay({
        position: pos1,
        element: document.getElementById('pamekasan')
      });
      map.addOverlay(pamekasan);

      // Popup showing the position the user clicked
      var popup = new ol.Overlay({
        element: document.getElementById('popup')
      });
      map.addOverlay(popup);

      map.on('click', function(evt) {
        var element = popup.getElement();
        var coordinate = evt.coordinate;
        var hdms = ol.coordinate.toStringHDMS(ol.proj.transform(
            coordinate, 'EPSG:3857', 'EPSG:4326'));

        $(element).popover('destroy');
        popup.setPosition(coordinate);
        // the keys are quoted to prevent renaming in ADVANCED mode.
        $(element).popover({
          'placement': 'top',
          'animation': false,
          'html': true,
          'content': '<p>The location you clicked was:</p><code>' + hdms + '</code>'
        });
        $(element).popover('show');
      });
    </script>
  </body>
</html>

GitHub
github.com/polarleaf/GIS/

Link Scan Plagiarism
https://drive.google.com/file/d/0B17w878LGlWFX3V6TUpYRktMMUE/view

Referensi
https://gilangromadhanutartila.blogspot.co.id/2017/01/resume-pertemuan-10-sistem-informasi.html
