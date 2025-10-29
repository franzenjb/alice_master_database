# 🗺️ ALICE Project - Complete Roadmap

**Created:** October 28, 2025
**Author:** Jeff Franzen
**Purpose:** Economic vulnerability data mapping and analysis for American Red Cross

---

## 📦 WHAT YOU HAVE IN THIS FOLDER

### ALICE Master Database (Local Files)
**Location:** `ALICE Master Database/` subfolder

This contains the **complete consolidated dataset** from 33 states:
- County-level ALICE data with demographics (2010-2023)
- Subcounty data: CCDs, Places, ZIP codes (2023 only)
- Red Cross organizational reference
- **Map-ready GeoJSON file**
- Comprehensive documentation

**Start Here:** Open `ALICE Master Database/README.md`

---

## 🌐 YOUR 6 GITHUB REPOSITORIES

You have **6 GitHub repositories** related to ALICE data. Each serves a different purpose:

### 1. 📊 alice_master_database ⭐ NEWEST
**URL:** https://github.com/franzenjb/alice_master_database
**Created:** October 28, 2025
**Purpose:** Complete consolidated dataset for 33 US states

**What's In It:**
- Master county file with full demographics (21,152 records, 2010-2023)
- 3 subcounty files (CCDs, Places, ZIPs) - 2023 only
- Red Cross reference file (all 3,162 US counties)
- **GeoJSON file ready for instant mapping**
- Comprehensive README

**Use This For:**
- Downloading complete datasets
- Sharing data with colleagues
- Backup and version control
- Quick access to map-ready files

---

### 2. 🗺️ alice-red-cross-data [⚠️ ARCHIVED Oct 29, 2025]
**URL:** https://github.com/franzenjb/alice-red-cross-data
**Created:** October 27, 2025
**Status:** Archived - superseded by alice_master_database

**What Was In It:**
- County-level ALICE data
- Red Cross Chapter/Region/Division mapping
- GeoJSON files for ArcGIS
- Shapefile components

**→ Now Use:** alice_master_database - contains all this data plus more

---

### 3. 🏛️ alice-redcross-atlas
**URL:** https://github.com/franzenjb/alice-redcross-atlas
**Created:** October 25, 2025
**Description:** "Red Cross Community Vulnerability Atlas - Interactive ALICE data intelligence platform with 85,846 enriched records across 212 chapters"

**What's In It:**
- Interactive web application
- 85,846 enriched records
- 212 chapters covered
- Advanced analytics platform

**Use This For:**
- Interactive online exploration
- Presenting data to stakeholders
- Chapter-level vulnerability analysis

---

### 4. 🔍 alice-data-explorer
**URL:** https://github.com/franzenjb/alice-data-explorer
**Created:** October 21, 2025
**Description:** "Interactive ALICE Data Explorer with Advanced Choropleth Mapping and Analytics"

**What's In It:**
- Interactive web application
- Advanced choropleth mapping
- Data analytics tools
- Visualization dashboards

**Use This For:**
- Creating interactive maps
- Data exploration and analysis
- Presentations and demos

---

### 5. 📈 alice-demographics [⚠️ ARCHIVED Oct 29, 2025]
**URL:** https://github.com/franzenjb/alice-demographics
**Created:** October 20, 2025
**Status:** Archived - functionality now in alice-redcross-atlas & alice-data-explorer

**What Was In It:**
- Interactive demographics visualization
- Dual-range sliders for filtering
- Census data integration
- Visual exploration tools

**→ Now Use:** alice-redcross-atlas or alice-data-explorer for interactive filtering

---

### 6. 🗂️ alice-data-mapper [⚠️ ARCHIVED Oct 29, 2025]
**URL:** https://github.com/franzenjb/alice-data-mapper
**Created:** October 20, 2025
**Status:** Archived - data consolidated into alice_master_database

**What's In It:**
- Source Excel files for 33 states
- Data processing scripts
- Consolidation tools
- Original state-by-state data files

**Use This For:**
- Methodology reference only
- Understanding how master database was created
- Historical archive of source files

**→ Now Use:** alice_master_database for all current data needs

---

