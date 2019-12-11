---
layout: default
title: Loans
description: Lending of items in libraries
---

[&lt; Back to home](./)

### Definition

---

A loan is the issuing of an item of stock to a member of the library service. A renewal of an item already on loan is counted as an additional loan.
Loans of both physical and electronic materials are included.

### How the data can be collected

---

Library management systems will have the means of extracting and reporting data, and so this should be able to be automated. This may include automated publishing of the data at regular intervals.

### Sample data row

| Local authority | Library name | Month | Type | Loans |
| --------------- | ------------ | ----------- | ---- | ----- |
| Barnet | Barnet Book Club | 2019-04 | Adult audiobook | 9 |

An example for an earlier version of this dataset can be viewed at [Barnet loans](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/loans_barnet.csv).

### Field notes

---

#### Month

Use the format YYYY-MM for the month for which the data is reported.

#### Type

The type will be the item type the item is categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of types will be those that are used by each library service.

#### Loans

Combining issues and renewals of items into a single count is a method of reporting that was historically used by CIPFA, and is currently used for Public Lending Right data reporting. This means it is most likely to match the current reports that libraries run.

---

### Potential problems

#### Non-standardised item types

Using item types as they are designed by each library service will mean a lot of variation between similar types of items. For example one service may write 'Child Fiction' and another 'Fiction - Child'.

### How the data is updated

---

To update their loans data, library services can either:

- Publish an additional file with the new set of loans
- Update an existing file with the additional loans added as new rows

### How the data could be used

---

There are various types of dashboards that could be created to monitor loans either across libraries within an authority, or across authorities.

The following image shows a tool created by Richard Lynch to display Barnet loans data. It would also support data from other authorities and would allow people to filter or mix data for comparison.

The tool is available at [UK Library Issues](https://0sumrich.github.io/lib-issues/).

<figure>
    <img src="{{site.url}}/images/loans_uk.png" alt="A example of a bar chart displaying count of loans across different Barnet libraries." width="100%"/>
    <figcaption>Loans across a selection of libraries, with options to choose authority, date range, and library.</figcaption>
</figure>

### Future enhancements

---

#### Count start/end

A count start/end has been considered instead of the monthly reporting period.
The count start and end would be the report period the count is for. Detailed reporting would be encouraged. For example, the reporting could be on a daily basis, in which case the start and end would be the same. This would be good for analysis, such as comparing library use on different days of the week.

The proposal to test a monthly reporting was made at the early testers meeting in November 2019. We look forward to comments on the new column.

#### Each loan

To make the data more detailed, and to provide greater insight, each individual loan could be reported. This could allow for details such as popular titles and genres in different areas.

---

[&lt; Back to home](./)
