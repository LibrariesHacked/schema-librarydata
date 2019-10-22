---
layout: default
title: Mobile library stops
description: Locations of mobile library stops and when they are visited
---

[&lt; Back to home](./)

### Definition

---

A mobile library stop is a location visited by a mobile library vehicle. It should be open to all members of the public. This will exclude locations that are for home deliveries, or locations that have other access restrictions (such as school-only).

### Sample data row

| Organisation | Mobile name | Route | Community | Stop | Address | Postcode | GeoX | GeoY | Day | Arrival | Departure | Frequency | Start | End | Timetable |
| ------------ | ----------- | ----- | --------- | ---- | ------- | -------- | ---- | ---- | --- | ------- | --------- | --------- | ----- | --- | --------- |
| Somerset | Mobile | A | Brompton Regis | Wimbleball Lake | Wimbleball Lake, Brompton Regis | TA22 9NU | -3.47537 | 51.064823 | Tuesday | 10:05 | 10:20 | FREQ=WEEKLY;INTERVAL=4 | 2019-11-12 | | [Link](https://www.somerset.gov.uk/libraries-leisure-and-communities/libraries/library-facilities/mobile-library/) |

A full sample can be viewed at [Somerset mobile stops](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/somerset_mobile_library_stops.csv).

### Field notes

---

#### Frequency 

This describes when the stop will be visited. This uses the [iCalendar RRule specification](https://icalendar.org/iCalendar-RFC-5545/3-8-5-3-recurrence-rule.html). This is an open standard for communicating when recurring events happen.

In the majority of the cases, mobile library stops are visited at weekly intervals. For example, every week is described as 'FREQ=WEEKLY;INTERVAL=1', every two weeks would be 'FREQ=WEEKLY;INTERVAL=2'. In some cases stops are visited monthly by a named day of the week. For example, 'FREQ=MONTHLY;BYDAY=2MO', would mean the stop is visited on the second Monday of each month.

#### Start

This should be the first date at which the stop will be visited. It will then be possible to calculate future dates based upon the frequency field.
 
#### End

This field is optional, and describes the last date at which the stop will be visited. This could be used if timetables are planned for set periods in advance only.

#### Timetable

This field should provide a web address at which a citizen can find details of the mobile library stop, or the mobile library in general. This should not link to a PDF file, as these are less likely to fulfill [accessibility requirements](https://gds.blog.gov.uk/2018/07/16/why-gov-uk-content-should-be-published-in-html-and-not-pdf/).

### Potential problems

---

#### Private stops 

In some cases mobile library routes alternate between public and private stops (e.g. home visits). This currently restricts them from publicising their routes. This dataset should encourage services to take the chance to publish only their public stops, so that the data can be used to provide that public information.

#### Coordinates

Many services will not currently hold coordinates (latitude and longitude) for their mobile library stops. These are a requirement of this dataset so it may be that advice should be documented for ways to collect these.

### How the data is updated

---

Updates to the data should be made as soon as there are any changes to the stops. The data can then be revalidated and published to replace the previous data.

### How the data could be used

---

This data provides full timetable information for mobile library stops. It would be possible to create a national view of mobile libraries that displayed where they were at any time, and where a citizen's nearest stop was.

For an example usage see this [mobile library dashboard](https://www.mobilelibraries.org).

### Future enhancements

---

#### Vehicle stops

Some services publish details such as lunch breaks, or the time mobile vehicles leave and arrive at the depot. This could add interesting possibilities for providing more information about how the mobile library is operated.

#### Cancellations

If the data were updated in 'real-time' it would be possible to add last-minute cancellations of the service.

#### Real-time GPS data

A further real-time data option would be to include coordinates of the position of the mobile library vehicle. This would provide the opportunity to provide estimated arrival times, and to alert users to delays.

---

[&lt; Back to home](./)
