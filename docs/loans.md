---
layout: default
title: Loans
description: Lending of items in libraries
---

[&lt; Back to home](./)

### Definition

---

A loan is the issuing of any item of stock within the library management system to a member of the library service. A renewal of a item on loan is counted as an additional loan.

### How the data can be collected

---

Library management systems will have the means of extracting and reporting data, and so this should be able to be automated. This may include automated publishing of the data at regular intervals.

### Sample data row

| Local authority | Library name | Count start | Count end | Type | Loans |
| --------------- | ------------ | ----------- | --------- | ---- | ----- |
| Barnet | Barnet Book Club | 2019-04-01 | 2019-06-30 | Adult audiobook | 9 |

A full sample can be viewed at [Barnet loans](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/loans_barnet.csv).

### Field notes

---

#### Count start/end

The count start and end is the report period the count is for.

Detailed reporting is encouraged. For example, the reporting could be on a daily basis, in which case the start and end would be the same date. This would be good for analysis, such as comparing library use on different days of the week.

#### Type

The type will be the item type as the item has been categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of item types will be whatever are used by the library service.

#### Loans

Combining issues and renewals of items into a single count is a method of reporting that was historically used by CIPFA, and is currently used for Public Lending Right data reporting. This means it is most likely to match the current reports that libraries run.

---

### Potential problems

#### Non-standardised item categories

Using item types as they are designed by each library service will mean a lot of variation between similar types of items. For example one service may write 'Child Fiction' and another 'Fiction - Child'.

### How the data is updated

---

To update their loans data, library services can either:

- Publish an additional file with the new set of loans
- Update an existing file with the additional loans added as new rows

### How the data could be used

---

Accurate loans data, by item type will be able to show patterns in what type of items are loaned between different authorities. As stock data by item type will also be published, tools can be created that aim to analyse stock alongside loans to provide local and national insight into stock and demand.

<figure>
    <img src="{{site.url}}/images/loans_barnet.png" alt="Bar chart displaying count of items of stock in Barnet with markers for loan counts per type." width="100%"/>
    <figcaption>Items of stock in Barnet with markers to show count of loans of those item types.</figcaption>
</figure>


### Future enhancements

---

#### Each loan

To make the data more detailed, and to provide greater insight, each individual loan could be reported.

---

[&lt; Back to home](./)
