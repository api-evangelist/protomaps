---
title: "What is a clustered PMTiles archive?"
url: "https://protomaps.com/blog/pmtiles-cluster/"
date: "2024-01-17"
feed_url: "https://protomaps.com/blog/index.xml"
---
One detail in the PMTiles version 3 specification is a boolean flag called clustered . Popular tools like the pmtiles CLI , tippecanoe and Planetiler always create clustered archives. PMTiles is an open specification in the public domain, so this post is to aid developers in implementing this optional feature.
