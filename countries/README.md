Data taken from [Natural Earth](https://www.naturalearthdata.com/).

Howto update:
1. Make sure [ogr2ogr](https://gdal.org/programs/ogr2ogr.html) is installed and available on the commandline
2. Download the 1:10m Cultural Vectors (Admin 0 – Countries) from [Natural Earth](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/) *We've taken the German POV here*
3. Unzip the downloaded file
4. run `ogr2ogr -select admin,iso_a3 -f geojson countries.geojson "$(find *.shp)"`
5. You will find the resulting geojson-file in `countries.geojson`
