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

Detailed reporting is encouraged. For example, the reporting could be on a daily basis, in which case the start and end dates would be the same. This would be good for analysis, and b a level of detail that allowed for comparing library use on different days of the week.

#### Count type

At the moment we are not prescribing a standard way to report count type. It is up to each library service to describe their method in their own words. We recommend using concise and consistent wording in this field. If details about the count type(s) are needed they should be added to the dataset metadata.

### Potential problems

---

#### Count type

Each service will need to explain their method of manual counting in their metadata.

#### Date format

Recurring problem of software “auto-correcting” dates to another format.

### How the data is updated

---

To update their physical visits data, library services can:

- update the existing published file with the additional visits data added as new rows.

### How the data could be used {#usage}

---

#### Locally

It would be interesting to explore tools for physical visits that went beyond reporting a visit as a performance metric.

If a library service has automatic counters, that data could eventually be published in 'real-time'. This would allow for people to see how busy the library currently is - useful for deciding when to visit. Additional future datasets such as usage of computers, and desks, could provide more detailed information such as whether there are any free working spaces.

Manual data can be used retrospectively in data analysis. Through machine learning techniques this could be combined with other local data to predict visits and to gain a better understanding of how visits are affected by external factors. Such as weather, events, school holidays, etc.

#### Nationally

At a National level, a better understanding of visits into libraries is essential.

In 2019, Ordance Survey and the Office for National Statistics [released data on the High Streets of Great Britain](https://www.ordnancesurvey.co.uk/business-government/sectors/public-sector/high-streets). This included defining what a high street was, as well as analysing population and retail growth in those high streets, compared to other areas.

Combined with a completed [libraries](/libraries) dataset, this data could be used to answer questions such as:

- How many libraries are 'on' the high street, or in other areas?
- Do physical visits differ between libraries that are on the high street, and those that are not?
- Does declining (or rising) use of retail in different areas match that of visits to the local library?

### Future enhancements

---

#### Same count period for everyone

Depending on what testers and consulted parties prefer, we could adopt a count period (week, month) as part of the schema instead of the Count start and Count end. The disadvantage would be that in places that do not have an automatic counter the number may not be the actual data anymore but an extrapolated number. The advantage would be that figures can be easily compared between libraries and library services.

After discussions with an early group of testers in November 2019, it was decided to continue using count start / count end rather than a prescribed period for all libraries. It was felt that the data would be more accurate with a count start / end system.

---

[&lt; Back to home](./)
