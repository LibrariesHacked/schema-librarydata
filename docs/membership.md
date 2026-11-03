---
layout: default
title: Membership
description: Count of active members with address located in an area
---

[< Back to home](./)

### Definition

---

An active member is someone who has used the library service in the previous twelve months.

This includes loans, using public computers, logging into online library services, or having library staff access their record on their behalf (e.g. to reset passwords).

### How the data can be collected

This data will be recorded in the library service's Library Management System (LMS).

Library management systems will have the means of extracting and reporting data, and so this should be able to be automated. This may include automated publishing of the data at regular intervals.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/membership.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Local authority code | Count date | Area code | Members |
| --------------- | -------------------- | ---------- | --------- | ------- |
| Bristol City Council | E06000023 | 2018-10-23 | E01014486 | 557 |

A full sample can be viewed at [Bristol membership](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/membership_bristol.csv).

### Field notes

---

#### Local authority code

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E06000023` for Bristol). This links directly to the parent [library services dataset](./library-services).

#### Area code

We cannot publish membership by postcode, as postcodes can identify individuals. An alternative option would be to use postcode area (e.g. 'BA1' rather than 'BA1 6AX'). However, this does not have much use for data analysis, and will have a great variation in the number of people in each area.

The area code in this dataset is the Office for National Statistics 9-character code for the Lower super output area (LSOA). The data holds counts of members by the LSOA they live in. If members have multiple addresses, the primary addresses should be used.

An LSOA is a small geographic area used in statistics. More detail and a beginner's guide are available at the [Oxford Consultants for Social Inclusion](https://ocsi.uk/2019/03/18/lsoas-leps-and-lookups-a-beginners-guide-to-statistical-geographies/) website.

A benefit of reporting membership data using LSOAs is that many other datasets use these areas. For example, population counts, health, income, education, car ownership, etc.

As long as the library service can extract member postcodes, they should be able to report members by LSOA. The ONS also publish [postcode to LSOA lookup tables](https://geoportal.statistics.gov.uk/datasets/postcode-to-output-area-hierarchy-with-classifications-august-2019-lookup-in-the-uk).

A [postcode to LSOA converter](https://create.librarydata.uk) has been published to help services to create this dataset.

If address data is unavailable for a member, or for any other reason the LSOA is not known, an "Unknown" value can be placed in the column to group together members with no specified LSOA.

If using a different area code this should be specified in the dataset metadata.

#### Count date

The date the count was taken.

#### Members

The number of active members in the specified LSOA.

---

[< Back to home](./)
