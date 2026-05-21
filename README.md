# What is this repository

Dataset used by workshop at https://github.com/rouault/gdal_cli_workshop

## Provenance

- S2B_MSIL2A_20260423T094029_N0512_R036_T34TDR_20260423T115714.SAFE/
  S2B_MSIL2A_20260423T094029_N0512_R036_T34TER_20260423T115714.SAFE/
  S2B_MSIL2A_20260423T094029_N0512_R036_T34TES_20260423T115714.SAFE/

  Sentinel 2 scenes from Sentinel Hub. Files larger than 100 MB removed, except
  S2B_MSIL2A_20260423T094029_N0512_R036_T34TDR_20260423T115714.SAFE/GRANULE/L2A_T34TDR_A047681_20260423T094113/IMG_DATA/R10m/T34TDR_20260423T094029_B08_10m.jp2 that has been reprocessed to a reduced precision using
  ``gdal raster convert`` with ``--of JP2OpenJPEG --creation-option QUALITY=45 --co BLOCKXSIZE=1024 --co BLOCKYSIZE=1024``
  settings to fit under 100 MB.

- timisoara.osm.pbf

  Subset of https://download.geofabrik.de/europe/romania-260516.osm.pbf generated with:

  ``osmium extract -b 20.99713,45.62764,21.51496,45.89526 romania-260516.osm.pbf -o timisoara.osm.pbf``

- dem.tif

  Source:

  ``gdal raster clip /vsicurl/https://opentopography.s3.sdsc.edu/raster/SRTM_GL1/SRTM_GL1_srtm.vrt dem.tif --bbox 399960,4990200,609780,5200020 --bbox-crs EPSG:32634 --co COMPRESS=LZW --co TILED=YES --co PREDICTOR=2``

- ne_10m_admin_1_states_provinces.zip from https://www.naturalearthdata.com/downloads/10m-cultural-vectors/

