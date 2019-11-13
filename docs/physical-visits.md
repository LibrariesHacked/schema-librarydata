---
layout: default
title: Physical visits
description: People counters and manual surveys of library visitors
---


[&lt; Back to home](./)

### Definition

---

A physical visit is defined as an individual entering the library premises - for whatever reason.
For co-located premises this may mean counting visits that are not specifically for using library services. To show that premises are co-located use the relevant columns in the [libraries dataset](https://schema.librarydata.uk/libraries).

### How the data can be collected

---

An automatic people counter at the the entrance of the space occupied by the library is ideal. However, it is up to each service to decide how they collect this data. Sometimes libraries within the same service will each use a different system to count physical visits. This is fine as long as it is clearly explained in the count type field and in the dataset metadata.

If starting from scratch, a [physical visits template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/physical_visits.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Library name | Count start | Count end | Count type | Visits |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| Newcastle City Council | Outer West | 2019-02-11 | 2019-02-17 | Manual (one week every quarter) | 767 |

You can view a bigger [sample from Newcastle Libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/physical_visits_newcastle.csv).

### Field notes

---

Template metadata - accompanying text which explains the fields used and provides additional details on the data - will be provided for this dataset at a later stage.

#### Count start / Count end

The count start and end is the report period the count is for.

Detailed reporting is encouraged. For example, the reporting could be on a daily basis, in which case the start and end would be the same. This would be good for analysis, such as comparing library use on different days of the week.

#### Count type

At the moment we are not prescribing a standard way to report count type. It is up to each library service to describe their method in their own words. We recommend using concise wording in this field. If details about the count type(s) are needed they should be added to the dataset metadata.

### Potential problems

---

#### Count type

Each service may need to explain their method of manual counting in their metadata.

#### Date format

Recurring problem of software “auto-correcting” dates to another format.

### How the data is updated

---

To update their physical visits data, library services can:
- update the existing published file with the additional visits data added as new rows.

### How the data could be used

---

To be added later: an example of what could be done with the data.

### Future enhancements

---

#### Same count period for everyone
Depending on what testers and parties consulted prefer, we could adopt a count period (week, month) as part of the schema instead of the Count start and Count end. The disadvantage would be that in places that do not have an automatic counter the number may not be the actual data anymore but an extrapolated number. The advantage would be that figures can be easily compared between libraries and library services.


---

[&lt; Back to home](./)
