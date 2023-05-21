Data taken from [Natural Earth](https://www.naturalearthdata.com/).

## `countries.geojson`
this is countries with ISO_A3 code included

Howto update:
1. Make sure [ogr2ogr](https://gdal.org/programs/ogr2ogr.html) is installed and available on the commandline
2. Download the 1:10m Cultural Vectors (Admin 0 – Countries) from [Natural Earth](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/) *We've taken the German POV here*
3. Unzip the downloaded file
4. run `ogr2ogr -select admin,iso_a3 -f geojson countries.geojson "$(find *.shp)"`
5. You will find the resulting geojson-file in `countries.geojson`

## `countries.de.geojson`
this is countries with german name (NAME_DE) included

Howto update:
1. Make sure [ogr2ogr](https://gdal.org/programs/ogr2ogr.html) is installed and available on the commandline
2. Download the 1:10m sovereignty (Admin 0 – Details) from [Natural Earth](https://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-0-details/)
3. Unzip the downloaded file
4. run `ogr2ogr -select NAME_DE -f geojson -t_srs crs:84 countries.de.geojson ne_10m_admin_0_sovereignty.shp`
5. You will find the resulting geojson-file in `countries.de.geojson`
