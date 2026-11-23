---
layout: default
title: Mobile library stops
description: Locations of mobile library stops and when they are visited
---

[< Back to home](./)

### Definition

---

A mobile library stop is a location visited by a mobile library vehicle. It should be part of the public timetable.

### How the data can be collected

Library services will often already hold mobile library stops in spreadsheets. They may also be held in the Library Management System, but this is rarely the 'master' copy of the data.

The most likely method for compiling this data will be to rearrange existing spreadsheets or documents into this data format.

If starting from scratch, [this template file](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/templates/mobile_library_stops.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| local_authority | local_authority_code | mobile_name | route | community | stop | address | postcode | geox | geoy | day | type | arrival | departure | frequency | start | end | exceptions | timetable |
| --------------- | -------------------- | ----------- | ----- | --------- | ---- | ------- | -------- | ---- | ---- | --- | ---- | ------- | --------- | --------- | ----- | --- | ---------- | --------- |
| Somerset | E06000066 | Mobile | A | Brompton Regis | Wimbleball Lake | Wimbleball Lake, Brompton Regis | TA22 9NU | -3.47537 | 51.064823 | Tuesday | Public | 10:05 | 10:20 | FREQ=WEEKLY;INTERVAL=4 | 2019-11-12 | | | https://www.somerset.gov.uk/libraries-leisure-and-communities/libraries/library-facilities/mobile-library/ |

A full sample can be viewed at [Somerset mobile stops](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/mobile_library_stops_somerset.csv).

### Field notes

---

#### Local authority (`local_authority`)

The local authority responsible for the library service. In the UK, this should be the local authority name as listed on gov.uk (see [common field standards](./common-fields)).

#### Local authority code (`local_authority_code`)

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E06000066` for Somerset). This links directly to the parent [library services dataset](./library-services).

#### Mobile name (`mobile_name`)

A name or identifier for the mobile library vehicle or service point (e.g. 'Mobile A', 'Supermobile').

#### Type (`type`)

This describes the type of stop. It should be one of the following values.

| Type | Description |
| ---- | ----------- |
| Public | The vast majority will be this type. A stop available to all members of the public |
| Private | In some situations it may be necessary to mark stops as Private. For example, home visits in the middle of mobile routes |
| Dynamic | Time set aside for stops where the time could be used dynamically by the mobile van. For example, to allow for request stops |
| Other | Any other situation where a stop is included in the timetable. This could be to include maintenance such as refuelling, or lunch breaks |

#### Frequency (`frequency`)

This describes when the stop will be visited. This uses the [iCalendar RRule specification](https://icalendar.org/iCalendar-RFC-5545/3-8-5-3-recurrence-rule.html). This is an open standard for communicating when recurring events happen.

In the majority of the cases, mobile library stops are visited at weekly intervals. For example, every week is described as 'FREQ=WEEKLY;INTERVAL=1', every two weeks would be 'FREQ=WEEKLY;INTERVAL=2'. Stops may be visited at monthly intervals, by a named day of the week. For example, 'FREQ=MONTHLY;BYDAY=2MO', would mean the stop is visited on the second Monday of each month.

#### Start (`start`)

This should be the first date at which the stop will be visited. It will then be possible to calculate future dates based upon the frequency field.

#### End (`end`)

This field is optional, and describes the last date at which the stop will be visited. This could be used if timetables are planned for set periods in advance only.

#### Exceptions (`exceptions`)

Comma separated list of ISO-8601 dates (e.g. YYYY-MM-DD) on which this stop is not visited (for example bank holidays or maintenance days).

#### Timetable (`timetable`)

Link to a webpage, timetable PDF, or service webpage for the route or stop.

### Potential problems

---

#### Coordinates (`geox` and `geoy`)

Some services will not currently hold coordinates (longitude and latitude) for their stops. These are recommended for this dataset to allow mapping and proximity searching.

### How the data is updated

---

Updates to the data should be made when there are any changes to timetables or stops. The data can then be revalidated and published to replace the previous data.

---

[< Back to home](./)