## 🎯 WHICH REPOSITORY SHOULD I USE?

| If You Want To... | Use This Repository |
|-------------------|-------------------|
| **Download complete datasets** | alice_master_database ⭐ |
| **Create a map immediately** | alice_master_database (use GeoJSON file) |
| **Build an interactive web app** | alice-data-explorer or alice-redcross-atlas |
| **Work with ArcGIS/QGIS shapefiles** | alice_master_database (has GeoJSON) |
| **Explore demographics interactively** | alice-redcross-atlas or alice-data-explorer |
| **Access original state files** | alice-data-mapper [ARCHIVED - ref only] |
| **See data processing workflow** | alice-data-mapper [ARCHIVED - ref only] |

---

## 📁 FILE INVENTORY - WHAT'S IN YOUR LOCAL FOLDER

### ALICE Master Database/

| File | Size | Description |
|------|------|-------------|
| **README.md** | 13 KB | **START HERE** - Complete documentation |
| **MASTER_counties_redcross_alice_demographics.csv** | 6.3 MB | Primary dataset - Counties with everything (2010-2023) |
| **counties_with_alice_2023.geojson** | 3.9 MB | **Map-ready GeoJSON** - Drag and drop into GIS! |
| subcounty_ccd_all_states.csv | 5.2 MB | Census County Divisions (2023) |
| subcounty_place_all_states.csv | 3.8 MB | Cities/Towns (2023) |
| subcounty_zip_all_states.csv | 4.0 MB | ZIP Codes (2023) |
| RED_CROSS_Reference_All_Counties_Chapters_Regions_Divisions.csv | 1.5 MB | Complete Red Cross org reference |
| counties_boundaries.geojson | 3.1 MB | Base county boundaries (reference) |
| GEOJSON_FILES_README.md | 1.3 KB | GeoJSON usage instructions |

---

## 🗺️ QUICK START GUIDES

### To Create a County Vulnerability Map (5 minutes):

1. **Option A - Drag & Drop (Easiest)**
   - Open `ALICE Master Database/counties_with_alice_2023.geojson`
   - Drag into ArcGIS Online, QGIS, or http://geojson.io
   - Style by "Combined_Vulnerability_Pct" field
   - Done!

2. **Option B - CSV + Shapefile**
   - Open `ALICE Master Database/MASTER_counties_redcross_alice_demographics.csv`
   - Filter to Year = 2023
   - Join to county shapefile using FIPS code
   - Calculate: (Poverty_Households + ALICE_Households) / Total_Households × 100
   - Style by this calculated field

### To Build an Interactive Web App:

1. Visit: https://github.com/franzenjb/alice-data-explorer
2. Clone the repository
3. Follow README instructions
4. Deploy to GitHub Pages or Netlify

### To Access Source Data by State:

1. Visit: https://github.com/franzenjb/alice-data-mapper
2. Navigate to `data/` folder
3. Download individual state files (e.g., `florida_data.xlsx`)

---

## 📊 DATA COVERAGE SUMMARY

### Geographic Coverage:
- **33 US States** with ALICE data
- **2,348 counties** (98% of counties in covered states)
- **23,665 Census County Divisions** (CCDs)
- **19,324 Cities/Towns/Places**
- **22,074 ZIP Codes**

### Organizational Coverage:
- **170 Red Cross Chapters**
- **39 Red Cross Regions**
- **6 Red Cross Divisions**

### Time Coverage:
- **County data:** 2010, 2012, 2014, 2016, 2018, 2019, 2021, 2022, 2023 (9 years)
- **Subcounty data:** 2023 only

### States Included:
Alabama, Arkansas, Colorado, Connecticut, Delaware, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Louisiana, Maine, Maryland, Michigan, Minnesota, Mississippi, New Jersey, New Mexico, New York, North Carolina, Ohio, Oregon, Pennsylvania, South Carolina, Tennessee, Texas, Virginia, Washington, West Virginia, Wisconsin

---

## 💡 COMMON USE CASES & WHICH REPO TO USE

### 1. Grant Application (Need Data + Narrative)
**Use:** alice_master_database
**Files:** MASTER CSV + README
**Why:** Complete data with demographics, easy to export

