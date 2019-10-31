---
layout: default
title: Events
description: Library event attendance and outcomes
---

### Definition

---

A library event is an event held within a library, and facilitated or organised by the library service. Each event should be listed.

### How the data can be collected

---

Data collection on events is likely to be manual, but could be helped by existing booking systems, such as Eventbrite. Or be recorded in custom spreadsheets and databases. For example, Barnet collect (and publish) event data using a custom Access database.

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

We should look at options to:

- Assign multiple outcomes
- Have an option for leaving this empty or unknown
- Have guidance for common event types that suggests which outcomes to use

#### Non-library events

The definition of library events as being 'facilitated or organised by the library service' is broad. This means library services may include events that others wouldn't. For example, reading groups that are largely self-organised, but use library premises and books. For now, if the library is collecting data on the events, and counts of attendees, this will left to the discretion of the service.

### How the data is updated

---

To update their event data, library services can either:

- Publish an additional file with the new set of events
- Update an existing file with each new event as an additional row

Depending on how many events the service holds, a new file may be easier to manage. It is likely that this data will collected as the events are held, so we should explore guidance for updating this data regularly (e.g. monthly).

### How the data could be used

---

An example of what could be done with the data.

### Future enhancements

---

#### Publishing in advance

With a couple of addtional columns (start time, end time), this dataset could be used as a way of publishing future events. The count of attendees would then be updated once the event had finished.

This would provide the potential of having a stadard format for national event listings, allowing services and websites to use that data to promote upcoming events.

#### Additional columns

Barnet [publish data on events](https://open.barnet.gov.uk/dataset/barnet-libraries-events) that includes extra detail such as core and partnership events, target audience, charge, and counts of both adult and child attendees.

---

[&lt; Back to home](./)
