---
name: leaflet-mapping
description: >
  Leaflet client-side interactive map layers and tile coordinate bounding.
---

# Leaflet Interactive Maps

## Overview
Leaflet is the leading open-source JavaScript library for mobile-friendly interactive maps. It is lightweight, simple, and has all the mapping features most developers ever need.

## JavaScript Code Example
```javascript
// Initialize map centered at coordinates
var map = L.map('map').setView([51.505, -0.09], 13);

// Add OpenStreetMap tiles
L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
    maxZoom: 19,
    attribution: '&copy; OpenStreetMap'
}).addTo(map);

// Add a marker
L.marker([51.5, -0.09]).addTo(map)
    .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
    .openPopup();
```
