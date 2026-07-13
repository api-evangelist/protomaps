---
title: "PMTiles version 3: Disk Layout and Compressed Directories"
url: "https://protomaps.com/blog/pmtiles-v3-layout-compression/"
date: "2022-08-12"
feed_url: "https://protomaps.com/blog/index.xml"
---
PMTiles is a single-file archive format for pyramids of tiled map data. The last post described the new Entry struct to compact repetitive data in-memory; the next step is to further shrink directories for storage on disk and transfer over the Internet. PMTiles is designed to substitute for APIs like this: https://example.s3-like-storage.com/tileset/{z}/{x}/{y}.pbf One storage pattern is to store each tile as its own object, relying on cloud storage’s filesystem-like paths: ┌───┐ ┌────────┐ ┌───▶│███│ /tileset/1/0/0.pbf │ │───┘ └───┘ │ │ ┌───┐ │ S3 │───────▶│███│ /tileset/1/0/1.pbf │ │ └───┘ │
