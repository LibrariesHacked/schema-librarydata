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

For our public library data, each dataset has its own schema definition file. All schemas include the official ONS/GSS Local Authority Code, linking relationally to the master Library Services registry. Current schemas in development can be viewed using the links below.

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

- [v1.0.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/1.0.0): Major release adding the master `library-services.json` registry with all 208 UK authorities, extending `libraries.json` to 51 fields with coordinates, operational status, ACE co-locations, WiFi breakdown, and accessibility facilities, standardizing `Local authority code` with foreign keys across all schemas, and fully aligning `mobile-library-stops.json`.
- [v0.3.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.3.0): Added `events.json`, `libraries.json`, `loans.json`, `membership.json`, `physical_visits.json`, and `stock_summary.json`.
- [v0.2.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.2.0): Added `library-locations-survey.json`.
- [v0.1.0](https://github.com/LibrariesHacked/schema-librarydata/tree/master/archive/0.1.0): Initial release with `mobile-library-stops.json`.

---

[< Back to home](./)
