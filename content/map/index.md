---
title: School Map
---

<div id="map" style="height: 400px;"></div>
<script>
  var map = L.map('map').setView([35.8469, 127.1295], 15);
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
    attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
  }).addTo(map);
  L.marker([35.8469, 127.1295]).addTo(map)
    .bindPopup('전북대학교')
    .openPopup();
</script>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
