---
layout: default
title: "How to: validate a dataset"
description: Instructions for checking your data conforms to the schema
---

[&lt; Back to home](./)

### Data validation

---

Validating data gives us confidence it is in the right format.

It does not guarantee the data is **accurate**. A count of loans could be factually wrong. But it ensures the data we publish will work in systems that are designed to use it, and it can be combined with other services' data.

### Instructions

---

These instructions use the tool, [Good Tables](https://goodtables.io), developed by the [Open Knowledge Foundation](https://okfn.org/).

1. In your browser, navigate to [https://try.goodtables.io](http://try.goodtables.io/)
2. In the **Source** text field, select the option to 'Upload File'.
3. Using the **Browse** button, upload your CSV file
4. In the **Schema** text field, enter the URL of the schema that you want to validate the data against. These are listed in the table further down this page.
5. Click the **Validate** button. The tool will report whether the table is valid.

<figure>
    <img src="{{site.url}}/images/how-to-validate-a-dataset-valid.png" alt="Example of successful data validation" />
    <figcaption>An example of a successful data validation, using Plymouth library listings.</figcaption>
</figure>

#### Possible schemas to use

| Schema | URL |
| ------ | --- |
| Events | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/events.json |
| Libraries | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/libraries.json |
| Loans | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/loans.json |
| Membership | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/membership.json |
| Mobile library stops | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/mobile-library-stops.json |
| Physical visits | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/physical_visits.json |
| Stock summary | https://raw.githubusercontent.com/LibrariesHacked/schema-librarydata/master/stock_summary.json |

### Dealing with problems

---

The data validation may tell you you don't have a valid table.

In these cases, it will display the things that are incorrect. In the example shown below, the data has failed validation because some mandatory columns have no values in them (reported as a 'required constraint'). Another error reported is an 'enumerable constraint', which means a column value does not match what the schema is expecting. In this case, 'Mon' has been used instead of 'Monday'. Although it often seems overly picky, it's important we use consistent values for our data.

It may not be clear what is wrong with the data. This documentation should give guidance of the data expected. The [sample files](https://github.com/LibrariesHacked/schema-librarydata/tree/master/data) have all successfully passed validation, and can also be used as reference.

<figure>
    <img src="{{site.url}}/images/how-to-validate-a-dataset-invalid.png" alt="Example of invalid data"/>
    <figcaption>An example of invalid data, with errors displayed.</figcaption>
</figure>

---

[&lt; Back to home](./)