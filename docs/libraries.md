---
layout: default
title: Libraries
description: Library location opening hours and contact details
---



[&lt; Back to home](./)

### Definition

---

A library is a static service point which allows access to the general public to provide library services. This does not include mobile library services which are covered in a separate dataset.

### How the data can be collected

---

Manual collection. Library services will be able to use the library locations survey 2016 as a starting point.



### Sample data row


| Local authority | Library name | Address 1 | Address 2 | Address 3 | Postcode | Unique Property Reference Number | Statutory | Type of Library | Year opened | Year closed | Monday hours | Tuesday hours | Wednesday hours | Thursday hours | Friday hours | Saturday hours | Sunday hours | Special hours | Colocated | Colocated with | Notes | URL | Email address |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| Plymouth  | Crownhill | Cross Park Road | Crownhill | | PL6 5AN | 100041062012 | Yes | LAL | 1991 | | 08:30-18:00| 08:30-18:00 | 08:30-18:00 | 08.30-20:00 | 08:30-18:00 | 09:00-17:00 | | | No | | | https://www.plymouth.gov.uk/libraries/findlibraryandopeninghours/crownhilllibrary | library@plymouth.gov.uk

A full sample can be viewed at [Plymouth library list](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/libraries_plymouth.csv).



### Field notes

#### Local authority
This should be the official local authority name as listed in the relevant register.
England: https://www.registers.service.gov.uk/registers/local-authority-eng

Although the organisation may not actually be the local authority (e.g. a commissioned library service), it is important we can see which authorities are covered.

#### Statutory
All statutory libraries should be listed. For libraries that are not statutory it is up to the individual service as to whether they are included.

#### Type of library
The type of library is a code that describes how the library is run.

| Code | Title | Description | 
| ------------ | ------------ | ------------ |
| LAL | Local authority library | Library building funded, run and managed by local authority staff (can be augmented by unpaid volunteers). |
| LAL- | Local authority library (-) | As LAL, but unstaffed, for example, a book drop |
| CL | Commissioned library | Running of the library building/service has been transferred from the council to a separate trust or organisation. This may be operating as a social enterprise or may be commercial and is commissioned and funded by a local authority. The local authority are still accountable for the service.|
| CRL | Community run library | Library with some level of ongoing support from the council. Work according to a joint agreement such as a Service Level Agreement, Memorandum of Understanding or contract. Staff are volunteers, but some form of support is available. May or may not be counted as part of the statutory service. |
| IL | Independent library | Library that has been transferred to the management of a non local authority body, either community group or third party, which is outside the local authority network (for example for circulating bookstock, access to online catalogue). |

#### Year opened/closed
These columns should allow for new libraries, closures, and replacement libraries to be recorded. It would initially be too complex to try to link a new library to the library it is replacing. Closed libraries should be included if they were closed in or after 2010.

#### Opening hours
There are example formats for opening hours on schema.org, but they rely on very particular structures to the data which may be a barrier for users and data maintainers.

There are also complex situations such as breaks for lunch, extended access, seasonal hours, and opening hours which vary depending on what week of the month it is.

Google have a format which they use for people to manage their Google business accounts, which also includes a bulk upload spreadsheet option. See https://support.google.com/business/answer/3370250?hl=en-GB 

There is a column for each day. Hours are in 24 hour clock and include start and end e.g. 09:00-17:00. If there are multiple sessions in a day (e.g. a lunch break) these can be separated by commas e.g. 09:00-12:00,13:00-17:00.

#### Special hours
This column provides a means for adding dates that do not conform to the normal hours. This could be public holidays when the library is closed.

#### Address
If UPRN is provided, then coordinates, building footprint, and height, could all be available from Ordnance Survey. Ordnance Survey could potentially be approached by DCMS via BEIS (Department for Business, Energy and Industrial Strategy) to allow this data to be included, and automatically added if UPRN is provided.




### Potential problems

---

#### UPRN 

Excel can tend to be tricky when holding big numbers, and transform them to scientific notation when exporting to CSV format. UPRNs are also difficult as they are often held as a single number e.g. ‘199356’, but are sometimes held as ‘zero padded’ to ensure they are all the same length e.g. ‘00000199356’. We will likely get a mix of both.


### How the data is updated

---
Each service can maintain a single data file that is updated when the library details are updated. As the data contains closed libraries, there is no need to remove these if a library is closed, the file can be updated by adding the year of closure. If there are new libraries, they can be added as an additional row.

### How the data could be used

---

An example of what could be done with the data.

### Future enhancements

---

#### Future enhancement title

Something that could be added later on that will bring extra value to the dataset. Will generally be something that is likely to be too difficult immediately.

---

[&lt; Back to home](./)
