Nodetiles-PostGIS
=============

Nodetiles-PostGIS is a data source for Nodetiles that allows you to load and render geographic data from a PostGIS database (PostGIS is Postgres with geographic additions).

Quick Start
-----------

```
/* Set up the libraries */
var nodetiles = require('nodetiles-core');
var PostGIS = nodetiles.datasources.GeoJson;
    
/* Create your map context */
var map = new nodetiles.Map({
    projection: "EPSG:4326" // set the projection of the map
});

/* Add some data from PostGIS! */
map.addData(new PostGIS({
  name: "world",
  path: __dirname + '/countries.geojson', 
  projection: "EPSG:900913"
}));
```

Copyright
---------
Copyright (c) 2012-2013 Code for America. See LICENSE for details.
