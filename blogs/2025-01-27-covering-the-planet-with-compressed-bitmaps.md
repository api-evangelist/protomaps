---
title: "Covering the Planet with Compressed Bitmaps"
url: "https://protomaps.com/blog/pmtiles-compressed-bitmaps/"
date: "2025-01-27"
feed_url: "https://protomaps.com/blog/index.xml"
---
This is the first post explaining how the pmtiles extract command works to slice a smaller tileset from a larger one. Protomaps Builds contains a daily planet tileset - if you want just Canada, or South America, you can pass pmtiles extract a GeoJSON to get only that region. The first step in extracting a slice is computing a tile covering for the target region.
