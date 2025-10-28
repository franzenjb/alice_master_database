
# GeoJSON Files Created

## ✅ counties_with_alice_2023.geojson
- **Size:** 3.9 MB
- **Contains:** All 3,221 US counties with boundaries
- **ALICE Data:** 2,339 counties in 33 states (2023)
- **Ready to use:** YES - Open in any GIS tool or web map

### Properties included:
- County boundaries (polygons)
- FIPS code
- State, County name
- Red Cross: Chapter, Region, Division
- ALICE: Total/Poverty/ALICE households
- **Combined_Vulnerability_Pct** (use this for choropleth coloring!)
- Demographics: Population, Median Income

### How to use:
1. Open in ArcGIS Online, QGIS, Mapbox, or Leaflet
2. Style by "Combined_Vulnerability_Pct" field
3. Filter by "Chapter", "Region", or "Division"
4. Create interactive maps immediately!

## 📊 Subcounty Files (CSV format)
For subcounty mapping (CCDs, Places, ZIPs), use the CSV files:
- subcounty_ccd_all_states.csv
- subcounty_place_all_states.csv  
- subcounty_zip_all_states.csv

These need to be joined to shapefiles in your GIS tool due to file size.

### Where to get shapefiles:
- **Census TIGER/Line:** https://www.census.gov/geographies/mapping-files.html
- **ZIP codes (ZCTAs):** Search "ZCTA shapefile 2023"
- **Places:** Census "Places" shapefile
- **CCDs:** Census "County Subdivisions" shapefile

Join using the GEO_ID field from the CSV to the shapefile's geographic ID.
