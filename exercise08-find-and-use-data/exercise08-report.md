# Fundamentals of Agro-Environmental Data Science  
## Exercise 8 – Find and use data online

**Student:** Aster Noel Dsouza  
**Course:** Fundamentals of Agro-Environmental Data Science  
**Exercise:** 8  
**Submission date:** 21 November 2025

---
## 1. Identify if an API is available

| Platform | URL | Path to API information | Documentation URL | API URL example | Data format |
|--------|-----|------------------------|-------------------|-----------------|-------------|
| GBIF | https://www.gbif.org/ | Home → Footer → API | https://techdocs.gbif.org/en/openapi/ | https://api.gbif.org/v1/species/search?q=Quercus | JSON |
| Eurostat | https://ec.europa.eu/eurostat/ | Home → Data → Developers → Web services | https://ec.europa.eu/eurostat/web/main/data/web-services | https://ec.europa.eu/eurostat/api/dissemination/statistics/1.0/data/tps00001 | JSON |
| INE (Portugal) | https://www.ine.pt/ | Home → Footer → Resources (Services, Feeds and APIs) | https://www.ine.pt/xportal/xmain?xpid=INE&xpgid=ics_feeds&xlang=en | https://www.ine.pt/ine/json_indicador?p_indicador=0012756 | JSON |
| Climate Data Store | https://cds.climate.copernicus.eu/ | Home → API → How to use the CDS API | https://cds.climate.copernicus.eu/how-to-api | https://cds.climate.copernicus.eu/api/v2 | NetCDF, GRIB |
| Copernicus Data Space Ecosystem | https://dataspace.copernicus.eu/ | Home → Footer → Analysis → APIs | https://dataspace.copernicus.eu/analyse/apis | https://catalogue.dataspace.copernicus.eu/resto/api/collections | JSON |
| WMO | https://worldweather.wmo.int/en/home.html | No public API information found | N/A | N/A | HTML |
| Agri4Cast | https://agri4cast.jrc.ec.europa.eu/ | Home → Data Portal | No public API documentation found | N/A | CSV, PDF |
| European Environment Agency | https://www.eea.europa.eu/ | Home → Analysis and data → Datahub | No public API documentation found | N/A | Multiple (CSV, XLS, SHP, GPKG, etc.) |


The GBIF API is clearly documented and accessible through the official OpenAPI documentation, providing structured biodiversity data in JSON format.

Eurostat provides programmatic access to its data through “Web services”, which correspond to a REST API documented under the Developers section, although it is not explicitly labelled as an API on the homepage.

INE (Portugal) offers machine-readable statistical data via services and feeds accessible from the homepage footer. These services support parameterised requests returning JSON, functioning as an API.

The Climate Data Store provides a documented API intended for programmatic access, primarily via Python, enabling automated retrieval of large climate datasets in formats such as NetCDF and GRIB.

The Copernicus Data Space Ecosystem supports programmatic access through APIs aimed at advanced users, although API information is not immediately visible and is accessed via the footer navigation.

The WMO World Weather platform does not provide publicly documented API services for programmatic data access. Data appears to be intended for human consumption through web pages, with no references to developer-oriented services or machine-readable endpoints.
  
Although Agri4Cast provides open datasets through a data portal, no public or documented API was identified. Data access is primarily designed for manual download via the web interface rather than automated machine-to-machine access.

Although the EEA Datahub uses dynamic filtering and query parameters in the URL, no publicly documented API endpoints are provided for programmatic access. Data access is intended through manual download of datasets rather than automated retrieval.

## 2. Web scraping and hidden APIs

### How can I detect that a web site has hidden data?

Hidden data can be detected by inspecting the network traffic of a webpage using browser developer tools. If data is loaded dynamically when interacting with the page, API calls returning JSON or similar formats can often be identified.

### When should I do web scraping manually versus automatically?

Manual steps are useful when exploring a site for the first time or when the structure is unclear. Automated scraping should be used when data extraction is repetitive, large-scale, or needs to be reproducible.

### Advantages and problems of web scraping

**Advantages:**
- Access to data not officially published
- Automation of repetitive tasks

**Problems:**
- Legal and ethical risks
- Fragile scripts if website structure changes
- Possible violation of terms of service

### Differences between web scraping and APIs

APIs provide structured, stable, and legally supported access to data. Web scraping extracts data from HTML intended for human consumption and is more error-prone. APIs are preferred whenever available.


### Web scraping plan – SASSCAL WeatherNET

**Can I do it legally?**  
Data is publicly accessible for viewing. Scraping may be legal for educational purposes, but terms of use should be checked to ensure compliance.

**Available items for scraping:**  
- Station ID
- Geographic location
- Date
- Weather parameters (temperature, rainfall, humidity)

