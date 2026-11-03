---
layout: default
title: Library services
description: Core details, governance, digital platforms, systems, and operating models for UK public library services
---

[< Back to home](./)

### Definition

---

A library service (or library authority) is the administrative and operational entity responsible for providing statutory public library services across a local authority area in the United Kingdom.

While the statutory responsibility rests with the local authority (under the Public Libraries and Museums Act 1964 in England & Wales, Local Government etc. (Scotland) Act 1994, and Libraries Act (Northern Ireland) 2008), delivery models include in-house council delivery, public sector mutuals, charitable trusts, joint partnerships, and outsourced leisure contractors.

This dataset provides authority-level metadata, governance models, parent council departments, consortium memberships, primary web portals, online public access catalogue (OPAC) links, digital membership registration links, public enquiry channels, social media channels, mobile app downloads, technology supplier infrastructure, direct digital lending portals (ebooks, audiobooks, magazines), mobile library timetables, computer/Wi-Fi access, and fee schedules.

### How the data can be collected

---

Library services can maintain these details at the service level. Because service-wide URLs, systems, and supplier contracts change infrequently, this dataset functions as a slow-changing reference dataset that can be published once and updated as systems, apps, or governance models evolve.

A [template file](https://github.com/LibrariesHacked/schema-librarydata/blob/master/templates/library-services.csv) is available in the templates directory.

### Sample data row

---

| Field | Sample Value |
| :--- | :--- |
| **Local authority** | Bath and North East Somerset |
| **Local authority code** | E06000022 |
| **Country** | England |
| **Local authority department** | Customer Service |
| **Governance model** | Local authority run |
| **Operating organisation** | |
| **Consortium** | LibrariesWest |
| **Service URL** | https://beta.bathnes.gov.uk/library-and-information-services |
| **Libraries URL** | https://beta.bathnes.gov.uk/find-library-or-one-stop-shop |
| **Mobile library URL** | |
| **Home library service URL** | https://beta.bathnes.gov.uk/home-library-service |
| **Childrens service URL** | https://beta.bathnes.gov.uk/childrens-library-services |
| **Catalogue URL** | https://www.librarieswest.org.uk |
| **Join online URL** | https://beta.bathnes.gov.uk/join-library-network |
| **Events URL** | https://beta.bathnes.gov.uk/library-events |
| **Eventbrite ID** | |
| **Computer access URL** | https://beta.bathnes.gov.uk/computer-access |
| **Wifi access URL** | https://beta.bathnes.gov.uk/wifi-libraries |
| **Room booking URL** | |
| **Volunteer URL** | https://beta.bathnes.gov.uk/volunteering-libraries |
| **Fees and charges URL** | https://beta.bathnes.gov.uk/library-charges |
| **Adult fine** | 0.20 |
| **Child fine** | 0.00 |
| **Fine interval** | Day |
| **Email address** | councilconnect@bathnes.gov.uk |
| **Phone number** | 01225 394041 |
| **App name** | LibrariesWest |
| **Android app URL** | https://play.google.com/store/apps/details?id=uk.co.solus.librarieswest |
| **iOS app URL** | https://itunes.apple.com/us/app/librarieswest/id935637390 |
| **Twitter URL** | https://twitter.com/BathnesL |
| **Facebook URL** | https://www.facebook.com/BathnesLibraries1 |
| **Instagram URL** | https://www.instagram.com/bathnes_libraries |
| **YouTube URL** | |
| **Blog URL** | |
| **Podcast URL** | |
| **Library management system supplier** | SirsiDynix |
| **Library management system** | Symphony |
| **Online catalogue system** | Enterprise |
| **Ebook supplier** | Bibliotheca |
| **Ebook URL** | https://www.librarieswest.org.uk/ebooks |
| **Audiobook supplier** | Bolinda |
| **Audiobook URL** | https://fe.bolindadigital.com/wldcs_bol_fo/b2i/mainPage.html?b2bSite=6431 |
| **Emagazine supplier** | PressReader |
| **Enewspaper supplier** | PressReader |
| **Online reference subscriptions** | Ancestry Library Edition; Findmypast; British Newspaper Archive |
| **Green library** | Yes |
| **Notes** | |

A dataset of all 208 UK library authorities can be viewed at [library_services.csv](https://github.com/LibrariesHacked/schema-librarydata/blob/master/data/library_services.csv).

### Field notes

---

#### Local authority code

The Government Statistical Service (GSS / ONS) 9-character code identifies the statutory authority uniquely (e.g. `E06000026` for Plymouth, `E09000003` for Barnet, `S12000049` for Glasgow City, `W06000015` for Cardiff, `N92000002` for Northern Ireland). This serves as the primary key for the service and the foreign key for all branch libraries in the [libraries dataset](./libraries).

#### Country

Specifies which UK nation the authority is located in: `England`, `Scotland`, `Wales`, or `Northern Ireland`.

#### Governance model & Operating organisation

- **Governance model**: The overarching operating model:
  - `Local authority run`: In-house council service.
  - `Public sector mutual`: Public service mutual / staff-led trust (e.g. *Libraries Unlimited*, *Explore York*, *Suffolk Libraries*, *Inspire*).
  - `Charitable trust`: Leisure/cultural trust (e.g. *OnFife*, *Glasgow Life*, *Live Borders*, *High Life Highland*).
  - `Commissioned contractor`: Outsourced commercial or social enterprise partner (e.g. *Greenwich Leisure Limited / Better*).
- **Operating organisation**: The legal name of the delivering body if not operated in-house.
- **Local authority department**: The council directorate overseeing the service (e.g. *Community Solutions*, *Place*, *Public Health*).

#### Consortia and shared services

Several library authorities share LMS infrastructure, catalogues, or mobile apps through regional consortia (e.g. *LibrariesWest*, *The Libraries Consortium (TLC)*, *SELMS*, *Libraries NI*). In these cases, catalogue and mobile app URLs will point to the shared regional portal rather than an individual council URL.

#### Public Service Delivery Channels & Specialized URLs

- **Join online URL**: Direct URL enabling residents to register online for immediate digital or physical borrowing.
- **Mobile library URL**: Web page detailing mobile library schedules, routes, and timetables.
- **Home library service URL**: Page detailing book delivery options for homebound patrons.
- **Childrens service URL**: Dedicated page for early literacy, storytimes, and children's collections.
- **Computer access URL & Wifi access URL**: Public IT facilities, booking systems, and Wi-Fi access details.
- **Events URL**: Central What's On / Eventbrite listing for library workshops, author talks, and children's activities.
- **Fees and charges URL**: Detailed tariff of library fees, reservations, room hire, and printing costs.
- **Adult fine & Child fine**: Standard daily overdue charges in GBP (0.00 for fine-free services).

#### Digital Content Suppliers & Direct URLs

- **Ebook URL & Audiobook URL**: Direct links to the service's digital lending portals (e.g. OverDrive, BorrowBox, cloudLibrary) alongside the supplier names.
- **Emagazine & Enewspaper suppliers**: Digital press providers (*PressReader*, *NewsBank*, *Libby*).
- **Online reference subscriptions**: Major digital research tools provided for free to patrons (e.g. *Ancestry Library Edition*, *Findmypast*, *British Newspaper Archive*, *Theory Test Pro*, *BFI Replay*).

#### Social Media & Audio Channels

Direct profile URLs for official service accounts on `Twitter URL` (X), `Facebook URL`, `Instagram URL`, `YouTube URL`, `Blog URL`, and `Podcast URL`.

### How the data is updated

---

This reference dataset is updated whenever an authority changes suppliers, re-procures an LMS or digital content contract, launches a new app, or adopts a new operating model.

---

[< Back to home](./)
