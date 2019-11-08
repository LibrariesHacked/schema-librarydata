---
layout: default
title: Membership
description: Active membership of libraries by area
---

[&lt; Back to home](./)

### Definition

---

A library member is a user registered with the library service. The user does not need to have borrowed an item within any timescale to be considered a member. It is assumed inactive users are removed from the library system after an appropriate period of time, in accordance with GDPR.

### How the data can be collected

---

Library management systems will have the means of extracting and reporting data on membership. However, it's unlikely that systems will be able to report the area codes required by this dataset, so there will be the need for a tool to convert from postcodes to the area codes (more details on this page).

### Sample data row

| Local authority | Count date | Area code | Members |
| --------------- | ---------- | --------- | ------- |
| Bristol City Council | 2018-10-23 | E01014486 | 557 |

A full sample can be viewed at [Bristol membership](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/membership_bristol.csv).

### Field notes

---

#### Area code

It is not possible to allow reporting of membership by postcode, as postcodes could include very few people. An alternative option would be to use postcode area (e.g. 'BA1' rather than 'BA1 6AX'). However, this has little use for data analysis, and will have a great variation in terms of the number of people.

The area code is the Office for National Statistics 9-character code for the Lower super output area (LSOA), the member lives in. If members have multiple addresses, the primary addresses should be used.

An LSOA is a small geographic area used for statistics. More detail and a beginner's guide are available
at the [Oxford Consultants for Social Inclusion](https://ocsi.uk/2019/03/18/lsoas-leps-and-lookups-a-beginners-guide-to-statistical-geographies/) website.

A benefit of reporting membership data using LSOAs is that they also hold all kinds of other associated data from other sources. For example, population counts, health, income, education, car ownership, etc. This allows for really powerful data analysis.

As long as the library service can report counts of members by postcode, they should be able to report members by LSOA. The ONS publish [postcode to LSOA lookup tables](https://geoportal.statistics.gov.uk/datasets/postcode-to-output-area-hierarchy-with-classifications-august-2019-lookup-in-the-uk).

---

### Potential problems

#### Area codes

There are lookup files that will convert from postcode to LSOA area code. So as long as the library service can report on membership by postcode, then they can also report on membership by LSOA

### How the data is updated

---

As the data is a 'snapshot' of the current count of members, it would be easiest for the library services to publish a new file every time they do this count.

### How the data could be used

---

The natural usage for data that includes geographic areas would be to map these against other statistics for those areas. One of these is population counts, another is indices of deprivation.

For example, in the sample data row, we have the following:

| Local authority | Count date | Area code | Members |
| --------------- | ---------- | --------- | ------- |
| Bristol City Council | 2018-10-23 | E01014486 | 557 |

This shows that there were 557 library members in the area E01014486. [Area E01014486](https://mapit.mysociety.org/area/115005.html), which is St Agnes in Bristol. Looking at other data for the area, for deprivation the area is ranked 3,573 out of 32,844 in England, which puts it in the 20% most deprived neighbourhoods in England. The population of the area was estimated in mid-2018 to be 2435, so we can estimate a library membership of about 25%.

Mapping and analysing this data provides all sorts of uses in terms of outreach programmes, seeing why certain areas don't use the library, looking at the particular needs of existing members, etc. Nationally, if we had detailed library membership data, that would become something that would be of use for many other agencies such as those looking at digital exlcusion, or social engagement.

### Future enhancements

---

An additional level of detail would be to include the library that the member is registered at. 

#### Usage type

It would be interested to be able to group the members into the type of library usage. For example, those that use PCs, that borrow books, that use the WiFi (and any combinations of those).

---

[&lt; Back to home](./)
