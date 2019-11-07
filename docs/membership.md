---
layout: default
title: Membership
description: Active membership of libraries by area
---

[&lt; Back to home](./)

### Definition

---

A library member is a user registered with the library service, with a record in the library management system. The user does not need to have borrowed an item within any timescale to be considered a member. It is assumed inactive users are removed from the library system after an appropriate period of time in accordance with GDPR.

### How the data can be collected

---

Library management systems will have the means of extracting and reporting data on membership. It's unlikely that systems will be able to directly report the area codes required by this dataset, so there will be the need for a tool to convert from postcodes to the area codes (see details below).

### Sample data row

| Local authority | Count date | Area code | Members |
| --------------- | ---------- | --------- | ------- |
| Bristol City Council | 2018-10-23 | E01014370 | 395 |

A full sample can be viewed at [Bristol membership](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/membership_bristol.csv).

### Field notes

---

#### Area code

The area code is the Office for National Statistics agency 9-character code for the Lower super output area (LSOA), calculated from the member's postcode. If members have multiple addresses, the primary addresses should be used.

An LSOA is a small geographic area used for statistics. More detail and a beginner's guide are available
at the [Oxford Consultants for Social Inclusion](https://ocsi.uk/2019/03/18/lsoas-leps-and-lookups-a-beginners-guide-to-statistical-geographies/) website.

A benefit of reporting membership data using these area codes is that they also hold all kinds of other associated data from other sources. For example, population codes, health, income, education level, car ownership, etc. This allows for really powerful data analysis.

It is not possible to allow reporting of membership by postcode, as postcodes could include just one or very few people. An alternative option would be to report using higher level postcode data (e.g. 'BA1' rather than 'BA1 6AX'). However, this has little actual use for data analysis and will have a great variation in terms of the number of people.

---

### Potential problems

#### Area codes

There are lookup files that will convert from postcode to LSOA area code. So as long as the library service can report on membership by postcode, then they can also report on membership by LSOA

### How the data is updated

---



### How the data could be used

---

### Future enhancements

---

---

[&lt; Back to home](./)
