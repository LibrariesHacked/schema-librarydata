---
layout: default
title: Common field standards
description: Guidelines for fields that are shared between datasets
---

[< Back to home](./)

### Field standards in v2.0.0

---

From version 2.0.0, every field in our Table Schemas uses a standard **lowercase machine name** (`name`) for CSV column headers and API properties, alongside a **friendly human-readable title** (`title`) for display interfaces, documentation, and data entry forms.

### Field notes

---

This page describes fields that will be used in multiple datasets.

#### Local authority (`local_authority`)

In the UK, this should be the local authority name as listed in the relevant register on gov.uk.

| Area | Local authority register |
| ---- | ------------------------ |
| Scotland | [Local authorities in Scotland](https://www.registers.service.gov.uk/registers/local-authority-sct) |
| Wales | [Local authorities in Wales](https://www.registers.service.gov.uk/registers/principal-local-authority) |
| Northern Ireland | [LibrariesNI](https://www.librariesni.org.uk) |
| England | [Local authorities in England](https://www.registers.service.gov.uk/registers/local-authority-eng) |

Although the organisation running the library service may be different (e.g. they may be a commissioned library service), it's the local authority that has statutory responsibility for the library service, and should be listed.

An exception to this is Northern Ireland, as Libraries NI have statutory responsibility for libraries.

#### Local authority code (`local_authority_code`)

The official Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E06000026` for Plymouth, `E09000003` for Barnet).

This standard 9-character alphanumeric code (matching `^[ELMNSW][0-9]{8}$`) uniquely identifies the statutory local authority across England (`E`), London (`L`), Metropolitan districts (`M`), Northern Ireland (`N`), Scotland (`S`), and Wales (`W`), as well as Crown Dependencies. It serves as a relational foreign key across all library datasets, linking directly to the central [library services dataset](./library-services).

#### Library name (`library_name`)

It is recommended for each authority to be consistent as to whether the word 'Library' is included in their library names.

The name should be consistent wherever it is listed. This is important for linking data between datasets. For example, the physical visits dataset does not include data to show whether the library is colocated with other services. That data is held in the libraries dataset. Combining both datasets relies on the two datasets sharing the same library names.

#### Date fields

The 25th December 2019 could be written in multiple ways.

- 2019-12-25
- 25/12/2019
- 12/25/2019

Dates should be specified using the International Standard [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) (e.g. **2019-12-25**, described as YYYY-MM-DD). This provides a widely recognised and unambiguous solution.

### Potential problems

#### Dates

There can be a recurring problem of software 'auto-correcting' dates to another format. This will often use settings on the user's computer. Data validation will ensure that the format is enforced, but guidance can be provided for data publishers on how to tackle these software issues.

It could also be that online tools detect the date format, and convert it to the standard.

---

[< Back to home](./)
