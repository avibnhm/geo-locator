Geo-Locator
==========

A native NodeJS API for the GeoLite data from MaxMind.

This product includes GeoLite data created by MaxMind, available from http://maxmind.com/

introduction
------------

Extend Geoip-lite by enabling direct update from main module


synopsis
--------

```javascript
var geoip = require('geo-locator');

var ip = "207.97.227.239";
var geo = geoip.lookup(ip);

console.log(geo);
{ range: [ 3479299040, 3479299071 ],
  country: 'US',
  region: 'CA',
  city: 'San Francisco',
  ll: [37.7484, -122.4156] }
```

installation
------------
### 1. get the library

    $ npm install geo-locator

### 2. get the datafiles

Then download the city data files from https://github.com/bluesmoon/node-geoip/tree/master/data
You need to get `geoip-city.dat` and `geoip-city-names.dat` and put them into the `data/` directory
of this package.

You could also run `geoip.updateMaxmindeDB` to do this automatically.




