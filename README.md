## Delaware Schools Pelias Importer

This package is an example app for importing 3rd party data into a Pelias Elasticsearch instance.  It uses the [Who's on First bundles](https://whosonfirst.mapzen.com/bundles/) for admin lookup (filling in city/county/state/etc for addresses).  

`index.js` is hardcoded to request the list of [Delaware Schools](https://data.delaware.gov/api/views/wky5-77bt/rows.csv?accessType=DOWNLOAD) from [Delaware Open Data](https://data.delaware.gov/).

To run:

```javascript
npm i
npm start
```

When done, 218 schools should have been added to the Elasticsearch index.  Execute `GET /pelias/venue/_search?pretty=true&q=*:*` in sense to confirm.  
