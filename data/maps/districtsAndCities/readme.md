# Georgian district's and cities 

## How was the data extracted?

1. Data was extracted from [overpass-turbo](http://overpass-turbo.eu/) using following query  

```
area[name="საქართველო"];
(node["place"~"town|city"](area););
out;
```

2. Then it was exported as `geoJSON` to `export.geojson` file

3. Then we have converted this geoJSON to csv using <code><a href="https://stedolan.github.io/jq">jq (command-line JSON processor)</a> </code> with  command  
  `
    jq -r '.features[]|[.id, .properties."name:ka", .properties."name:en", .properties."population", .geometry.coordinates[0], .geometry.coordinates[1]]|@csv' export.geojson
  `
