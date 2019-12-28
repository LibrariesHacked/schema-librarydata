# Library data schemas

This is a repository to hold open data schemas for public library data. A data schema describes how data is structured, such as the fields that should be held. It also describes constraints about the data, such as whether a field is optional, and what data type the fields should hold.

## Information

The schemas are written using Table Schema. Table Schema is a standard format for describing table data, such as that which can be held in a spreadsheet. A benefit of writing schemas in this format is there are  software tools that will provide additional functionality, such as validating that data conforms to a schema.

- [Table Schema Documentation](https://frictionlessdata.io/docs/table-schema/)
- [Frictionless Data Software Tools](https://frictionlessdata.io/software/)
- [Good Tables](https://goodtables.io/)

## Documentation

Descriptive documentation for these schemas is held in the ```docs``` directory within this repository.

## Schemas

| Name | File | Description |
| ---- | ---- | ----------- |
| Membership | membership.json | The membership of a library service |
| Events | events.json | The number of people attending library events |
| Loans | loans.json | The number of items being issued in libraries |
| Libraries | libraries.json | A listing of library locations and their details |
| Library locations survey 2019 | library-locations-survey.json | A survey of library locations in England in 2019 |
| Mobile library stops | mobile-library-stops.json | Mobile library stops with their timetabled visits |
| Physical visits | physical-visits.json | The number of visits made to library buildings |
| Stock summary | stock-summary.json | Summary of the stock held in libraries |

## Test data

For each schema, test data is held in the *tests* folder. This is to enable easy testing of the schema using tools such as [CSVLint](https://csvlint.io/) and [Good Tables](https://try.goodtables.io). These files could also be used for automated testing, when making any schema updates.

For each schema, test files will be provided:

- Each will have one example row of data
- Files with the name _success will provide a successful test
- Files with the the name _fail should fail validation.

## Real data

We will also be providing real data examples, held in the data folder.

## Versioning

We use [SemVer](http://semver.org/) for versioning.

Each schema will share a single version number, which will be updated on making any changes. If a new schema is added it will increment the version number of the current set, rather than start at 0.

All completed schemas will be held in the archived folder in this repository and the file name will include the version number. Schemas in development are held in the root folder.

## Authors

See the list of [contributors](https://github.com/librarieshacked/schema-librarydata/contributors) who participated in this project.
