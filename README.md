# Where can we get data about Sheffield?

Sheffield Council's Socrata platform: https://data.sheffield.gov.uk/ (it's rubbish, let me know if you find anything useful)

I found "neighbourhoods" on data.sheffield.gov.uk https://data.sheffield.gov.uk/dataset/Neighbourhoods-Sheffield/wwma-jstu No idea what they're used for.

Deprivation Indices https://www.gov.uk/government/statistics/english-indices-of-deprivation-2015

Outlines for LSOA and other geographies from Census https://borders.ukdataservice.ac.uk//easy_download.html


## A note about coordinates

Much of the raw geographic data for the UK, such as the LSOA boundaries published by the census,
are specified as coordinates on [The National Grid (Ordnance Survey)](https://www.ordnancesurvey.co.uk/resources/maps-and-geographic-resources/the-national-grid.html).
In this system points are specified as a number of metres east, _the easting_, and a number of number north, _the northing_,
of the National Grid's false origin.
The false origin is Southwest of Scilly, meaning that all points in Great Britain have positive eastings and northings.

Sheffield is entirely within Great Britain,
meaning that we do not have to deal with the added complication of using the Irish Grid system
that is shared by Ireland and Northern Ireland.

Most web and other mapping systems use a latitude and longitude system based on [WGS84 (World Geodetic System 1984)](https://en.wikipedia.org/wiki/World_Geodetic_System#WGS84) shared with GPS.
This requires conversion.
