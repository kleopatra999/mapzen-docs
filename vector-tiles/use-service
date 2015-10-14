# Use the vector tile service

Now, just plug that api key into this URL pattern to get started:

`http://vector.mapzen.com/osm/{layers}/{z}/{x}/{y}.{format}?api_key={api_key}`

The [OpenStreetMap Wiki](http://wiki.openstreetmap.org/wiki/Slippy_map_tilenames) has more information on this url scheme.

Here’s a sample tile in GeoJSON:

http://vector.mapzen.com/osm/all/16/19293/24641.json?api_key={api_key}

Layers to return can specified as `all`, or as one or more layer names separated by commas, e.g.:

`buildings`: http://vector.mapzen.com/osm/buildings/16/19293/24641.json?api_key={api_key}

`earth,landuse`: http://vector.mapzen.com/osm/earth,landuse/16/19293/24641.json?api_key={api_key}

## Multiple layers in GeoJSON
When requesting multiple layers in GeoJSON, a dictionary of FeatureCollections will be returned, keyed by layer name, e.g.:

```
{
   "earth": {
      "type":"FeatureCollection",
      "features": [...],
      ...
   },
   "landuse": {
      "type":"FeatureCollection",
      "features": [...],
      ...
   }
}
```

When requesting a single layer, the response will simply be a single FeatureCollection, without any layer name prefix, e.g.:

```
{
   "type":"FeatureCollection",
   "features": [...],
   ...
}
```

The currently supported binary formats can handle single vs. multiple layers directly.
