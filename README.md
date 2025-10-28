# 🗺️ ALICE Data - Complete Dataset for 33 States

**Created:** October 28, 2025
**Purpose:** Economic vulnerability mapping and analysis for American Red Cross
**Coverage:** 33 US States, 2010-2023 (9 data points)

---

## 📁 WHAT'S IN THIS FOLDER

This folder contains **COMPLETE** ALICE (Asset Limited, Income Constrained, Employed) economic vulnerability data combined with Red Cross organizational boundaries and US Census demographics.

**ALICE = Working Poor**: Households earning above poverty but below the actual cost of living in their community.

---

## 📊 THE 5 FILES YOU HAVE

### 🌟 FILE 1: MASTER_counties_redcross_alice_demographics.csv
**THIS IS YOUR PRIMARY FILE - USE THIS FOR MOST ANALYSIS**

| What It Is | Records | Coverage |
|------------|---------|----------|
| County-level data with EVERYTHING | 21,152 | 33 states, 2,348 counties, 9 years (2010-2023) |

**What's Inside (36 columns):**
- ✅ **Geography:** State, County, FIPS code
- ✅ **Time Series:** 2010, 2012, 2014, 2016, 2018, 2019, 2021, 2022, 2023
- ✅ **ALICE Data:** Poverty %, ALICE %, Combined vulnerability rate
- ✅ **Red Cross:** Chapter, Region, Division assignments
- ✅ **Demographics (2023):** Population, income, age, race, housing, unemployment

**Use This File For:**
- Choropleth maps showing county vulnerability
- Time-series analysis (how has vulnerability changed 2010-2023?)
- Filtering by Red Cross Chapter/Region/Division
- Grant applications (show need with demographics + ALICE data)
- Resource allocation decisions

**Key Fields:**
```
State, State_Abbr, Year, FIPS, County
Chapter, Region, Division
Total_Households, Poverty_Households, ALICE_Households, Above_ALICE_Households
Pop_2023, Med_HH_Inc_2023, Median_Age_2023, Unemp_Rate_2023
```

---

### 📁 FILE 2: subcounty_ccd_all_states.csv
**Census County Divisions (CCDs) / Townships**

| What It Is | Records | Coverage |
|------------|---------|----------|
| Sub-county geographic divisions | 23,665 | 33 states, 2023 data only |

