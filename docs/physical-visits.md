---
layout: default
title: Physical visits
description: Number of visits made to library buildings
---

[< Back to home](./)

### Definition

---

A physical visit is an individual visiting a library building.

### How the data can be collected

Counting physical visits is notoriously difficult. Physical visits to shared buildings are especially tricky to count accurately.

An automatic people counter at the entrance of the space occupied by the library is ideal. However, it is up to each service to decide how they collect this data. Sometimes libraries within the same service will each use a different system to count physical visits. This is fine as long as it is clearly explained in the count type field and in the dataset metadata.

If starting from scratch, a [physical visits template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/physical_visits.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Local authority code | Library name | Count start | Count end | Count type | Visits |
| --------------- | -------------------- | ------------ | ----------- | --------- | ---------- | ------ |
| Newcastle City Council | E08000021 | Outer West | 2019-02-11 | 2019-02-17 | Manual (one week every quarter) | 767 |

You can view a bigger [sample from Newcastle Libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/physical_visits_newcastle.csv) and [sample from Plymouth Libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/physical_visits_plymouth.csv).

### Field notes

---

#### Local authority code

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E08000021` for Newcastle, `E06000026` for Plymouth). This links directly to the parent [library services dataset](./library-services).

#### Count start / Count end

The count start and end is the report period the count is for.

Detailed reporting is encouraged. For example, the reporting could be on a daily basis, in which case the start and end dates would be the same. This would be good for analysis, and be a level of detail that allowed for comparing library use on different days of the week.

#### Count type

At the moment we are not prescribing a standard way to report count type. It is up to each library service to describe their method in their own words. We recommend using concise and consistent wording in this field. If details about the count type(s) are needed they should be added to the dataset metadata.

### Potential problems

---

#### Co-location

Where a library is co-located with other services, such as a council customer service centre, leisure centre, or café, it can be difficult to count library visits specifically unless dedicated sensors or turnstiles are present.

---

[< Back to home](./)
