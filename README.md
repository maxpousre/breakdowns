# breakdowns

testing
<!DOCTYPE html>
<html>
  <head>
    <title>Simple Map</title>
    <meta name="viewport" content="initial-scale=1.0">
    <meta charset="utf-8">
    <style>
      /* Always set the map height explicitly to define the size of the div
       * element that contains the map. */
      #map {
        height: 100%;
      }
      /* Optional: Makes the sample page fill the window. */
      html, body {
        height: 100%;
        margin: 0;
        padding: 0;
      }
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script>
      var map;
      function initMap() {
        map = new google.maps.Map(document.getElementById('map'), {
          center: {lat: 34.023, lng: -84.361},
          zoom: 8
        });
		
		var layer = new google.maps.FusionTablesLayer({
    query: {
      select: '\'Geocodable address\'',
      from: '1mZ53Z70NsChnBMm-qEYmSDOvLXgrreLTkQUvvg'
    }
  });
  layer.setMap(map);
		
      }
    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyDfWGsshfo5D6QcsNT4jIcEX69k36A8Quk&callback=initMap"
    async defer></script>
  </body>
</html>
