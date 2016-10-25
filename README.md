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
var geoip = require('geoip-lite');

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

    $ npm install geoip-lite

### 2. get the datafiles

Then download the city data files from https://github.com/bluesmoon/node-geoip/tree/master/data
You need to get `geoip-city.dat` and `geoip-city-names.dat` and put them into the `data/` directory
of this package.

You could also run `npm run-script updatedb` to do this automatically.

**NOTE** that this requires a lot of RAM.  It is known to fail on on a Digital Ocean or AWS micro instance.
There are no plans to change this.  `geoip-lite` stores all data in RAM in order to be fast.


