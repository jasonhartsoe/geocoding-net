# Generic C# GeoCoding API #

**This project is now hosted on [GitHub](https://github.com/chadly/Geocoding.net)**

Includes a portable GeoCoding domain model along with a generic IGeoCoder service interface.  Current implementations include:

  * [Google Maps](http://code.google.com/apis/maps/)
  * [Yahoo! PlaceFinder](http://developer.yahoo.com/geo/placefinder/)
  * [Bing Maps (aka Virtual Earth)](http://www.microsoft.com/maps/)

The API returns latitude/longitude coordinates and normalized address information.  This can be used to perform address validation, real time mapping of user-entered addresses, distance calculations, and much more.

**Simple Example**

```
IGeoCoder geoCoder = new GoogleGeoCoder("my-api-key");
Address[] addresses = geoCoder.GeoCode("123 Main St");
```

It can also be used to return address information from latitude/longitude coordinates (aka reverse geocoding):

```
IGeoCoder geoCoder = new YahooGeoCoder("my-app-ID");
Address[] addresses = geoCoder.ReverseGeoCode(38.8976777, -77.036517);
```