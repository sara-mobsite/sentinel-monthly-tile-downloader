# sentinel1-monthly-tile-downloader

A Python script to download the best monthly Sentinel-1 scenes for selected tiles from the Microsoft Planetary Computer using coverage-based selection.

This workflow uses the **Sentinel-2 tiling grid**, which is based on the **Military Grid Reference System (MGRS)**. The selected tile IDs (for example, `21JXJ`, `24LTR`) are Sentinel-2 MGRS tiles used to define the areas of interest for Sentinel-1 data downloads.

## Features

- Search Sentinel-1 scenes from Microsoft Planetary Computer
- Select the best scene for each month for each chosen tile
- Filter scenes by minimum tile coverage
- Download `VV` and `VH` assets
- Save item metadata as JSON
- Export the monthly scene selection as CSV
- Switch between **RTC** and **GRD** by changing `collection_name`

## Requirements

Install the required Python packages:

```bash
pip install geopandas pandas planetary-computer pystac-client requests shapely
