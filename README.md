# Berlin Historic Clubs Dataset

A curated dataset of 106 closed/historic nightclubs and music venues in Berlin, documenting the city's legendary club culture from the late 1960s through 2020.

## Dataset Contents

This repository contains location and contextual data for historic Berlin clubs in two formats:

- **berlin_historic_clubs.csv** (26KB) - Spreadsheet format with all fields
- **berlin_historic_clubs.geojson** (59KB) - GeoJSON format for mapping applications

## Data Fields

Each club entry includes:

- **name** - Club name (original naming preserved, including German characters)
- **Category** - Berlin district/neighborhood (Mitte, Friedrichshain, Neukölln, etc.)
- **address** - Full street address with postal code
- **years** - Years of operation (e.g., "2002–2013", "late 1990s–2010")
- **Music** - Music genres and styles (e.g., "techno, house, drum & bass")
- **description** - Historical context, cultural significance, notable features

## Sample Entry

```csv
Club ZMF,Mitte,"Brunnenstraße 10, 10119 Berlin",2002–2013,"house, electro, techno, indie/britpop",Low‑ceilinged basement 'Zur Möbelfabrik' near Rosenthaler Platz; raw post‑reunification vibe.
```

## Data Sources

**Original location data (lat/lon coordinates):**
- Extracted from the [Berlin History App](https://api.berlinhistory.app) (October 2025)
- Theme: "Geschlossene Berliner Clubs" (Closed Berlin Clubs)
- 106 venues with verified GPS coordinates

**⚠️ IMPORTANT DATA QUALITY NOTICE:**

**All other fields (address, music genres, descriptions, years, categories) were AI-researched and generated.** While efforts were made to ensure accuracy by cross-referencing multiple sources, this data should be considered:

- **Informational/educational use only**
- **Not verified by primary sources**
- **May contain inaccuracies or incomplete information**
- **Subject to interpretation and AI inference**

**Only the latitude/longitude coordinates are from the original Berlin History App dataset and can be considered reliable.**

If you require verified historical information for academic research, journalism, or archival purposes, please consult primary sources such as:
- Berlin club archives and cultural institutions
- Historical city records
- Direct interviews with venue operators and cultural historians
- Newspaper archives and contemporary documentation

## Notable Clubs Included

Historic venues documented in this dataset include:

- **Tresor** - Legendary techno club in a former bank vault
- **E-Werk** - Influential 90s techno club in a 1920s substation
- **Bar 25** - Open-air Spree riverside club (2003-2010)
- **Maria am Ostbahnhof** - Major techno/DnB venue (late 1990s-2010)
- **Berghain/Panorama Bar** (historic predecessor locations)
- **WMF** - Nomadic club that moved through 8 locations (1991-2010)
- **Eimer Club** - Legendary squat venue and post-wall cultural crucible
- **Dschungel** - West Berlin's Studio 54-style icon (1978-1993)
- **SchwuZ** - Germany's oldest queer club (1977-present, relocated 2013)

And 97 more venues spanning eras from late-60s disco to 2020s techno culture.

## Coverage

**Temporal range:** 1968 (earliest: Cheetah disco) to 2020 (latest: Griessmühle closure)

**Geographic coverage:** All major Berlin districts
- Mitte (historic center, post-wall club epicenter)
- Friedrichshain (riverside clubs, Ostbahnhof area)
- Kreuzberg (alternative/punk scene)
- Neukölln (DIY spaces, canal venues)
- Prenzlauer Berg (GDR-era venues)
- Tiergarten/Schöneberg (West Berlin nightlife)

**Cultural eras documented:**
- Late 60s-70s West Berlin disco era
- 80s New Wave and alternative scene
- Post-reunification explosion (1990-1997)
- 2000s minimal/tech-house era
- 2010s DIY and eviction era

## File Formats

### CSV Format
Standard comma-separated values with quoted text fields. Compatible with Excel, Google Sheets, data analysis tools.

### GeoJSON Format
Standard GeoJSON FeatureCollection with Point geometries. Compatible with:
- Mapping libraries (Mapbox, Leaflet, Google Maps)
- GIS software (QGIS, ArcGIS)
- Web mapping applications

Coordinate format: `[longitude, latitude]` (GeoJSON standard)

## Usage Examples

**Load in Python (pandas):**
```python
import pandas as pd
df = pd.read_csv('berlin_historic_clubs.csv')
print(f"Total clubs: {len(df)}")
```

**Load GeoJSON in JavaScript:**
```javascript
fetch('berlin_historic_clubs.geojson')
  .then(response => response.json())
  .then(data => {
    // Add to Mapbox/Leaflet map
    map.addSource('clubs', { type: 'geojson', data: data });
  });
```

## License & Attribution

**Original location data:** Berlin History App (api.berlinhistory.app)

**AI-enhanced data:** Generated for educational/informational purposes. See data quality warning above.

When using this dataset, please include attribution and the data quality disclaimer regarding AI-generated content.

## Project Background

This dataset was created by extracting GPS coordinates from the Berlin History Android app and subsequently enriching the data with contextual information through AI research. The goal is to preserve and visualize the geographic footprint of Berlin's legendary club culture, which has been heavily impacted by gentrification, noise complaints, and urban redevelopment.

## Contributing

If you have corrections, verified historical information, or additional clubs to add, contributions are welcome. Please note that any additions should include verified GPS coordinates and clearly indicate the source of information.

---

**Created:** October 2025
**Total venues:** 106
**Format version:** 1.0
