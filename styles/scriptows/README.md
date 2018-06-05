
# Import process

Add osm_tags_... columns with `node ./extend.js myfile.gdb`, it will create files in extended folder.

Import extended layers to postgres wit `node ./import.js`.

`npm install` is required to download related packages and remove remove-placeholder.txt files

# extend.js arguments (optional)

```
node ./extend.js fileSrc targetSrs srcSrs ogr2ogr
```
- fileSrc: name of file with extension, must be placed in ./src folder, default 'layers.gdb'
- targetSrs: srs of destination, default 'EPSG:3857'
- srcSrs: srs of source, default 'EPSG:4326'
- ogr2ogr: bin path or 'ogr2ogr', default 'C:/OSGeo4W64/bin/ogr2ogr'

# import.js arguments (optional)

```
node ./import.js dbname host port user password ogr2ogr
```
- dbname: name of database with postgis extension, default 'ows'
- host: host of postegres, default 'localhost'
- host: port of postegres, default '5432
- user: username, default 'postgres'
- password: password, default 'postgres'
- ogr2ogr: bin path or 'ogr2ogr', default 'C:/OSGeo4W64/bin/ogr2ogr'
---
`node v6.0.0`

`ogr2ogr GDAL 2.2.4, released 2018/03/19`

`postgres (PostgreSQL) 10.1`