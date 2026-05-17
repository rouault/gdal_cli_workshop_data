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
