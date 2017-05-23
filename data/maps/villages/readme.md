# Georgian villages

## How was the data extracted?

1. Data was extracted from [overpass-turbo](http://overpass-turbo.eu/) using following query  

```
area[name="საქართველო"];
(node["place"~"village"](area););
out;`
```

2. Then it was exported as `geoJSON` to `export.geojson` file

3. Then with help of `d3.js` , we have assigned sub region to each village, and exported json as a csv
