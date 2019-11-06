---
layout: default
title: Stock summary
description: Summary counts of the stock held by libraries
---

[&lt; Back to home](./)

### Definition

---

An item of stock is any item held by the library that is available to the public, and catalogued in the library management system. This dataset is a summary set of the number of different types of items held by libraries.

### How the data can be collected

---

Library management systems will have the means of extracting and reporting data, and so this collection should be able to be automated. This may include automation that also publishes the data at regular intervals.

### Sample data row

| Local authority | Library name | Count date | Type | Items |
| --------------- | ------------ | -----------| ---- | ----- |
| Barnet | Burnt Oak | 2019-10-07 | Adult audiobook | 208 |

A full sample can be viewed at [Barnet stock summary](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/stock_summary_barnet.csv).

### Field notes

---

#### Type

The type will be the item type as the item has been categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of item types will be whatever are used by the library service.

---

### Potential problems

#### Non-standardised item categories

Using item types as they are designed by each library service will mean a lot of variation between similar types of items. For example one service may write 'Child Fiction' and another 'Fiction - Child'.

### How the data is updated

---

As the data is a 'snapshot' of the current count of items in a library catalogue, it would be easiest for the library services to publish a new file every time they do this count.

### How the data could be used

---



### Future enhancements

---

#### Full catalogue detail


---

[&lt; Back to home](./)
