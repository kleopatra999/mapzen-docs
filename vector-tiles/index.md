Mapzen provides a free & open vector tile service for OpenStreetMap base layer data, with worldwide coverage updated daily, available in GeoJSON, TopoJSON, and binary data [formats](#formats).

Making OpenStreetMap and other open geo data more accessible to developers is central to Mapzen’s mission. We don’t want you to have to struggle with installing PostGIS, building osm2pgsql, or downloading a planet file to start playing with OSM data.

Vector tiles make real-time rendering possible by sending the underlying OSM geometry and tags directly to the client, whether that’s a browser or a native mobile app. Check out [Tangram, our work-in-progress WebGL rendering library](https://mapzen.com/tangram) for an example.

But we also believe that vector tiles will enable other, yet-to-be-invented types of OpenStreetMap-powered applications. Use this service to experiment with ideas!

Please note: this service is in active development and is subject to change! Questions, feedback, requests? [Let us know](https://github.com/mapzen/vector-datasource/issues).

# How it Works
Vector tiles are served by clipping geometries to the tile bounding box, and then simplified to match the zoom level (to avoid unnecessary complexity at lower zoom levels). These geometries and features are also further processed to facilitate styling.

This is based on the work of [Michal Migurski](http://mike.teczno.com/), and extends his [OSM.US-hosted vector tile service](http://openstreetmap.us/~migurski/vector-datasource/) with additional data and format support.

If you are interested in setting up your own version of this service, look at our [installation instructions](https://github.com/mapzen/vector-datasource/wiki/Mapzen-Vector-Tile-Service), or you can also try this [Vagrant VM](https://github.com/mapzen/vagrant-tiles), which will additionally set up other tile components as well. You may also be interested in our [Metro Extracts](https://mapzen.com/metro-extracts), which provide weekly, city-sized chunks of OSM data in several formats for over 200 cities.


