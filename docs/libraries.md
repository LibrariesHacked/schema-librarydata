---
layout: default
title: Libraries
description: Library location opening hours and contact details
---

[&lt; Back to home](./)

### Definition

---

A library is a static service point which provides access to library services for the general public. This does not include mobile libraries, which are covered separately.

### How the data can be collected

---

Library services will be able to use the [library locations survey 2016](https://www.gov.uk/government/publications/public-libraries-in-england-basic-dataset) as a starting point, which includes similar fields.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/libraries.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Library name | Address 1 | Address 2 | Address 3 | Postcode | Statutory | Type of Library | Year opened | Year closed | Monday staffed hours | Tuesday staffed hours | Wednesday staffed hours | Thursday staffed hours | Friday staffed hours | Saturday staffed hours | Sunday staffed hours | Monday unstaffed hours | Tuesday unstaffed hours | Wednesday unstaffed hours | Thursday unstaffed hours | Friday unstaffed hours | Saturday unstaffed hours | Sunday unstaffed hours |Special hours | Co-located | Co-located with | Notes | URL | Email address |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| Plymouth  | Crownhill | Cross Park Road | Crownhill | | PL6 5AN | Yes | LAL | 1991 | | 08:30-18:00| 08:30-18:00 | 08:30-18:00 | 08.30-20:00 | 08:30-18:00 | 09:00-17:00 | | | | | | | | | | No | | | https://www.plymouth.gov.uk/libraries/findlibraryandopeninghours/crownhilllibrary | library@plymouth.gov.uk

An example for an earlier version of this dataset  can be viewed at [Plymouth libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/libraries_plymouth.csv).

### Field notes

---

#### Library name

You should list all libraries managed by your service. Independent libraries such as community-managed are not expected to be included.

If however you are updating the dataset and a library that used to be listed as managed by your service has since become independent, we recommend you still include it. In this case use the Type of library as IL for Independent Library. You may then omit this library from your list in future updates.

#### Statutory

All statutory libraries should be listed. For libraries that are not statutory it is up to the service whether to include them.

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

#### Staffed hours

Staffed hours are the hours during which individuals with responsibility for library services are present and are able to assist visitors.

There is a column for each day. Hours are in 24-hour clock and include start and end e.g. **09:00-17:00**. If there are multiple opening hours in a day these can be separated by commas e.g. **09:00-12:00,13:00-17:00** would accommodate a lunch break.

This is a format used by Google for listing opening hours. For more info see [these Google support pages](https://support.google.com/business/answer/3370250?#hours).

#### Unstaffed hours

Unstaffed hours are the hours during which the library space can be accessed and used by visitors without the presence of individuals with responsibility for library services or anyone else trained to assist visitors in using those services.

The conditions of access during unstaffed hours should be specified in the metadata / additional information accompanying the dataset.

There is a column for each day. Hours are in 24-hour clock and include start and end e.g. **09:00-17:00**. If there are multiple opening hours in a day these can be separated by commas e.g. **07:00-10:00,17:00-22:00** would accommodate staffed hours 10:00-17:00 that day and unstaffed hours before and after.

#### Special hours

This column allows for adding dates that are different to normal. This could be public holidays when the library is closed, or other exceptional situations. The format is to specify the date, include a colon, and then the opening hours. Instances of special hours are then separated by commas. For example, **2019-12-25: X, 2019-12-26: X,2019-12-27: 10:00-13:00**. This would describe that the library is closed on the 25th and 26th December, and open from 10am to 1pm on the 27th December.

For more info see [these Google support pages](https://support.google.com/business/answer/6303076).

### Potential problems

---

#### UPRN

UPRN (Unique property reference number) is not currently part of the schema. If we include this it is worth nothing that Excel can do odd things when holding big numbers, and it may transform them to scientific notation (e.g. 1.23E+10). UPRNs are also sometimes stored as 'zero padded' to ensure they are all the same length e.g. '00000199356' rather than '199356'. We would likely get a mix of both styles.

### How the data is updated

---

Each service can maintain a single data file that is updated whenever the details change, including changes to opening hours. As the data contains closed libraries, there is no need to remove these if a library is closed, the file can be updated by adding the year of closure. If there are new libraries, they can be added as an additional row.

### How the data could be used {#usage}

---

#### Locally

Accurate data on libraries is useful to analyse library provision, especially at a local level. For example, a tool to display Plymouth library locations uses location data to assess the population within walking, cycling, or driving distance of a library and compare these visually.

<figure>
    <img src="{{site.url}}/images/libraries_plymouth.png" alt="Displaying a map with Plymouth Central Library at the centre and walking travel distances around it"/>
    <figcaption>Population within 5 minute walking intervals around Plymouth Central Library.</figcaption>
</figure>

The application also uses opening hours to show libraries open at the current time, and event data to search for libraries hosting certain types of events.

It was built using library listings from Plymouth, event listings, and open map data from open street map. To try it out see the [Plymouth Library Finder](https://plymouth.librarydata.uk).

#### Nationally

Nationally, combined with the mobile library stops dataset, we can use this data to identify particular areas that are without libraries, and that would be in particular need of a library service.

This can be harder to assess with only local data, as many libraries and mobile library stops serve people between authority boundaries.

### Future enhancements

---

#### Staffed and unstaffed hours

Paragraph below superseded by discussions from November 2019 meeting, when testers decided to include unstaffed hours in the January 2020 testing phase.

*Many libraries will have a mix of 'types' of opening hours, such as when the library can be entered using a library card and PIN when there are no staff. This can be described in different ways, such as extended access.*

*Different ways of handling these hours could be:*

1. *Separate out staffed/non-staffed into separate columns*
2. *Decide on set guidance about what hours should be included (e.g. the opening hours MUST be staffed hours where the building is open to all)*
3. *Leave it up to the services to decide what hours to use, but encourage use of the notes field for additional details (e.g. a service may say "Our opening hours include extended access use, for which members must...")*

*Before deciding on this, more research should be conducted with a wider group of services. It will likely be important to capture additional information about unstaffed hours, such as:*

- *Who is able to access*
- *Training required for access*
- *Facilities available during these hours*

#### Unique Property Reference Number

The Unique Property Reference Number (UPRN) is a unique number that identifies a property. A UPRN is assigned by the local authority to each building.

Discussions on Slack December 2019 on IP rights claimed over UPRN and coordinates led to the removal of the UPRN field for the January 2020 testing phase for this dataset.

#### Library floor space and building

Adding data about the library building would give a useful context to the library, particularly as there can be a big difference between the facilities offered by a central library to a branch library. Some indicative data could be available through Ordnance Survey, as the UPRN identifier for the building would allow us to lookup building footprint and height.

---

[&lt; Back to home](./)
