---
layout: default
title: Mobile library stops
description: Locations of mobile library stops and when they are visited
---

[&lt; Back to home](./)

### Definition

---

A mobile library stop is a location visited by a mobile library vehicle. It should be part of the public timetable.

### How the data can be collected

Library services will often already hold mobile library stops in spreadsheets. They may also be held in the Library Management System, but this is rarely the 'master' copy of the data.

The most likely method for compiling this data will be to rearrange existing spreadsheets or documents into this data format.

If starting from scratch, [this template file](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/templates/mobile_library_stops.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Organisation | Mobile name | Route | Community | Stop | Address | Postcode | GeoX | GeoY | Day | Type | Arrival | Departure | Frequency | Start | End | Exceptions | Timetable |
| ------------ | ----------- | ----- | --------- | ---- | ------- | -------- | ---- | ---- | --- | ---- | ------- | --------- | --------- | ----- | --- | ---------- | --------- |
| Somerset | Mobile | A | Brompton Regis | Wimbleball Lake | Wimbleball Lake, Brompton Regis | TA22 9NU | -3.47537 | 51.064823 | Tuesday | Public | 10:05 | 10:20 | FREQ=WEEKLY;INTERVAL=4 | 2019-11-12 |  |  | Link to webpage |

A full sample can be viewed at [Somerset mobile stops](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/mobile_library_stops_somerset.csv).

### Field notes

---

#### Type

This describes the type of stop. It should be one of the following values.

| Type | Description |
| ---- | ----------- |
| Public | The vast majority will be this type. A stop available to all members of the public |
| Private | In some situations it may be necessary to mark stops as Private. For example, home visits in the middle of mobile routes |
| Dynamic | Time set aside for stops where the time could be used dynamically by the mobile van. For example, to allow for request stops |
| Other | Any other situation where a stop is included in the timetable. This could be to include maintenance such as refuelling, or lunch breaks |

#### Frequency

This describes when the stop will be visited. This uses the [iCalendar RRule specification](https://icalendar.org/iCalendar-RFC-5545/3-8-5-3-recurrence-rule.html). This is an open standard for communicating when recurring events happen.

In the majority of the cases, mobile library stops are visited at weekly intervals. For example, every week is described as 'FREQ=WEEKLY;INTERVAL=1', every two weeks would be 'FREQ=WEEKLY;INTERVAL=2'. Stops may be visited at monthly intervals, by a named day of the week. For example, 'FREQ=MONTHLY;BYDAY=2MO', would mean the stop is visited on the second Monday of each month.

#### Start

This should be the first date at which the stop will be visited. It will then be possible to calculate future dates based upon the frequency field.

#### End

This field is optional, and describes the last date at which the stop will be visited. This could be used if timetables are planned for set periods in advance only.

#### Exceptions

These will be dates when the mobile library is not running for the particular stop. This will include public holidays where the mobile library would otherwise have visited the stop. It may also include maintenance days such as servicing and MOT. It could also be used to cancel stops at short notice when the mobile van is taken off the road. The format for this field is a comma separated list of dates. For example, **2019-12-26,2020-01-01** would exclude Christmas Day and New Years Day (a likely situation for a weekly mobile library).

#### Timetable

This field should provide a web address at which a citizen can find details of the mobile library stop, or the mobile library in general. This should not link to a PDF file, as these are less likely to fulfill [accessibility requirements](https://gds.blog.gov.uk/2018/07/16/why-gov-uk-content-should-be-published-in-html-and-not-pdf/).

### Potential problems

---

#### Coordinates (GeoX and GeoY)

Some services will not currently hold coordinates (latitude and longitude) for their stops. These are a requirement of this dataset, so it may be that advice is also provided for options of how to collect these.

### How the data is updated

---

Updates to the data should be made when there are any changes to the stops. The data can then be revalidated and published to replace the previous data.

### How the data could be used {#usage}

---

#### Locally

Current mobile library information provided online is inaccessible, hard to understand, and difficult to maintain. Many mobile library timetables are still published only in PDF format, and include accessibility mistakes such as using colour coding to convey information. PDF is a poor format in general for accessibililty [as detailed on GOV.UK](https://www.gov.uk/guidance/how-to-publish-on-gov-uk/accessible-pdfs). It is now a legal requirement to address these issues.

By collecting and publishing data for mobile libraries, the task of presenting this information can be shared and tools made available to services to display the information.

- The option to embed HTML stop lists on local authority websites could also be provided from the data
- A single, accessible format for PDF timetables could be automatically generated from the data.

#### Nationally

This data provides full timetable information for mobile library stops. It will be possible to create a national view of mobile libraries showing where they are at any time, and where a citizen's nearest stop is.

For an example usage see the [mobile library dashboard](https://www.mobilelibraries.org).

<figure>
    <img src="{{site.url}}/images/mobile_library_stops_somerset.png" alt="Somerset mobile library on a map"/>
    <figcaption>The Somerset Mobile library on it's route towards Higher Chillington stop.</figcaption>
</figure>

Having this data also allows us to spot opportunities for collaboration that were previously difficult for anyone to manually detect.

For example, with mobile library stops mapped we can see stops that are either side of the borders of local authorities. By displaying visit dates we can then also see where these could allow for collaboration. Such as one authority visiting another's mobile library stop when in the area.

We can also use route information to show where a neighbouring mobile library may pass by or through a community within a neighbouring local authority.

### Future enhancements

---

#### Real-time GPS data

A further real-time option would be to include coordinates of the current position of the mobile library vehicle. This would provide the opportunity to provide estimated arrival times, and alert users to delays.

---

[&lt; Back to home](./)
