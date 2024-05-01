# Natural Earth extract

The dataset uses a minimal subset of the [NaturalEarth](https://www.naturalearthdata.com/) 5.1 data set.

It reproduces the data set used in https://github.com/pka/mvt-benchmark

## Creation

Download NaturalEarth data and create GeoPackage files:

    just create-extracts

Import GeoPackage files into PostGIS database:

    just start-db
    just create-splitted-extracts
    just create-extracts-db

Create tiles:

    just seed-all

View tile map:

    just serve-merc
    xdg-open http://localhost:8080/assets/maplibre.html
