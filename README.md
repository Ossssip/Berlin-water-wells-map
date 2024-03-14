# Berlin-water-wells-map
A project showcasing [Berlin street water pumps](https://www.berlin.de/umwelt/themen/wasser/artikel.155619.php) and the time required to reach the nearest one.

[See the interactive map on Github Pages](https://ossssip.github.io/Berlin-water-wells-map/).

## Data Sources
- [OpenStreetMap](https://www.openstreetmap.org/copyright), [ODbL](https://opendatacommons.org/licenses/odbl/) - Locations of water wells, calculation of isochrones, and Nominatim search for the map hosted on GitHub Pages.
- [basemap.de Web Raster](https://basemap.de/web_raster/), [BKG](https://www.bkg.bund.de) [dl-de/by-2-0](https://www.govdata.de/dl-de/by-2-0) - Base map.
- [Geoportal Berlin/ALKIS Berlin Gemeinde](https://fbinter.stadt-berlin.de/fb/wfs/data/senstadt/s_wfs_alkis_bezirk), [dl-de/by-2-0](https://www.govdata.de/dl-de/by-2-0) - Borders of Berlin and its districts.
- [Geoportal Berlin/Einwohnerdichte 2022 (Umweltatlas)](https://daten.berlin.de/datensaetze/einwohnerdichte-2022-umweltatlas-wms), [CC BY 3.0 DE Deed](https://creativecommons.org/licenses/by-sa/3.0/de/deed.de) - Population density.
- Schiavina M., Freire S., Carioli A., MacManus K. (2023): GHS-POP R2023A - GHS population grid multitemporal (1975-2030), European Commission, Joint Research Centre (JRC), PID: [http://data.europa.eu/89h/2ff68a52-5b5b-4a22-8f40-c41da8332cfe](http://data.europa.eu/89h/2ff68a52-5b5b-4a22-8f40-c41da8332cfe), [doi:10.2905/2FF68A52-5B5B-4A22-8F40-C41DA8332CFE](https://doi.org/10.2905/2FF68A52-5B5B-4A22-8F40-C41DA8332CFE) - Population density.

## Tools
- [Openrouteservice](https://openrouteservice.org/) for isochrone calculations. As it required way more requests than allowed by their API, I spun it up locally in a Docker container. See the corresponding directory for details.
- [QGIS](https://qgis.org/) for working with the WFS data from Geoportal Berlin and for processing raster images from the GHS-POP dataset.
- [Felt Tippercanoe](https://github.com/felt/tippecanoe) for vector tile generation. See [Martin Fleischmann's guide on creating a vector-based web map hosted on GitHub](https://martinfleischmann.net/how-to-create-a-vector-based-web-map-hosted-on-github/) (this project's index.html is mostly adopted from that instruction, too).
- Python, mostly [GeoPandas](https://geopandas.org/) for everything else.
