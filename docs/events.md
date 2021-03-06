---
layout: default
title: Events
description: Library event attendance and outcomes
---

[&lt; Back to home](./)

### Definition

---

A library event is an event facilitated or organised by the library service. Each event should be listed.

### How the data can be collected

---

Data collection on events is likely to be manual, but could be aided by reports from existing systems, such as Eventbrite. Or recorded in custom spreadsheets and databases. For example, Barnet collect event data using a Microsoft Access database, which can then be exported as CSV.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/events.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| Local authority | Library name | Event date | Name | Main outcome | Secondary outcome | Attendees |
| --------------- | ------------ | ---------- | ---- | ------------ | ----------------- | --------- |
| Barnet | Burnt Oak | 2018-01-12 | Toddler Read and Rhyme | Stronger more resilient communities | Increased reading and literacy | 11 |

An example for an earlier version of this dataset can be viewed at [Barnet events](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/events_barnet.csv).

### Field notes

---

#### Library name

If the event is not held in a library: use "Outreach" in this column and add the location to the event name.

See an example below.

| Local authority | Library name | Event date | Name | Main outcome | Secondary outcome | Attendees |
| --------------- | ------------ | ---------- | ---- | ------------ | ----------------- | --------- |
| Newcastle | Outreach | 2019-07-23 | Copyright for Newcastle City Learning tutors at Westgate College | Helping everyone achieve their full potential | Greater prosperity | 5 |

#### Main outcome

The outcomes are taken from the Libraries Taskforce Ambition document: [outcomes libraries deliver for their communities](https://www.gov.uk/government/publications/libraries-deliver-ambition-for-public-libraries-in-england-2016-to-2021/libraries-deliver-ambition-for-public-libraries-in-england-2016-to-2021#the-outcomes-libraries-deliver-for-their-communities). A main outcome should be selected for each event.

| Outcome |
| ------- |
| Cultural and creative enrichment |
| Increased reading and literacy |
| Increased digital access and literacy |
| Helping everyone achieve their full potential |
| Healthier and happier lives |
| Greater prosperity |
| Stronger more resilient communities |

#### Secondary outcome

The secondary outcome is optional. Some events will clearly fit under one outcome; this column should be used for events that fit under multiple outcomes.

See related "multiple or unknown outcomes" problem below.

### Potential problems

---

#### Multiple or unknown outcomes

It could be difficult for a library service to assign an outcome to each event. It's also likely that events could apply to multiple outcomes. In these cases, just one should be selected. This may lead to situations where the same events are assigned under different outcomes.

We should investigate options to:

- Assign multiple outcomes (e.g. "Healthier and happier lives,Stronger more resilient communities")
- Have an option for leaving this empty or unknown
- Have guidance for common events that suggests the outcome(s) to use

#### Non-library events

The definition of library events as being 'facilitated or organised by the library service' is broad. This means library services may include events that others wouldn't. For example, reading groups that use library premises and books. For now this will left up to the service.

### How the data is updated

---

To update their event data, library services can either:

- Publish an additional file with the new set of events
- Update an existing file with each new event as an additional row

Depending on how many events the service holds, a new file may be easier to manage.

### How the data could be used {#usage}

---

#### Locally

Comprehensive data on events, alongside usage data such as loans, will be a long-overdue tool for reporting on the full impact of libraries.

The Barnet events data, filtered by those in 2019, shows the scale of attendance at different types of library events. Particularly the popularity of those such as Rhyme Time.

<figure>
    <img src="{{site.url}}/images/events_barnet.png" alt="Bubble chart displaying barnet events by type." width="100%"/>
    <figcaption>2019 attendees at Barnet library events held grouped by event type.</figcaption>
</figure>

Reporting events alongside loans provides a way to recognise different aspects of library usage as being equally valid.

#### Nationally

Event data could be used to list and publicise events that are happening across library services.

People may not be particularly interested in what is happening in their local authority. They want to know what is happening near to them. If services can publish standard event data we can list events ahead of time, and show these by library, regardless of authority. This would be especially useful during times of national events, such as World Book Day, and the Summer Reading Challenge (see future enhancements, below).

### Future enhancements

---

#### Publishing in advance

With a couple of additional columns (start time, end time), this dataset could be used as a way of publishing future events and publicising these across library services. The count of attendees would be updated once the event had finished.

#### Additional columns

Barnet [publish data on events](https://open.barnet.gov.uk/dataset/barnet-libraries-events), including extra detail such as core/partnership events, target audience, charge, and counts of adult and child attendees.

---

[&lt; Back to home](./)
