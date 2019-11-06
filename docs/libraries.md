---
layout: default
title: Libraries
description: Library location opening hours and contact details
---

[&lt; Back to home](./)

### Definition

---

A library is a static service point which allows access to library services for the general public. This does not include mobile library services which are covered in a separate dataset.

### How the data can be collected

---

Manual collection. Library services will be able to use the [library locations survey 2016](https://www.gov.uk/government/publications/public-libraries-in-england-basic-dataset) as a starting point, which includes similar fields.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/libraries.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Library name | Address 1 | Address 2 | Address 3 | Postcode | Unique Property Reference Number | Statutory | Type of Library | Year opened | Year closed | Monday hours | Tuesday hours | Wednesday hours | Thursday hours | Friday hours | Saturday hours | Sunday hours | Special hours | Colocated | Colocated with | Notes | URL | Email address |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| Plymouth  | Crownhill | Cross Park Road | Crownhill | | PL6 5AN | 100041062012 | Yes | LAL | 1991 | | 08:30-18:00| 08:30-18:00 | 08:30-18:00 | 08.30-20:00 | 08:30-18:00 | 09:00-17:00 | | | No | | | https://www.plymouth.gov.uk/libraries/findlibraryandopeninghours/crownhilllibrary | library@plymouth.gov.uk

A full sample can be viewed at [Plymouth libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/libraries_plymouth.csv).

### Field notes

---

#### Statutory

All statutory libraries should be listed. For libraries that are not statutory it is up to the individual service as to whether they are included.

#### Type of library

The type of library is a code that describes how the library is run.

| Code | Title | Description |
| ---- | ----- | ----------- |
| LAL | Local authority library | Library building funded, run and managed by local authority staff |
| LAL- | Local authority library (-) | As LAL, but unstaffed, for example, a book drop |
| CL | Commissioned library | Running of the library building/service has been transferred from the council to a separate trust or organisation. The local authority are still accountable for the service.|
| CRL | Community run library | Library with some level of ongoing support from the council. Work according to a joint agreement such as a Service Level Agreement, Memorandum of Understanding or contract. Staff are volunteers, but some form of support is available. May or may not be counted as part of the statutory service. |
| IL | Independent library | Library that has been transferred to the management of a non local authority body, either community group or third party, which is outside the local authority network. |

#### Year opened/closed

These columns should allow for new libraries, closures, and replacement libraries to be recorded.

#### Opening hours

Currently, opening hours should be all hours in which the library is open and available to all members of the public.

There is a column for each day. Hours are in 24 hour clock and include start and end e.g. **09:00-17:00**. If there are multiple opening hours in a day (e.g. a lunch break) these can be separated by commas e.g. **09:00-12:00,13:00-17:00**.

This is a format used by Google for listing opening hours. For more info see [these Google support pages](https://support.google.com/business/answer/3370250?#hours)

#### Special hours

This column provides a means for adding dates that have special changes to hours. This could be public holidays when the library is closed. The format is to specify the date, include a colon, and then the opening hours. Separate different entries with commas. For example, **2019-12-25: X, 2019-12-27: 10:00-13:00** would signify that the library is closed on the 25th December, and open from 10am to 1pm on the 27th December.

For more info see [these Google support pages](https://support.google.com/business/answer/6303076).

#### Unique property reference number

Unique property refence numbers (UPRNs) are administered centrally to local authorities. These are then used by the adddress custodians within local authorities when creating new properties, and are assigned to the property until demolition. For more info see these [UPRN pages on the GeoPlace website](https://www.geoplace.co.uk/addresses/uprn).

If you do not know the UPRNs of your library it is likely that the Geographic Information System (GIS) department will know, or the street naming and numbering department.

### Potential problems

---

#### UPRN

Excel can tend to be tricky when holding big numbers, and it may transform them to scientific notation when exporting to CSV format. UPRNs are also difficult as they are often held as a single number e.g. '199356', but are sometimes stored as 'zero padded' to ensure they are all the same length e.g. '00000199356'. We will likely get a mix of both but this should not matter.

### How the data is updated

---

Each service can maintain a single data file that is updated whenever the library details change, including changes to opening hours. As the data contains closed libraries, there is no need to remove these if a library is closed, the file can be updated by adding the year of closure. If there are new libraries, they can be added as an additional row.

### How the data could be used

---

Accurate location data on libraries is useful to analyse library provision, especially at a local level. For example, the [Plymouth Library Finder](https://plymouth.librarydata.uk) uses location data to assess the population within walking, cycling, or driving distance of a library and compare these visually.

<figure>
    <img src="{{site.url}}/images/libraries_plymouth.png" alt="Displaying a map with Plymouth Central Library at the centre and walking travel distances around it"/>
    <figcaption>Population within 5 minute walking intervals around Plymouth Central Library.</figcaption>
</figure>

The application also uses opening hours to show libraries open at the current time, and event data to search for libraries that host certain types of events. All these aspects of data are proposed for this core schema, and the tool could be updated to a national one.

### Future enhancements

---

#### Staff and unstaffed hours

Many libraries will have a mix of 'types' of opening hours, often when the library is accessible by using a library card and PIN at times when there are no staff. This can be described in different ways, such as extended access.

Different ways of handling these hours could be:

1. Separate out staffed/non-staffed into separate columns
2. Decide on set guidance about what hours should be included (e.g. the opening hours MUST be staffed hours where the building is open to all)
3. Leave it up to the services to decide what hours to use, but encourage use of the notes field for additional details (e.g. a service may say "Our opening hours include extended access use, for which members must...'" (edited)

Before deciding on this, more research should be conducted with a wider group of services. It will likely be important to capture additional information about unstaffed hours, such as:

- Who is able to access
- Training or authorisation required for access
- Facilities available during these hours

#### Library floor space and building

Adding data about the library building would give a useful context to the library, particularly as there can be a big difference between the facilities offered by a central library to a branch library. Some indicative data could be available through Ordnance Survey, as the UPRN identifier for the building would allow us to lookup building footprint and height.

---

[&lt; Back to home](./)
