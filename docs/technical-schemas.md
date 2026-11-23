---
layout: default
title: Technical schemas
description: Formal definitions of what the data should look like
---

[< Back to home](./)

### Schema definitions

---

[Table Schema](https://frictionlessdata.io/docs/table-schema/) is a standard for writing data schemas. It allows for a formal definition of what the columns should be in a dataset, and what type of data can be in each column.

This allows us to validate data with tools that can check whether files match the specified schema.

For our public library data, each dataset has its own schema definition file. All schemas in v2.0.0 use:
- **Lowercase field names** (`name`): snake_case machine identifiers used for CSV headers and database columns (e.g. `local_authority`, `local_authority_code`, `library_name`).
- **Friendly field titles** (`title`): human-readable display labels for user interfaces, data entry forms, and reports (e.g. `Local authority`, `Local authority code`, `Library name`).
- **Relational integrity**: explicit `primaryKey` and `foreignKeys` linking child records via `local_authority_code` to the central `library-services` registry.
- **Full LibraryCommons Alignment**: complete 62-field `libraries.json` schema (including accessibility, modern spaces, and branch URLs) and 52-field `library-services.json` schema.
- **Frictionless Compliance**: formal top-level metadata, `homepage`, and explicit `missingValues: [""]` across all schemas.

Current schemas in development can be viewed using the links below:

- [Library services](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/library-services.json)
- [Libraries](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/libraries.json)
- [Events](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/events.json)
- [Loans](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/loans.json)
- [Membership](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/membership.json)
- [Mobile library stops](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/mobile-library-stops.json)
- [Physical visits](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/physical_visits.json)
- [Stock summary](https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/stock_summary.json)

### Version archive

---

Completed releases are archived by semantic version in the [archive folder](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive):

- [v2.0.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/2.0.0) (Current / Release candidate): Upgrades all schemas to standard lowercase `name` identifiers with friendly `title` labels; enhances validation rules including non-negative counts, UPRN bounds, coordinate ranges, and expanded `^[ELMNSW][0-9]{8}$` code patterns; and adds full support for LibraryCommons project requirements.
- [v1.0.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/1.0.0): Added master `library-services.json` registry with all 208 UK authorities, extended `libraries.json` to 51 fields with coordinates, operational status, ACE co-locations, WiFi breakdown, and accessibility facilities, standardized `Local authority code` with foreign keys across all schemas, and fully aligned `mobile-library-stops.json`.
- [v0.3.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.3.0): Added `events.json`, `libraries.json`, `loans.json`, `membership.json`, `physical_visits.json`, and `stock_summary.json`.
- [v0.2.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.2.0): Added `library-locations-survey.json`.
- [v0.1.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.1.0): Initial release with `mobile-library-stops.json`.

---

[< Back to home](./)
