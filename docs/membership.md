---
layout: default
title: Membership
description: Active membership of libraries by area
---

[&lt; Back to home](./)

### Definition

---

A library member is any user registered with the library service. The user does not need to have borrowed a library item within any timescale to be considered a member. It is assumed inactive users are removed from the library system after an appropriate period of time, in accordance with GDPR.

### How the data can be collected

---

Library management systems will be able to extract data about members. However, it's unlikely those systems will be able to report the area codes required in this dataset, so an additional [tool to convert from postcodes to LSOAs](https://create.librarydata.uk/postcode-to-lsoa) has been created to help. A list of postcodes is required to use this.

### Sample data row

| Local authority | Count date | Area code | Members |
| --------------- | ---------- | --------- | ------- |
| Bristol City Council | 2018-10-23 | E01014486 | 557 |

A full sample can be viewed at [Bristol membership](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/membership_bristol.csv).

### Field notes

---

#### Area code

We cannot publish membership by postcode, as postcodes can identify individuals. An alternative option would be to use postcode area (e.g. 'BA1' rather than 'BA1 6AX'). However, this does not have much use for data analysis, and will have a great variation in the number of people in each area.

The area code in this datset is the Office for National Statistics 9-character code for the Lower super output area (LSOA). The dataset will count members by the LSOA they live in. If members have multiple addresses, the primary addresses should be used.

An LSOA is a small geographic area used in statistics. More detail and a beginner's guide are available
at the [Oxford Consultants for Social Inclusion](https://ocsi.uk/2019/03/18/lsoas-leps-and-lookups-a-beginners-guide-to-statistical-geographies/) website.

A benefit of reporting membership data using LSOAs is that many other datasets use these areas. For example, population counts, health, income, education, car ownership, etc.

As long as the library service can extract member postcodes, they should be able to report members by LSOA. The ONS also publish [postcode to LSOA lookup tables](https://geoportal.statistics.gov.uk/datasets/postcode-to-output-area-hierarchy-with-classifications-august-2019-lookup-in-the-uk).

A [postcode to LSOA converter](https://create.librarydata.uk) has been published to help services to create this dataset.

If address data is unavailable for a member, or for any other reason the LSOA is not known, an "Unknown" value can be placed in the column to group together members with no specified LSOA.

#### Members

The members column specifies the count of membership in each LSOA.

If this count is less than 5, the data should be suppressed. This protects confidentiality, and avoids identifying individuals.

For example, the following would be used if only 3 members were identified to be in LSOA E01014486.

| Bristol City Council | 2018-10-23 | E01014486 | x |

---

### Potential problems

#### Area codes

There are lookup files that can be used to convert from postcode to LSOA area code. So as long as the library service can report on membership by postcode, then it will be possible to report on membership by LSOA.

### How the data is updated

---

As the data is a 'snapshot' of the current count of members, it would be easiest for the library services to publish a new file every time they do this count.

### How the data could be used

---

One usage for the data would be to map the areas along with other statistics. One of these is population counts, another is indices of deprivation.

For example, in the sample data row, we have the following area.

| Local authority | Count date | Area code | Members |
| --------------- | ---------- | --------- | ------- |
| Bristol City Council | 2018-10-23 | E01014486 | 557 |

This shows that there were 557 library members in [LSOA area E01014486](https://mapit.mysociety.org/area/115005.html), which is St Agnes in Bristol. Looking at other data sources, the area is ranked 3,573 out of 32,844 for deprivation in England, which puts it in the 20% most deprived neighbourhoods. The population of the area was estimated in mid-2018 to be 2,435, so we can estimate a library membership of about 25% in that area.

Mapping and analysing this data provides many local uses such as seeing why certain areas don't use the library, looking at the particular needs of existing members, etc. Nationally, if we had detailed library membership data, that would become a dataset that would be of use for other agencies, such as those looking at digital exclusion, or use of public services.

The map on [librarieswest.github.io](https://librarieswest.github.io/map/) shows detailed membership data for all services in Libraries West in 2018.

<figure>
    <img src="{{site.url}}/images/membership_bristol.png" alt="Map displaying shading of LSOAs to represent membership levels across Bristol" width="100%"/>
    <figcaption>Membership mapped for Bristol libraries, showing information popup for area with 23% library membership.</figcaption>
</figure>

The map was created using ONS population estimates merged with library membership and Office for National Statistics map boundaries.

### Future enhancements

---

#### Library

An additional level of detail would be to include the particular library that the member is registered at.

#### Usage type

It would be interesting to be able to group the members by type of library usage. For example, those that use PCs, that borrow books, or use the WiFi (and any combinations of those).

---

[&lt; Back to home](./)
