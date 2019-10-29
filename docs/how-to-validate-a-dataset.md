---
layout: default
title: "How to: validate a dataset"
description: Instructions for checking your data conforms to the schema
---

[&lt; Back to home](./)

### Data validation

---

Validating our data gives us confidence that it is in the right format.

It does not guarantee that the data is **accurate**. A count of loans could be wrong, for example, and it would be difficult to spot. But it is a good start to ensure the data we publish will work in the systems that are designed to use it, and it can be combined with other services' data.

### Instructions

---

These instructions use the third party tool, [Good Tables](https://goodtables.io). This has been developed by the [Open Knowledge Foundation](https://okfn.org/).

1. In your browser, navigate to [https://try.goodtables.io](http://try.goodtables.io/)
2. In the **Source** text field, change the option to select 'Upload File'.
3. Using the **Browse** button, upload your CSV file
4. In the **Schema** text field, enter the URL of the schema that you want to validate the data against. These are listed below.
5. Click the **Validate** button.

| Schema | URL |
| ------ | --- |
| Events | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/events.json |
| Libraries | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/libraries.json |
| Loans | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/loans.json |
| Membership | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/membership.json |
| Mobile library stops | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/mobile-library-stops.json |
| Physical visits | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/physical_visits.json |
| Stock summary | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/stock_summary.json |

If all goes well, the data should be reported as being a valid table.

<figure>
    <img src="{{site.url}}/images/how-to-validate-a-dataset-valid.png" alt="Example of successful data validation"/>
    <figcaption>An example of a successful data validation, using Plymouth library listings.</figcaption>
</figure>

### Dealing with problems

---

It is possible that the data validation tells you you don't have a valid table.

In these cases, the tool will report the things that are incorrect. In the example shown below, the data has failed validation because some of the mandatory columns have no values in them (reported as a 'required constraint'). Another error reported is an 'enumerable constraint' which means the column value does not match a set of values that the schema is expecting. In this particular case 'Mon' has been used instead of 'Monday'.

Although it may not always be clear what is wrong with the data, this documentation should give a full description of the data expected. The sample files have successfully passed validation, and can also be used as a comparison.

<figure>
    <img src="{{site.url}}/images/how-to-validate-a-dataset-invalid.png" alt="Example of invalid data"/>
    <figcaption>An example of invalid data, with numerous errors reported.</figcaption>
</figure>

---

[&lt; Back to home](./)