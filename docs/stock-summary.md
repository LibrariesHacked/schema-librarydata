---
layout: default
title: Stock summary
description: Summary of the stock held in libraries
---

[< Back to home](./)

### Definition

---

A count of the stock items held in each library, by the item type.

### How the data can be collected

This data will be recorded in the library service's Library Management System (LMS).

Library management systems will have the means of extracting and reporting data, and so this should be able to be automated. This may include automated publishing of the data at regular intervals.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/stock_summary.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Local authority code | Library name | Count date | Type | Items |
| --------------- | -------------------- | ------------ | -----------| ---- | ----- |
| Barnet | E09000003 | Burnt Oak | 2019-10-07 | Adult audiobook | 208 |

A full sample can be viewed at [Barnet stock summary](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/stock_summary_barnet.csv).

### Field notes

---

#### Local authority code

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E09000003` for Barnet). This links directly to the parent [library services dataset](./library-services).

#### Type

The type will be the item type the item is categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of types will be those that are used by each library service.

### Potential problems

---

#### Non-standardised item types

Using item types as used by each library service will mean variation between similar types of items. For example one service may write 'Child Fiction' and another 'Fiction - Child'.

### How the data is updated

---

To update stock summary data, library services can either publish a new file for each count period or append new count dates.

---

[< Back to home](./)
