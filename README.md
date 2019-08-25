# Library data schemas

This is a repository to hold open data schemas for public library data. A data schema describes how data is structured, such as the fields that should be held. It also describes constraints about the data, such as whether a field is required or optional, and what format the data in the field should be in.

## Prerequisites

The schemas are written using Table Schema. Table Schema is a standard format for describing table data, such as a spreadsheet. A benefit of writing schemas in this format is there are many associated software tools that will provide additional functionality, such as validating that a spreadsheet is correct.

- [Table Schema Documentation](https://frictionlessdata.io/docs/table-schema/)
- [Frictionless Data Software Tools](https://frictionlessdata.io/software/)

## Schemas

| Schema Name | File Name | Description |
| ----------- | --------- | ----------- |
| Mobile library stops | mobile-library-stops.json | Describes how data on mobile library stops can be held to enable to enable published timetables |
| Library locations survey | library-locations-survey.json | A survey conducted by DCMS libraries in 2016, with the schema updated in 2019 |

## Sample data

For each schema, sample data is held in the *samples* folder. This is to enable easy testing of the schema using tools such as [CSVLint](https://csvlint.io/). These files could also be used for automated testing, when making any schema updates.

For each schema, sample files will be provided:
- Each will have one example row of data
- Files with the name _success will provide a successful test against CSVLint
- Files with the the name _fail should fail validation.

## Versioning

We use [SemVer](http://semver.org/) for versioning.

Each schema will share a single version number, which will be updated on making any changes. If a new schema is added it will increment the version number of the current set, rather than start at 0.

All completed schemas will be held in the archived folder in this repository and the file name will include the version number. Schemas in development are held in the root folder.

## Authors

* **Dave Rowe** - *Initial work* - [DaveBathnes](https://github.com/DaveBathnes)

See also the list of [contributors](https://github.com/librarieshacked/schema-librarydata/contributors) who participated in this project.

## License

This project is openly licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
