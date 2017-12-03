# Where can we get data about Sheffield?

Sheffield Council's Socrata platform: https://data.sheffield.gov.uk/ (it's rubbish, let me know if you find anything useful)

I found "neighbourhoods" on data.sheffield.gov.uk https://data.sheffield.gov.uk/dataset/Neighbourhoods-Sheffield/wwma-jstu No idea what they're used for.

Deprivation Indices https://www.gov.uk/government/statistics/english-indices-of-deprivation-2015

Postcodes (for all UK) http://geoportal.statistics.gov.uk/datasets/ons-postcode-directory-latest-centroids
User manual is here: http://geoportal.statistics.gov.uk/datasets?q=ONSPD%20User%20Guide%20(November%202017)&sort=name

# Boundaries and so on

Outlines for LSOA and other geographies from Census https://borders.ukdataservice.ac.uk//easy_download.html

and the UK government's Geoportal: http://geoportal.statistics.gov.uk/

MySociety's mapit project has boundaries for Sheffield and its various subdivisions. https://mapit.mysociety.org/area/2537.html
Generally in WKT, KML, and GeoJSON formats.

A nice person on the internet has made lots of the boundaries available in other formats.
Here are the LSOA for each Local Authority Districts in England: https://github.com/martinjc/UK-GeoJSON/tree/master/json/statistical/eng/lsoa_by_lad

Sheffield has GSS code `E08000019`.

Geoportal has [boundaries all the Local Authority Districts (LAD) in the UK](http://geoportal.statistics.gov.uk/datasets/local-authority-districts-december-2016-full-clipped-boundaries-in-the-uk-wgs84).
Using this data, we can compute a latitude/longitude based bounding box for Sheffield:

Longitude: -1.802 to -1.324

Latitude: 53.304 to 53.504

(expanding the box to round the figures to 3 decimal places)

## A note about coordinates

Much of the raw geographic data for the UK, such as the LSOA boundaries published by the census,
are specified as coordinates on [The National Grid (Ordnance Survey)](https://www.ordnancesurvey.co.uk/resources/maps-and-geographic-resources/the-national-grid.html).
In this system points are specified as a number of metres east, _the easting_, and a number of number north, _the northing_,
of the National Grid's false origin.
The false origin is Southwest of Scilly, meaning that all points in Great Britain have positive eastings and northings.

Sheffield is entirely within Great Britain,
meaning that we do not have to deal with the added complication of using the Irish Grid system
that is shared by Ireland and Northern Ireland.

Sheffield lies between 413km and 446km east of the false origin, and between 378km and 401km north.
Thus generally eastings and northings for points in Sheffield will look like
4XXxxx for an easting and 3XXxxx for a northing.

Most web and other mapping systems use a latitude and longitude system based on [WGS84 (World Geodetic System 1984)](https://en.wikipedia.org/wiki/World_Geodetic_System#WGS84) shared with GPS.
This requires conversion.
