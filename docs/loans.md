---
layout: default
title: Loans
description: Number of items borrowed from libraries
---

[< Back to home](./)

### Definition

---

A loan is the issuing or renewal of an item from a library to a borrower.

### How the data can be collected

This data will be recorded in the library service's Library Management System (LMS).

Library management systems will have the means of extracting and reporting data, and so this should be able to be automated. This may include automated publishing of the data at regular intervals.

### Sample data row

| local_authority | local_authority_code | library_name | month | type | loans |
| --------------- | -------------------- | ------------ | ----- | ---- | ----- |
| Barnet | E09000003 | Barnet Book Club | 2019-04 | Adult audiobook | 9 |

A full sample can be viewed at [Barnet loans](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/loans_barnet.csv).

### Field notes

---

#### Local authority code (`local_authority_code`)

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E09000003` for Barnet). This links directly to the parent [library services dataset](./library-services).

#### Month (`month`)

Use the format YYYY-MM for the month for which the data is reported.

#### Type (`type`)

The type will be the item type the item is categorised under in the library management system.

This should ideally be a human readable value rather than a code. For example 'Adult Fiction' rather than 'ADU_FIC'. The set of types will be those that are used by each library service.

#### Loans (`loans`)

Combining issues and renewals of items into a single count is a method of reporting that was historically used by CIPFA, and is currently used for Public Lending Right data reporting. This means it is most likely to match the current reports that libraries run.

---

### Potential problems

---

#### Lack of standard categories

Library services use different categorisations for their stock items, and there is no national standard. For example, some services may split children's stock into 'Board books', 'Picture books', 'Early readers', etc. Others may just use 'Children's fiction'.

This means comparing data across services will require an agreed set of higher-level categories that service-specific types can be mapped into.

#### Issues and renewals combined

Combining issues and renewals loses the distinction between an item being borrowed for the first time and a loan being extended. Where possible, services should consider reporting these separately in future schemas.

---

[< Back to home](./)
