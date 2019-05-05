<template>
  <div id="map" />
</template>

<script>
import L from 'leaflet';

export default {
  name: 'MainMap',
  mounted() {
    const mymap = L.map('map').setView([51.505, -0.09], 13);

    L.tileLayer('https://api.tiles.mapbox.com/v4/{id}/{z}/{x}/{y}.png?access_token={accessToken}', {
        attribution: 'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
        maxZoom: 18,
        id: 'mapbox.streets',
        accessToken: 'pk.eyJ1IjoiaGVucmlkZWxvemFubmUiLCJhIjoiY2p2OXN3cXYzMGpzdjQ1bW1yM3RsMXo1ayJ9.4FNTFEq1qaN6FkYwJ8SjMQ'
    }).addTo(mymap);
  },
}
</script>
