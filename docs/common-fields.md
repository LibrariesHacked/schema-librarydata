---
layout: default
title: Common field standards
description: Guidelines for common fields between datasets
---

[&lt; Back to home](./)

### Field notes

---

This page describes some common guidelines for fields that will be used between multiple datasets.

#### Local authority

This should be the local authority name as listed in the relevant register on gov.uk. These datasets were planned to be completed by authorities in England, but there's no reason why other library services could not publish to the same schema, and benefit from the data.

| Area | Local authority register |
| ---- | ------------------------ |
| Scotland | [Local authorities in Scotland](https://www.registers.service.gov.uk/registers/local-authority-sct) |
| Wales | [Local authorities in Wales](https://www.registers.service.gov.uk/registers/principal-local-authority) |
| Northern Ireland | [LibrariesNI](https://www.librariesni.org.uk) |
| England | [Local authorities in England](https://www.registers.service.gov.uk/registers/local-authority-eng) |

Although the organisation running the library service may not be the local authority (e.g. a commissioned library service), it's the authority that has statutory responsibility for the library service.

An exception to this is Northern Ireland, as Libraries NI have statutory responsibility for libraries.

#### Library name

The [libraries](./libraries) dataset is the core dataset for listing libraries. The name should be the publicly known name of the library.

It is recommended to be consistent as to whether the word 'Library' is included in the name.

The name must also be consistent wherever it is listed. This is essential to provide linked data between datasets. For example, the physical visists dataset does not have colocation information within it, because that is in the libraries dataset. This relies on the two datasets providing complementary information, and sharing the same names.

#### Date fields

A common standard should be agreed for dates. For example, the 25th December 2019 could be written in multiple ways.

- 25/12/2019
- 12/25/2019
- 2019-12-25

At the moment, the technical schemas validate dates to the 'default' date format, which is the International Standard [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) (e.g. **2019-12-25** or described as YYYY-MM-DD). This option provides a widely recognised and unambiguous solution.

### Potential problems

#### Date standards

There can be a recurring problem of software 'auto-correcting' dates to another format. This will often use the settings on the user's computer. Data validation should ensure that the format is enforced, but clear guidance can be provided for data publishers on how to get round software issues.

It could also be that an online tool could detect the existing date format, and convert it to the standard.

---

[&lt; Back to home](./)
