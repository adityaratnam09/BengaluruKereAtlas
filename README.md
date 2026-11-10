# Bengaluru Kere Atlas

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24117384.svg)](https://doi.org/10.5281/zenodo.24117384)
![Status](https://img.shields.io/badge/Status-Live-1f6f78)
![License](https://img.shields.io/badge/License-All%20rights%20reserved-lightgrey)

**Bengaluru Kere Atlas: Bengaluru's lakes, understood through data.**

**Live site: <https://adityaratnam09.github.io/BengaluruKereAtlas/>**

---

## Overview

Bengaluru Kere Atlas ("kere" is the Kannada word for lake) is an interactive atlas of
water quality in 150+ Bengaluru lakes. It is built from the monthly reports of the
Karnataka State Pollution Control Board (KSPCB), from July 2023 onward, and is updated as
each new report is published.

---

## What the project does

KSPCB samples Bengaluru's lakes every month, but the results are published as PDF tables
whose layouts keep changing. That makes it hard to see how one lake has changed, how one 
lake compares with another, or how the city as a whole is doing. This project turns 
those reports into something people can read, question and check.

**It builds one dataset from the reports.** Every monthly report is read into a single
station-by-month record. Station names are matched to a lake registry with coordinates,
and the values as reported are kept next to the standardized ones, so every number can be
traced back to its source report.

**It checks the data and says where it doubts it.** Each reading is compared with the
lake's own history, with the citywide distribution, with related measurements that should
move together, and with the conditions a reported CPCB class implies. Readings that look
wrong are flagged with a reason and a confidence level. They are never silently removed or
corrected.

**It summarizes the whole city.** Citywide trends, monitoring coverage and rankings show
which lakes are worst off on dissolved oxygen, organic pollution, nutrients, fecal
contamination, dissolved solids and metals. A **Lake Pressure Index** combines three
pressure dimensions into one screening score so lakes can be compared at a glance. Results
are set against CPCB best-use classes and BIS and IS 10500 reference limits.

**It lets you look closely at one lake.** Each lake has a map location, a latest reading,
its full monthly history, its flagged readings, and a satellite comparison between two
dated images. A guided trace follows the documented Hebbal-Nagavara cascade of connected
lakes from upstream to downstream.

**It looks for patterns across lakes and seasons.** Wetter and drier months are compared
lake by lake and citywide, and any two curated parameters can be plotted against each other
to see which pollution signals travel together.

**It connects the numbers to people and places.** Visitors can log field observations from
a lake walk, try simulated low-cost field tools, test their local knowledge with a game
and a quiz, and read how Bengaluru's lake network grew, fragmented and was encroached on.

The data refreshes as each new KSPCB report is published.

### Sections of the atlas

| Section | What it is for |
| --- | --- |
| **Explore** | Map, search, satellite compare, Lake Pressure Index and the downstream cascade trace |
| **Dashboard** | Citywide chemistry over time, coverage, rankings and distributions |
| **Lake Profile** | One lake's full monthly history, latest reading and flagged readings |
| **Analyze** | Seasonal comparison and parameter-against-parameter correlations |
| **Play** | Guess the Lake and a lake-literacy quiz |
| **Verify** | Citywide table of suspected data errors, and a field-notes log |
| **About** | The story of the lakes, background, chemistry notes, sources and methods |

### Principles

- Suspect readings are flagged and explained, not deleted.
- Each chart states what it measures and what it does not. Seasonal patterns are shown as
  associations, not causes, and turbidity is not treated as pollution.
- Regulatory thresholds are shown as fixed references, separate from statistical patterns.
- A lake with no matching KSPCB record is marked as unmonitored, never as clean or polluted.
- Field notes stay in the visitor's own browser. The atlas has no server of its own and
  needs no account.

---

## Screenshots

**Landing page**

<p align="center">
  <img src="screenshots/01_home.png" alt="Bengaluru Kere Atlas landing page" width="850">
</p>

**Dashboard: lake health at a glance**

<p align="center">
  <img src="screenshots/02_dashboard_overview.png" alt="Dashboard overview with citywide DO, BOD and COD over time" width="850">
</p>

**Lake Pressure Index: one cell per lake, banded from Good to Severe**

<p align="center">
  <img src="screenshots/03_lake_pressure_index.png" alt="Lake Pressure Index citywide picture" width="850">
</p>

**Lake Profile: every reading on file for a single lake**

<p align="center">
  <img src="screenshots/04_lake_profile.png" alt="Lake Profile page for Bellandur Lake" width="850">
</p>

**Seasonal comparison: wetter versus drier months, lake by lake**

<p align="center">
  <img src="screenshots/05_seasonal.png" alt="Seasonal comparison scatter of dry-month against wet-month dissolved oxygen" width="850">
</p>

**Data errors: suspected reporting errors across all lakes**

<p align="center">
  <img src="screenshots/06_data_errors.png" alt="Suspected data errors table" width="850">
</p>

**Mobile layout**

<p align="center">
  <img src="screenshots/07_mobile_dashboard.png" alt="Dashboard on a phone-sized screen" width="280">
</p>

---

## What is in this repository

```text
BengaluruKereAtlas/
├── index.html      # the atlas: one self-contained page, served by GitHub Pages
├── README.md
├── LICENSE
├── CITATION.cff
├── .zenodo.json
└── screenshots/
```

The data-extraction and analysis code is not published here. It is available from the
author on reasonable request.

---

## Author

Aditya Rajiv Ratnam. ORCID: [0009-0008-8354-1756](https://orcid.org/0009-0008-8354-1756)

---

## License and use

Copyright (c) 2026 Aditya Rajiv Ratnam. All rights reserved. The atlas is published for
viewing and citation. Please do not copy, modify or redistribute the page, its design or
the compiled dataset without written permission; see [LICENSE](LICENSE). The underlying
KSPCB reports are public documents of the Karnataka State Pollution Control Board.

---

## Citation

```text
Ratnam, A. R. (2026).

Bengaluru Kere Atlas [Web application]. Zenodo.

https://doi.org/10.5281/zenodo.24117384

https://adityaratnam09.github.io/BengaluruKereAtlas/
```

**Paper**

```text
Ratnam, A. R. (2026).

Urban Lake Water Quality in Bengaluru: A Data-Driven Typology.

Zenodo.

https://doi.org/10.5281/zenodo.PAPER_DOI_TO_BE_ADDED
```
