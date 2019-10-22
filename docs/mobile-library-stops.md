---
layout: default
title: Mobile library stops
description: Locations of mobile library stops and how when they are visited
---

### Definition

A mobile library stop is a location served at intervals by a mobile library van, and available for visiting for all members of the public. For example, this would exclude home delivery locations or locations that are otherwise private.

### Sample data row

| Organisation | Mobile name | Route | Community | Stop | Address | Postcode | GeoX | GeoY | Day | Arrival | Departure | Frequency | Start | End | Timetable |
| ------------ | ----------- | ----- | --------- | ---- | ------- | -------- | ---- | ---- | --- | ------- | --------- | --------- | ----- | --- | --------- |
| Somerset | Mobile | A | Brompton Regis | Wimbleball Lake | Wimbleball Lake, Brompton Regis | TA22 9NU | -3.47537 | 51.064823 | Tuesday | 10:05 | 10:20 | FREQ=WEEKLY;INTERVAL=4 | 2019-11-12 | | [Link](https://www.somerset.gov.uk/libraries-leisure-and-communities/libraries/library-facilities/mobile-library/) |

The full sample can be viewed at [Somerset mobile stops](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/somerset_mobile_library_stops.csv).

### Field notes

### Potential problems

- **Private stops**. In some cases mobile library services alternate between private stops (e.g. home visits) and public stops. This restricts them from publicising their routes. This dataset definition should encourage services to take the chance to publish only their public stops so that the data ccan be used for public information.
- **Co-ordinates**. Many services will not have co-ordinates (latitude and longitude) for their mobile library stops. These are a requirement of the dataset. However, collecting these can be done with mobile devices, so advice should be provided on easy ways of doing this.

### How the data could be used

The data in this format provides full timetable information for mobile library stops. It would be possible to create a national view of mobile libraries that displayed where they were at any time, and where a citizen's nearest stop was.

For an example usage see this [mobile library dashboard](https://www.mobilelibraries.org).

[Back](./)
