---
layout: default
title: Mobile library stops
description: Locations of mobile library stops and when they are visited
---

[&lt; Back to home](./)

### Definition

A mobile library stop is a location served at intervals by a mobile library van. It should be open to all members of the public. For example, this would exclude home delivery locations, or locations that have other access restrictions (such as school-only).

### Collection method

1. Manually compile data. May include collecting stop coordinates using online map tools or GPS devices.
2. Data validation
3. Publish

### How the data is updated

Updates to the data should be made as soon as any changes are required. The data can then be revalidated and published to replace the previous data.

### Sample data row

| Organisation | Mobile name | Route | Community | Stop | Address | Postcode | GeoX | GeoY | Day | Arrival | Departure | Frequency | Start | End | Timetable |
| ------------ | ----------- | ----- | --------- | ---- | ------- | -------- | ---- | ---- | --- | ------- | --------- | --------- | ----- | --- | --------- |
| Somerset | Mobile | A | Brompton Regis | Wimbleball Lake | Wimbleball Lake, Brompton Regis | TA22 9NU | -3.47537 | 51.064823 | Tuesday | 10:05 | 10:20 | FREQ=WEEKLY;INTERVAL=4 | 2019-11-12 | | [Link](https://www.somerset.gov.uk/libraries-leisure-and-communities/libraries/library-facilities/mobile-library/) |

The full sample can be viewed at [Somerset mobile stops](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/somerset_mobile_library_stops.csv).

### Field notes

### Frequency 

The frequency field is used to describe when the stop will be visited. This uses a data format documented at the [iCalendar RRule specification](https://icalendar.org/iCalendar-RFC-5545/3-8-5-3-recurrence-rule.html). This is an open standard for communicating when a recurring calendar event happens.

In the majority of the cases, mobile library stops are visited at variations of weekly frequencies. For example, every two weeks is described as 'FREQ=WEEKLY;INTERVAL=2'. In some cases stops are monthly by a named day of the week. For example 'FREQ=MONTHLY;BYDAY=2MO', describes stops that visited eachsecond Monday of each month.

### Start

The start date should be the first date at which the stop will be visited. It will then be possible to calculate future dates based upon the frequency field.

### End

The end date is optional, and describes the last date at which the stop will be visited. This could be used if timetables are planned for set periods only.

### Timetable

The timetable URL should provide a web address at which a citizen can find details of the mobile library stop. This should not link to a PDF file as these are less likely to fulfill accessibility requirements.

### Potential problems

#### Private stops 

In some cases mobile library routes alternate between public and private stops (e.g. home visits). This currently restricts them from publicising their routes. This dataset should encourage services to take the chance to publish only their public stops, so that the data can be used to provide that public information.

#### Co-ordinates

Many services will not currently hold co-ordinates (latitude and longitude) for their mobile library stops. These are a requirement of this dataset so it may be that advice should be documented for ways to collect these.

### How the data could be used

This data provides full timetable information for mobile library stops. It would be possible to create a national view of mobile libraries that displayed where they were at any time, and where a citizen's nearest stop was.

For an example usage see this [mobile library dashboard](https://www.mobilelibraries.org).

### Future enhancements

#### Non-public stops

Some services publish details of mobile libraries such as lunch breaks, or the time they leave and arrive at the depot. This would add interesting possibilities for providing more information about how the mobile library is operated, with potential for further route optimisation from the data.

#### Cancellations

If the data were updated in 'real-time' it would be possible to use this standard for communicating late-notice cancellations of the service.

#### Real-time GPS data

A further real-time data option would be to include co-ordinates of the current position of the mobie library van. This would provide the opportunity to provide estimated arrival times, and to alert users to delays.

[&lt; Back to home](./)