### 2. Executive Presentation (Need Interactive Map)
**Use:** alice-data-explorer OR alice-redcross-atlas
**Why:** Beautiful interactive visualizations, web-based

### 3. ArcGIS Dashboard Project
**Use:** alice-red-cross-data + alice_master_database
**Files:** Shapefiles + GeoJSON
**Why:** GIS-ready formats

### 4. Research Paper (Need Source Data)
**Use:** alice-data-mapper
**Why:** Access to original state files and methodology

### 5. Chapter Vulnerability Report
**Use:** alice_master_database
**Filter:** By Chapter name in MASTER CSV
**Why:** Complete time-series data 2010-2023

### 6. Demographic Analysis
**Use:** alice-demographics
**Why:** Interactive demographic filtering tools

---

## 🔧 TECHNICAL REFERENCE

### Data Sources:
- **ALICE Data:** United For ALICE (www.unitedforalice.org)
- **Red Cross Org:** American Red Cross internal databases
- **Demographics:** US Census Bureau (2023)
- **Boundaries:** US Census TIGER/Line (2020)

### File Formats Available:
- ✅ CSV (all repositories)
- ✅ GeoJSON (alice_master_database, alice-red-cross-data)
- ✅ Shapefile (alice-red-cross-data)
- ✅ Excel (alice-data-mapper - source files)

### Coordinate System:
- EPSG:4326 (WGS84) for all spatial files
- Standard for web mapping and ArcGIS Online

---

## 📅 PROJECT TIMELINE

| Date | Repository Created | Purpose |
|------|-------------------|---------|
| Oct 20, 2025 | alice-data-mapper | Original data collection |
| Oct 20, 2025 | alice-demographics | Demographics visualization |
| Oct 21, 2025 | alice-data-explorer | Interactive mapping tool |
| Oct 25, 2025 | alice-redcross-atlas | Red Cross intelligence platform |
| Oct 27, 2025 | alice-red-cross-data | GIS-ready spatial files |
| Oct 28, 2025 | alice_master_database | ⭐ Consolidated master dataset |

---

## 🎓 WHAT IS ALICE?

**ALICE = Asset Limited, Income Constrained, Employed**

ALICE households are the "working poor" - they earn above the Federal Poverty Level but below what it actually costs to live in their community.

**Key Metrics:**
- **Poverty Rate:** % below Federal Poverty Level
- **ALICE Rate:** % above poverty but below survival budget (the working poor)
- **Combined Vulnerability:** Poverty + ALICE = total households struggling
- **Above ALICE:** % who can afford basic needs

**Why This Matters:**
Traditional poverty measures miss 2-3x as many struggling households. ALICE data reveals the true scope of economic hardship.

---

## 📞 NEXT STEPS

1. ✅ **Review this roadmap** - You just did!
2. 📖 **Read the main README** - Open `ALICE Master Database/README.md`
3. 🗺️ **Try the GeoJSON** - Drag `counties_with_alice_2023.geojson` into a map viewer
4. 🌐 **Explore a web app** - Visit alice-data-explorer or alice-redcross-atlas
5. 📊 **Download what you need** - All repos are public and accessible

---

## 🔗 QUICK LINKS

### GitHub Repositories:
1. https://github.com/franzenjb/alice_master_database ⭐
2. https://github.com/franzenjb/alice-red-cross-data
3. https://github.com/franzenjb/alice-redcross-atlas
4. https://github.com/franzenjb/alice-data-explorer
5. https://github.com/franzenjb/alice-demographics
6. https://github.com/franzenjb/alice-data-mapper

### External Resources:
- **ALICE Methodology:** https://www.unitedforalice.org/methodology
- **US Census TIGER/Line:** https://www.census.gov/geographies/mapping-files.html
- **ArcGIS Online:** https://arcgis.com
- **GeoJSON Viewer:** http://geojson.io

---

**Last Updated:** October 28, 2025
**Version:** 1.0
**Maintained By:** Jeff Franzen

---

*This portfolio represents months of data collection, processing, and visualization work to support the American Red Cross mission of helping vulnerable communities.*
