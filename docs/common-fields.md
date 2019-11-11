---
layout: default
title: Common field standards
description: Guidelines for common fields between datasets
---

[&lt; Back to home](./)

### Field notes

---

This page describes fields that will be used in multiple datasets.

#### Local authority

This should be the local authority name as listed in the relevant register on gov.uk.

| Area | Local authority register |
| ---- | ------------------------ |
| Scotland | [Local authorities in Scotland](https://www.registers.service.gov.uk/registers/local-authority-sct) |
| Wales | [Local authorities in Wales](https://www.registers.service.gov.uk/registers/principal-local-authority) |
| Northern Ireland | [LibrariesNI](https://www.librariesni.org.uk) |
| England | [Local authorities in England](https://www.registers.service.gov.uk/registers/local-authority-eng) |

Although the organisation running the library service may not be a local authority (e.g. a commissioned library service), it's the authority that has statutory responsibility for the library service and should be listed.

An exception to this is Northern Ireland, as Libraries NI have statutory responsibility for libraries.

#### Library name

It is recommended to be consistent as to whether the word 'Library' is included in the name.

The name should be consistent wherever it is listed. This is important to link data between datasets. For example, the physical visits dataset does not say whether the library is colocated with other services. That data is held in the libraries dataset. Using both datasets relies on the two datasets sharing the same library names.

#### Date fields

The 25th December 2019 could be written in multiple ways.

- 25/12/2019
- 12/25/2019
- 2019-12-25

At the moment, dates should be specified using the International Standard [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) (e.g. **2019-12-25**, or described as YYYY-MM-DD). This option provides a widely recognised and unambiguous solution.

### Potential problems

#### Dates

There can be a recurring problem of software 'auto-correcting' dates to another format. This will often use settings on the user's computer. Data validation will ensure that the format is enforced, but guidance can be provided for data publishers on how to tackle these software issues.

It could also be that an online tool could detect the date format, and convert it to the standard.

---

[&lt; Back to home](./)