**What's Inside (18 columns):**
- ✅ **Geography:** Census County Divisions (CCDs), Townships
- ✅ **ALICE Data:** Household counts by vulnerability level
- ✅ **Red Cross:** Chapter, Region, Division (inherited from parent county)
- ❌ **NO Demographics** (county demographics don't apply to subcounty areas)

**Examples:**
- "Gainesville CCD, Alachua County, Florida"
- "Marbury CCD, Autauga County, Alabama"

**Use This File For:**
- More granular mapping than county-level
- Identifying vulnerable neighborhoods within counties
- Rural township analysis

---

### 📁 FILE 3: subcounty_place_all_states.csv
**Cities, Towns, Census Designated Places**

| What It Is | Records | Coverage |
|------------|---------|----------|
| Incorporated cities and towns | 19,324 | 33 states, 2023 data only |

**What's Inside (18 columns):**
- ✅ **Geography:** Cities, towns, Census Designated Places
- ✅ **ALICE Data:** Household counts by vulnerability level
- ✅ **Red Cross:** Chapter, Region, Division
- ❌ **NO Demographics** (county demographics don't apply)

**Examples:**
- "Birmingham city, Alabama"
- "Boca Raton city, Florida"
- "Akron city, Ohio"

**Use This File For:**
- Urban area vulnerability analysis
- City-level comparisons
- Targeting specific municipalities

---

### 📁 FILE 4: subcounty_zip_all_states.csv
**ZIP Code Tabulation Areas (ZCTAs)**

| What It Is | Records | Coverage |
|------------|---------|----------|
| ZIP code areas | 22,074 | 33 states, 2023 data only |

**What's Inside (18 columns):**
- ✅ **Geography:** 5-digit ZIP codes
- ✅ **ALICE Data:** Household counts by vulnerability level
- ✅ **Red Cross:** Chapter, Region, Division
- ❌ **NO Demographics** (county demographics don't apply)

**Examples:**
- "35004" (St. Clair County, Alabama)
- "32003" (Florida)

**Use This File For:**
- ZIP code level analysis
- Direct mail targeting
- Service delivery planning by ZIP

---

### 📁 FILE 5: RED_CROSS_Reference_All_Counties_Chapters_Regions_Divisions.csv
**Red Cross Organizational Reference**

| What It Is | Records | Coverage |
|------------|---------|----------|
| Complete county-to-Red Cross mapping | 3,162 | ALL US counties with Red Cross assignments |

**What's Inside (58 columns):**
- ✅ **Geography:** County names, FIPS codes, State
- ✅ **Red Cross:** Chapter, Region, Division names and codes
- ✅ **Contact:** Chapter addresses, phone numbers, time zones
- ✅ **Demographics (2023):** Complete census data for reference
- ✅ **FEMA Regions**

**Use This File For:**
- Looking up which Chapter serves a specific county
- Finding Chapter contact information
- Understanding Red Cross organizational structure
- Reference when joining other datasets

**Key Fields:**
```
FIPS, County, State
Chapter, Region, Division
ECODE (Chapter code), RCODE (Region code), DCODE (Division code)
Address, Phone, Time_Zone, FEMA_Region
Pop_2023, Med_HH_Inc_2023, Total_HH_2023
```

---

## 🎯 WHICH FILE SHOULD I USE?

| If You Want To... | Use This File |
|-------------------|---------------|
| **Map county-level vulnerability over time (2010-2023)** | MASTER file |
| **Show trends in economic hardship** | MASTER file |
| **Filter by Red Cross Chapter/Region** | MASTER file |
| **Include demographics in analysis** | MASTER file |
| **Map cities or towns specifically** | subcounty_place file |
| **Map by ZIP code** | subcounty_zip file |
| **Show sub-county detail** | subcounty_ccd file |
| **Look up which Chapter serves a county** | RED_CROSS_Reference file |
| **Get Chapter contact info** | RED_CROSS_Reference file |

**Bottom Line:** Start with the **MASTER** file for 90% of use cases.

---

## 📈 KEY METRICS EXPLAINED

### ALICE Data Fields (In All Files)

| Field | What It Means |
|-------|---------------|
| **Total_Households** | All households in this area |
| **Poverty_Households** | Households below Federal Poverty Level (FPL) |
| **ALICE_Households** | Households above FPL but below survival budget (the "working poor") |
| **Above_ALICE_Households** | Households that can afford basic needs |

### Calculate These Key Metrics

**Poverty Rate (%):**
```
(Poverty_Households / Total_Households) × 100
```

**ALICE Rate (%):**
```
(ALICE_Households / Total_Households) × 100
```

**Combined Vulnerability Rate (%):** ← **USE THIS FOR CHOROPLETH MAPS**
```
((Poverty_Households + ALICE_Households) / Total_Households) × 100
```

---

## 🗺️ HOW TO MAP THIS DATA

### Step 1: Choose Your File
- County map → MASTER file
- City map → subcounty_place file
- ZIP map → subcounty_zip file

### Step 2: Get Shapefiles
Download from US Census TIGER/Line:
- Counties: https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-line-file.html
- Places: Same site, select "Places"
- ZCTAs: Same site, select "ZIP Code Tabulation Areas"

### Step 3: Join Data to Shapefile
**Join Field:**
- Counties → Use **FIPS** field (5-digit code like "12001")
- Places → Use **GEO_ID** field
- ZIPs → Use **GEO_ID** field (5-digit ZIP)

### Step 4: Create Choropleth
**Color by:** Combined Vulnerability Rate (calculate as shown above)

**Recommended Color Scale:**
- 0-20%: Green (Low vulnerability)
- 20-40%: Yellow (Moderate)
- 40-60%: Orange (High)
- 60%+: Red (Very High vulnerability)

### Step 5: Filter by Red Cross Organization
- **By Chapter:** `Chapter == "ARC of North Central Florida"`
- **By Region:** `Region == "Florida Region"`
- **By Division:** `Division == "Southeast and Caribbean Division"`

---

## 🏢 RED CROSS ORGANIZATIONAL STRUCTURE

### Hierarchy
```
Division (6 total)
  └─ Region (39 total)
      └─ Chapter (170 total)
          └─ Counties (3,162 total)
```

### The 6 Divisions
1. **Southeast and Caribbean Division** (includes FL, GA, AL, MS, SC, NC, TN, etc.)
2. **Southwest and Rocky Mountain Division** (TX, etc.)
3. **Mid-Atlantic Division**
4. **Midwest Division**
5. **Pacific Division**
6. **Northeast Division**

### Looking Up Chapter Info
Use the **RED_CROSS_Reference** file to find:
- Which Chapter serves any county
- Chapter contact information
- Region and Division assignments
- FEMA Region assignments

---

## 📊 DATA COVERAGE & COMPLETENESS

### States Included (33 total)
Alabama, Arkansas, Colorado, Connecticut, Delaware, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Louisiana, Maine, Maryland, Michigan, Minnesota, Mississippi, New Jersey, New Mexico, New York, North Carolina, Ohio, Oregon, Pennsylvania, South Carolina, Tennessee, Texas, Virginia, Washington, West Virginia, Wisconsin

### States NOT Included (17 total)
Alaska, Arizona, California, Kentucky, Massachusetts, Missouri, Montana, Nebraska, Nevada, New Hampshire, North Dakota, Oklahoma, Rhode Island, South Dakota, Utah, Vermont, Wyoming

(No ALICE data available for these states in the source dataset)

### Years Available
- **MASTER file:** 2010, 2012, 2014, 2016, 2018, 2019, 2021, 2022, 2023 (9 years)
- **Subcounty files:** 2023 only

### Data Quality
- **MASTER file:** 99.9% complete (all fields)
- **Subcounty files:** 98%+ have Red Cross org data, 100% have ALICE data
- **Missing records:** <2% due to territories, unassigned areas, data gaps

---

## 💡 COMMON USE CASES

### 1. Chapter Vulnerability Map
**Goal:** Show which counties in your Chapter have highest need

**Steps:**
1. Open MASTER file
2. Filter: `Chapter == "Your Chapter Name"` AND `Year == 2023`
3. Calculate: `Vulnerability_Rate = (Poverty_Households + ALICE_Households) / Total_Households * 100`
4. Join to county shapefile using FIPS
5. Create choropleth colored by Vulnerability_Rate
6. Add labels with county names

### 2. Trend Analysis
**Goal:** Show how vulnerability has changed over time

**Steps:**
1. Open MASTER file
2. Select years: 2010, 2016, 2023
3. Calculate vulnerability rate for each year
4. Create 3 side-by-side maps or line charts
5. Show increase/decrease by county

### 3. Grant Application Support
**Goal:** Demonstrate need for funding

**Steps:**
1. Open MASTER file, filter to 2023
2. Select high-vulnerability counties (>50% combined rate)
3. Export list with:
   - County name
   - Vulnerability %
   - Total affected households
   - Population
   - Median income
4. Add narrative about "working poor" (ALICE households)

### 4. City-Level Analysis
**Goal:** Find vulnerable neighborhoods within a county

**Steps:**
1. Open subcounty_place file
2. Filter: `County == "Your County, State"`
3. Calculate vulnerability rate for each city
4. Join to place shapefile
5. Create map showing variation within county

---

## 🔧 TECHNICAL NOTES

### File Formats
- All files are CSV (comma-separated values)
- Open in Excel, Tableau, ArcGIS, QGIS, Python, R

### Coordinate System
- Shapefiles use EPSG:4326 (WGS84)
- Standard for web mapping and ArcGIS Online

### Field Naming
- Underscores used (e.g., `Total_Households`)
- Year suffix for time-specific fields (e.g., `Pop_2023`)
- ALICE fields clearly labeled

### Data Sources
- **ALICE Data:** United For ALICE (www.unitedforalice.org)
- **Red Cross Org:** American Red Cross internal databases
- **Demographics:** US Census Bureau / Commercial data provider (2023)
- **County Boundaries:** US Census TIGER/Line (2020)

---

## 📞 QUESTIONS?

### About ALICE Methodology
Visit: https://www.unitedforalice.org/methodology

### About the Data
- ALICE data uses American Community Survey (ACS) estimates
- Different survey periods (1-year, 3-year, 5-year) based on population size
- See `ACS_Source` field to know which survey was used

### Data Vintage
- **ALICE Data:** 2023 (most recent available)
- **Demographics:** 2023
- **Red Cross Org Data:** Current as of October 2025
- **County Boundaries:** 2020 Census

---

## 🎉 YOU'RE READY!

**Quick Start Checklist:**
1. ✅ You have 5 files in this folder
2. ✅ You know the MASTER file is your primary file
3. ✅ You understand what ALICE means (working poor)
4. ✅ You know how to calculate vulnerability rate
5. ✅ You can look up Red Cross assignments in the reference file

**Next Steps:**
- Open the MASTER file in Excel/Tableau/ArcGIS
- Filter to your Chapter or Region
- Calculate vulnerability rates
- Create your first map!

---

**Last Updated:** October 28, 2025
**Data Repository:** https://github.com/franzenjb/alice-data-mapper
**Questions:** Review this README or contact your data team

---

*May this data help guide resources to those who need them most.*
