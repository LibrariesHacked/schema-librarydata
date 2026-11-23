---
layout: default
title: Libraries
description: Library location opening hours, coordinates, facilities, and contact details
---

[< Back to home](./)

### Definition

---

A library is a static service point which provides access to library services for the general public. This does not include mobile libraries, which are covered in the [mobile library stops dataset](./mobile-library-stops).

### How the data can be collected

---

Library services will be able to use the [public library basic dataset](https://www.gov.uk/government/publications/public-libraries-in-england-basic-dataset) (managed by Arts Council England / DCMS) and local authority records as a starting point, which includes similar fields.

If starting from scratch, [this template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/libraries.csv) can be downloaded and opened using spreadsheet software.

### Sample data row

| local_authority | local_authority_code | library_name | library_code | address_1 | address_2 | address_3 | town | postcode | unique_property_reference_number | latitude | longitude | status | statutory | facility_type | type_of_library | year_opened | year_closed | temporary_closed_until | monday_staffed_hours | tuesday_staffed_hours | wednesday_staffed_hours | thursday_staffed_hours | friday_staffed_hours | saturday_staffed_hours | sunday_staffed_hours | monday_unstaffed_hours | tuesday_unstaffed_hours | wednesday_unstaffed_hours | thursday_unstaffed_hours | friday_unstaffed_hours | saturday_unstaffed_hours | sunday_unstaffed_hours | special_hours | weekly_staffed_hours | weekly_total_hours | automated_access_system | co_located | co_located_with | guest_wifi | member_wifi | public_computers | printing | meeting_rooms | cafe | quiet_study_space | makerspace | step_free_access | accessible_toilet | baby_changing | changing_places_toilet | hearing_loop | sensory_space | accessible_parking | facilities_and_services | phone_number | email_address | url | catalogue_url | join_online_url | virtual_tour_url | notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Plymouth | E06000026 | Crownhill Library | PLY-CRO | Cross Park Road | Crownhill |  |  | PL6 5AN | 100041062012 | 50.4124 | -4.1345 | Open | Yes | Static library | LAL | 1991 |  |  | 08:30-18:00 | 08:30-18:00 | 08:30-18:00 | 08:30-20:00 | 08:30-18:00 | 09:00-17:00 |  |  |  |  |  |  |  |  |  | 57.5 | 57.5 |  | No |  | Yes | Yes | Yes | Yes | No |  | Yes |  | Yes | Yes |  |  | Yes |  |  | Books; Free Wi-Fi; Public computers; Printing; Quiet study space | 01752 305900 | library@plymouth.gov.uk | https://www.plymouth.gov.uk/libraries/findlibraryandopeninghours/crownhilllibrary |  |  |  |  |

An example of this dataset can be viewed at [Plymouth libraries](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/libraries_plymouth.csv).

### Field notes

---

#### Local authority code (`local_authority_code`)

The Government Statistical Service (GSS / ONS) 9-character code for the local authority (e.g. `E06000026` for Plymouth). This links directly to the parent [library services dataset](./library-services).

#### Library name (`library_name`)

You should list all libraries managed by your service. Independent libraries such as community-managed are not expected to be included unless they are part of a transition or service agreement.

If however you are updating the dataset and a library that used to be listed as managed by your service has since become independent, we recommend you still include it. In this case use the Type of library as ICL (Independent Community Library). You may then omit this library from your list in future updates.

#### Status (`status`)

The current operational status of the service point:
- `Open`: Currently operational.
- `Closed (permanent)`: Permanently closed.
- `Closed (temporary)`: Temporarily closed (e.g. for refurbishment, relocation, or emergency).
- `Planned`: Planned new library branch not yet opened.

#### Coordinates and Spatial Identifiers (`latitude`, `longitude`, `unique_property_reference_number`)

- **Latitude and Longitude**: Coordinates in WGS84 decimal degrees (e.g. 50.4124, -4.1345). Enables immediate mapping in web map tools without requiring geocoding.
- **Unique Property Reference Number (UPRN)**: The unique numeric identifier assigned by the local authority to the building unit, stored as an integer without leading zeros.

#### Statutory (`statutory`)

All statutory libraries should be listed with `Yes`. Non-statutory service points are indicated with `No`.

#### Facility type (`facility_type`)

The physical type of service point (aligned with the Arts Council England taxonomy):
- `Static library`: A permanent physical library building open to the public.
- `Static local history library`: A dedicated physical local history or special collection library.
- `Archive`: A public archive record office or heritage centre.
- `Mobile library`: A mobile library vehicle base or stop coordination point.
- `Prison library`: A library service operating within a prison or custodial establishment.

#### Type of library (`type_of_library`)

The governance and operating model of the public library branch:

| Code | Title | Description |
| ---- | ----- | ----------- |
| LAL | Local authority library | Library building funded, run and managed by local authority staff |
| LAL- | Local authority library (-) | As LAL, but unstaffed, for example, a book drop |
| CL | Commissioned library | Running of the library building/service has been transferred from the council to a separate trust or organisation. The local authority are still accountable for the service.|
| CRL | Community run library | Library with some level of ongoing support from the council. Work according to a joint agreement such as a Service Level Agreement, Memorandum of Understanding or contract. Staff are volunteers, but some form of support is available. May or may not be counted as part of the statutory service. |
| ICL | Independent community library | Library that has been transferred to the management of a non local authority body, either community group or third party, which is outside the local authority network. |

#### Staffed and Unstaffed hours

- **Staffed hours**: Hours when library staff or trained personnel are present to assist visitors.
- **Unstaffed hours**: Extended access hours where visitors access the space using automated systems (e.g. Open+ card and PIN access) without library staff present.
- Hours are specified in 24-hour clock format (e.g. `09:00-17:00`), with split sessions separated by commas (e.g. `09:00-12:00,13:00-17:00`).
- **Weekly staffed hours / Weekly total hours**: Numerical sum of regular hours open each week, providing rapid metrics for national benchmarking.
- **Automated access system**: The automated access technology used to support visitors during unstaffed hours (e.g. `Open+`, `Lyngsoe`, `Self-service kiosk`).

#### Co-location (`co_located`, `co_located_with`)

Libraries that share buildings with other community or public services should be indicated with `Co-located: Yes`.

In **`Co-located with`**, separate multiple co-located partners with a **semicolon (`;`)**. To promote standardisation across services, use the Arts Council England categories as a controlled vocabulary, augmented with specific organisation names:
* `Archives`
* `Arts centre`
* `Care home / hostel`
* `Catering / bars / pub`
* `Civic` (e.g. council customer services, town hall, registry office)
* `Community` (e.g. community centre, village hall)
* `Faith buildings`
* `Health` (e.g. GP surgery, clinic)
* `Hotel`
* `Industrial / business` (e.g. enterprise centre)
* `Library` (e.g. academic or partner library)
* `Museum` / Gallery
* `Retail` (e.g. post office, shop)
* `Schools & colleges`
* `Universities & higher education`
* `Other` (e.g. police contact point, nursery)

*Example*: `"Civic; Community; Council customer services; Pre-school nursery"`

#### Wi-Fi Access (`guest_wifi`, `member_wifi`)

- **Guest wifi**: Whether free public Wi-Fi is accessible to any visitor immediately without needing a library card/membership (`Yes`/`No`).
- **Member wifi**: Whether Wi-Fi is provided that requires library membership (card number and PIN login) (`Yes`/`No`).

#### Facilities and Amenities

- **Public computers**: Whether public access desktop PCs with internet are available for visitors (`Yes`/`No`).
- **Printing**: Whether printing, photocopying, or document scanning is available for public use (`Yes`/`No`).
- **Meeting rooms**: Whether meeting rooms, study rooms, or hireable community spaces are available (`Yes`/`No`).
- **Quiet study space**: Whether dedicated quiet study spaces or desk carrels with power outlets are available (`Yes`/`No`).

#### Physical Accessibility

- **Step-free access**: Level access or ramp/lift access for wheelchairs and pushchairs (`Yes`/`No`/`Partial`).
- **Accessible toilet**: Whether an accessible wheelchair-friendly public toilet or Changing Places facility is available (`Yes`/`No`).
- **Hearing loop**: Whether an induction loop / hearing loop system is installed for hearing aid users (`Yes`/`No`).

#### Facilities and Services

- **Facilities and services**: A semicolon-separated list of all public amenities, services, and digital subscriptions available at the branch, directly supporting digital discovery platforms like LibraryOn (e.g. `Books; Printing; Free Wi-Fi; Public computers; Findmypast; British Newspaper Archive; BFI Replay; Meeting rooms`).

### How the data is updated

---

Each service can maintain a single data file that is updated whenever details change. Closed libraries can be retained with Status `Closed (permanent)` and `Year closed` to preserve historical continuity.

---

[< Back to home](./)
