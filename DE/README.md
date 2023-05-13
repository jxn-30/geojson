Data taken from [Bundesamt für Kartographie und Geodäsie](https://gdz.bkg.bund.de/index.php/default/open-data/nuts-gebiete-1-250-000-stand-31-12-nuts250-31-12.html)

Data version: 31.12.2022
Data precision: 1:250000

Level 0: Germany
Level 1: Bundesländer
Level 2: überwiegend Regierungsbezirke
Level 3: kreisfreie Städte und Landkreise

Data has been downloaded in `.shp` format. Conversion (requires [ogr2ogr](https://gdal.org/programs/ogr2ogr.html)):
* `ogr2ogr -f geojson -t_srs crs:84 level1.geojson NUTS250_N1.shp`
* `ogr2ogr -f geojson -t_srs crs:84 level2.geojson NUTS250_N2.shp`
* `ogr2ogr -f geojson -t_srs crs:84 level3.geojson NUTS250_N3.shp`

Data is under following Copyright:
© GeoBasis-DE / [BKG](http://www.bkg.bund.de) 2023 
