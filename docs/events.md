---
layout: default
title: Events
description: Library event attendance and outcomes
---

[&lt; Back to home](./)

### Definition

---

A library event is an event held within a library, and facilitated or organised by the library service. Each event should be listed.

### How the data can be collected

---

Data collection on events is likely to be manual, but could be aided by reports from existing systems, such as Eventbrite. Or be recorded in custom spreadsheets and databases. For example, Barnet collect event data using a custom Access database, which can then be exported as CSV.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/events.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Library name | Event date | Name | Outcome | Attendees |
| --------------- | ------------ | ---------- | ---- | ------- | --------- |
| Barnet | Burnt Oak | 2018-01-12 | Toddler Read and Rhyme | Stronger more resilient communities | 11 |

A full sample can be viewed at [Barnet events](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/events_barnet.csv).

### Field notes

---

#### Outcome

The set of outcomes are taken from the Libraries Taskforce Ambition document: [outcomes libraries deliver for their communities](https://www.gov.uk/government/publications/libraries-deliver-ambition-for-public-libraries-in-england-2016-to-2021/libraries-deliver-ambition-for-public-libraries-in-england-2016-to-2021#the-outcomes-libraries-deliver-for-their-communities). One of these outcomes must be selected for each event.

| Outcome |
| ------- |
| Cultural and creative enrichment |
| Increased reading and literacy |
| Increased digital access and literacy |
| Helping everyone achieve their full potential |
| Healthier and happier lives |
| Greater prosperity |
| Stronger more resilient communities |

---

### Potential problems

#### Multiple or unknown outcomes

It could be difficult for a library service to assign an outcome to each event. It's likely that an event would apply to multiple different outcomes. In these cases, at the moment just one has to be selected. This is likely to lead to situations where similar events are assigned under different outcomes.

We should investigate options to:

- Assign multiple outcomes
- Have an option for leaving this empty or unknown
- Have guidance for common event types that suggests which outcomes to use

#### Non-library events

The definition of library events as being 'facilitated or organised by the library service' is broad. This means library services may include events that others wouldn't. For example, reading groups that are largely self-organised, but use library premises and books. For now this will left to the discretion of the service.

### How the data is updated

---

To update their event data, library services can either:

- Publish an additional file with the new set of events
- Update an existing file with each new event as an additional row

Depending on how many events the service holds, a new file may be easier to manage.

### How the data could be used

---

Having comprehensive data on events alongside traditional usage data such as loans will be a long-overdue tool for analysis of library event impact.

### Future enhancements

---

#### Publishing in advance

With a couple of additional columns (start time, end time), this dataset could be used as a way of publishing future events. The count of attendees would be updated once the event had finished.

This would provide the potential of having a stadard format for national event listings, allowing services and websites to use that data to promote upcoming events.

#### Additional columns

Barnet [publish data on events](https://open.barnet.gov.uk/dataset/barnet-libraries-events), including extra detail such as core/partnership events, target audience, charge, and counts of both adult and child attendees.

---

[&lt; Back to home](./)
