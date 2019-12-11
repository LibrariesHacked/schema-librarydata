---
layout: default
title: Stock summary
description: Summary counts of the stock held by libraries
---

[&lt; Back to home](./)

### Definition

---

An item of stock is any item held by the library that is available to the public, and catalogued in the library management system. This dataset is a summary of the number of different types of items held by libraries.

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

The type will be the item type the item is categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of types will be those that are used by each library service.

### Potential problems

---

#### Non-standardised item types

Using item types as used by each library service will mean a lot of variation between similar types of items. For example one service may write 'Child Fiction' and another 'Fiction - Child'.

### How the data is updated

---

As the data is a 'snapshot' of the current count of items in a library catalogue, it would be easiest for the library services to publish a new file every time they do this count.

### How the data could be used

---

Tools can be created that aim to analyse stock alongside loans, to provide local and national insight into stock and demand.

<figure>
    <img src="{{site.url}}/images/loans_barnet.png" alt="Bar chart displaying count of items of stock in Barnet with markers for loan counts per type." width="100%"/>
    <figcaption>Items of stock in Barnet with markers to show count of loans of those item types.</figcaption>
</figure>

The above graph was created using Tableau, and used Barnet stock summary and loans to compare the two. In this example, note the particular high use of Children's Fiction items.

It is also a first step to publishing more detailed catalogue data, which could be used for more powerful purposes. Such as an open source inter-library loans and cross-catalogue single platform.

### Future enhancements

---

#### Full catalogue detail

It is likely that the enhancements to this dataset would need an additional schema e.g. 'stock detail'. This would provide more complete information on all the titles and items held by the library service such as:

- Title
- Author (where applicable)
- ISBN (where applicable)
- Date acquired
- Date published
- Checkout status or item status (missing, withdrawn, on loan...)
- Count of loans

As well as providing detailed insight into catalogues across the country, workshops could be held on cleaning and refining the data held in library catalogues.

---

[&lt; Back to home](./)
