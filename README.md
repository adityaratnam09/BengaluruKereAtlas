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
each new report is published. The source reports are published on the
[KSPCB water monitoring page](https://kspcb.karnataka.gov.in/environmental-monitoring/water).

---

## Getting started

Here are some ways to use the atlas. The tabs can be used in any order.

**Explore: start from the map.**
1. Search for a lake by name, or find it on the map.
2. Switch the marker colors between the reported class and the Lake Pressure Index to see
   the same lakes through two different lenses. With the index selected, use the minimum
   score slider to hide lakes below a score and focus on the most stressed ones.
3. Select a lake to see its latest reading, and use the satellite comparison to look at
   the lake between two dates.
4. Follow the cascade trace to move through a chain of connected lakes, upstream to
   downstream, and compare the reported conditions along the chain.

**Dashboard: start from the city.**
1. Read the citywide trends first. They show how oxygen demand, nutrients and other
   indicators have moved month by month.
2. Use the best-off and worst-off rankings to see which lakes stand out for a given
   indicator, and the distributions to see how a single lake sits within the city.
3. Open a lake's profile from a ranking to see the history behind its position.

**Analyze: start from a question.**
1. Use the seasonal comparison to ask whether a lake does better or worse in wetter months
   than in drier ones, lake by lake or for the city as a whole.
2. Use the parameter-against-parameter plots to explore relationships between
   measurements, such as dissolved oxygen and organic load, or nitrate and phosphate. Read
   what the plot shows, then read the note on associations under "How to read the data"
   below.

**Verify: start from a doubt.**
1. If a number in a chart or profile looks too high or too low, open the data-errors table
   to see whether it was flagged and why.
2. Sort the table by column, filter it with the boxes under each heading, or search for a
   lake, then open the lake's profile to see the flagged reading in context.
3. Use the field-notes log to record what you see on a lake walk. Observations are a
   useful complement to the reported values, but they cannot confirm or refute a
   laboratory measurement.

---

## What the project does

KSPCB publishes water-quality monitoring results for Bengaluru's lakes in monthly PDF
reports, but the reports vary in layout and coverage. That makes it hard to see how one
lake has changed, how one lake compares with another, or how the city as a whole is doing.
This project turns those reports into something people can read, question and check.

**It builds one dataset from the reports.** Each monthly report is processed into
station-by-month records. Station names are matched to a lake registry with coordinates,
and the originally reported values are retained alongside the standardized values, so
every measurement can be traced to its source.

**It checks the data and says where it doubts it.** Applicable checks compare each reading
with the lake's own history, with the citywide distribution, with related measurements
that should move together, and with the conditions a reported CPCB class implies. Readings
that appear inconsistent are flagged with a reason and a confidence level. Original values
are retained, and suspected errors are never silently corrected.

**It summarizes the whole city.** Citywide trends, monitoring coverage and rankings reveal
which lakes show the greatest impairment across indicators of oxygen availability, organic
pollution, nutrient enrichment, fecal contamination, dissolved solids and metals. A
**Lake Pressure Index** combines three pressure dimensions into one screening score so
lakes can be compared at a glance. Results are compared with CPCB designated-best-use
criteria and relevant reference limits from BIS IS 10500.

**It lets you look closely at one lake.** Each monitored lake has a map location, its
latest available reading, monthly history, flagged readings and a satellite comparison
between two dated images. A guided trace follows the documented Hebbal-Nagavara cascade of
connected lakes from upstream to downstream.

**It looks for patterns across lakes and seasons.** Wetter and drier months are compared
lake by lake and citywide, and any two curated parameters can be plotted against each
other to see which pollution signals travel together.

**It connects the numbers to people and places.** Visitors can log field observations from
a lake walk, try simulated low-cost field tools, test their local knowledge with a game
and a quiz, and read how Bengaluru's lake network grew, fragmented and was encroached on.

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

### How to read the data

- Regulatory thresholds are shown as fixed references, separate from statistical patterns.
- A lake with no matching KSPCB record is marked as unmonitored, never as clean or
  polluted.
- Field notes stay in the visitor's own browser. The atlas has no server of its own and
  needs no account.

Some limits matter when reading any chart:

- **"Latest" is not "current".** A lake's latest reading is the most recent value KSPCB
  reported for that lake. It is not a measurement made today, and it can come from an
  earlier month than another lake's latest reading, because lakes are reported on
  different schedules and some months have no report at all. Check the month shown beside
  a value before treating it as the lake's present condition.
- **A ranking depends on the indicator.** The lakes that look worst for dissolved oxygen
  are not always the worst for nutrients, fecal contamination or dissolved solids. A
  lake's position changes with the indicator, the month and the number of readings behind
  it, so a rank describes one view of the data, not an overall verdict on a lake.
- **Seasonal relationships are associations, not causes.** A pattern between wetter and
  drier months, or between two parameters that rise together, shows that they move
  together. It does not show that one drives the other, or that rainfall is the reason.
- **Coverage is uneven.** Some parameters, such as metals, are measured only a few times a
  year, and some months or lakes have gaps. Averages and scores built on fewer readings
  deserve more caution.
- **Reference limits are benchmarks.** Thresholds shown on the charts are used for
  comparison. Staying under one does not certify water as safe to drink, bathe in or
  support aquatic life.

---

## Understanding the Lake Pressure Index

The **Lake Pressure Index** (LPI) is a screening score. It condenses several measurements
for one lake in one month into a single number, so that lakes can be compared and tracked
at a glance. It summarizes the water-quality pressure indicated by the reported
measurements. It does not classify the lake.

**What goes into it.** The score uses six inputs, grouped into three dimensions:

| Dimension | Inputs |
| --- | --- |
| Oxygen and organic load | Dissolved oxygen, BOD |
| Nutrients and ammonia | Ammoniacal nitrogen, nitrate, phosphate (treated as phosphorus, P; reporting basis unconfirmed) |
| Fecal contamination | Fecal coliform |

COD and pH do not enter the score, and neither does the class reported by KSPCB.

**How it is calculated.**
1. Each input is compared with a benchmark. For most inputs, a reading at its benchmark
   scores 100. Readings below the benchmark score proportionally, while those above it
   follow a logarithmic scale to limit the influence of extreme values. Scores are capped
   at 300. Dissolved oxygen is handled in reverse because lower concentrations indicate
   greater oxygen stress: it scores zero at 8 mg/L or more, 100 at the benchmark, and 300
   at zero.
2. The available inputs are averaged within each dimension.
3. The dimension scores are averaged with equal weight, so a dimension with one input,
   such as fecal contamination, counts as much as one with three.
4. The dimension with the highest score is shown as the **main driver**, so that a
   high-pressure dimension stays visible even when averaging lowers the overall score. The
   term refers to the largest dimension score, not to a demonstrated cause of pollution.

If a month lacks some inputs, the score uses the ones that are available, and is marked
partial. Missing readings are left out rather than filled in, and a month with no valid
dimension gets no score. Partial scores may be based on different parameters or
dimensions, so comparisons between lakes or months should take their completeness into
account. This matters most when ranking lakes by LPI on the map.

**How the score is read.**

| Score | Band |
| --- | --- |
| Below 50 | Good |
| 50 to 100 | Fair |
| Above 100, up to 150 | Poor |
| Above 150, up to 200 | Very poor |
| Above 200 | Severe |

These bands describe pressure indicated by selected water-quality measurements, not
overall lake health. The cut-offs are fixed and do not depend on how other lakes score.

Because the overall score is an average, 100 does not mean that every input is at its
benchmark. Comparisons between lakes use each lake's most recent scorable month within the
latest twelve months of the dataset. Lakes whose last score is older than that are left
out of the comparisons, and their histories remain available in the lake profile.

**Why it is not a CPCB classification.** CPCB's designated-best-use classification system
categorizes water according to prescribed use-related criteria. The classes reported by
KSPCB are separate from the LPI, which is calculated independently from measured
parameters. In more detail:
- It is a project index built for comparison and tracking. It is not an official
  classification, and it is calculated from the readings alone, without reference to the
  class that KSPCB reports for a station.
- Its benchmarks are drawn from several places: CPCB criteria for dissolved oxygen, BOD
  and ammonia, a BIS drinking-water limit for nitrate, a desirable bathing-water level for
  fecal coliform, and a project anchor for phosphorus. Some of these are used only as
  comparison points and were not set as ecological thresholds. The phosphate anchor, for
  example, is an empirical reporting limit. KSPCB's phosphate values are used as reported,
  with no conversion, on the assumption that they are expressed as P, which the reports do
  not confirm.
- A lake can therefore have a high LPI and a favorable reported class, or the reverse. The
  two measure different things, and neither replaces the other.
- It does not certify that water is safe to drink, bathe in or sustain aquatic life.

The benchmarks, formulas and sources are listed in full under the Sources and Methods
section of the atlas.

---

## Understanding data-quality flags

KSPCB's reports are PDF tables whose layouts change from month to month, and some of the
values in them appear inconsistent. The atlas applies the checks that are relevant to each
reading and flags potential inconsistencies for further examination. Not every parameter
has a cross-parameter or class test. The flags appear in the **Verify** table and on each
lake's profile.

**Why anomalous readings are flagged and not removed.**
- A flag is a suspicion and not a finding. Without access to the laboratory records, the
  atlas cannot tell whether a strange value is a typing error, a unit problem, a parsing
  problem or a real pollution event, and real events are often the most important readings
  in a lake's history.
- Deleting a reading would hide that judgment from the reader. Keeping it, with the reason
  it was flagged, lets anyone examine the evidence and decide.
- Flagged readings stay in the data and are listed in the Verify table with the reason
  they were flagged. How much an extreme reading matters then depends on the view. Where
  Dashboard rankings and citywide trends use medians, as the BOD, fecal coliform and
  turbidity rankings and the citywide time series do, individual extreme readings have
  limited influence. Other views, such as the dissolved oxygen best-off and worst-off
  lists, use each lake's latest reading, so an unusual latest value can move a lake's
  position.
- Extreme values are displayed so that they stay visible without flattening the rest of a
  chart. Lake profiles plot individual readings, and the coliform chart uses a log scale
  so that values from single digits to millions can share one axis. A scatter plot pins a
  point beyond its axis range to the edge and rings it, with the actual values shown in
  the detail strip, and the total dissolved solids histogram collects the rarest high
  values in a final overflow bar.
- Original reported values are preserved. Corrections to extracted or standardized values
  are made only where supported by the source report or a documented extraction rule.
  Otherwise, a suspected error, such as a misplaced decimal point, is described in the
  flag without changing the reported value.

**What the checks compare.** A reading is compared with:
- the lake's own history;
- the citywide distribution for the same parameter;
- related measurements that should move together or that can be recomputed from each
  other, such as hardness against its calcium and magnesium components, a sodium
  adsorption ratio recalculated from its ions, or fecal coliform against total coliform;
- the conditions that a reported CPCB class requires. For a station reported as Class D,
  for example, the atlas tests whether the month's measurements meet the minimum
  conditions for that class. A failure is flagged as a mismatch between the reported class
  and the measured water quality. It is not a reclassification, and it does not by itself
  show that the reported class is wrong.

**What the confidence levels mean.** Every flag carries a confidence level of high or
medium.
- **High** means the evidence is strong. The reading conflicts with something that can be
  checked independently, such as a calculation that does not add up or a relationship that
  cannot hold in practice.
- **Medium** means the reading is unusual compared with the lake's history or the rest of
  the city, but could still be genuine. These are the ones to look at with the most
  curiosity and the least assumption.

Neither level means a reading is confirmed wrong. Both mean "worth a second look", and the
reason given with each flag shows what the check found.

---

## Screenshots

**Landing page**

<p align="center">
  <img src="screenshots/01_home.png" alt="Bengaluru Kere Atlas landing page" width="850">
</p>

**Dashboard: citywide water-quality trends**

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

---

## Author

Aditya Rajiv Ratnam. ORCID: [0009-0008-8354-1756](https://orcid.org/0009-0008-8354-1756)

---

## License and use

Copyright (c) 2026 Aditya Rajiv Ratnam. All rights reserved. The atlas is published for
viewing and citation. Please do not copy, modify or redistribute the page, its design or
the compiled dataset without written permission; see [LICENSE](LICENSE). The underlying
KSPCB reports are public documents of the Karnataka State Pollution Control Board,
available from its
[water monitoring page](https://kspcb.karnataka.gov.in/environmental-monitoring/water).

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
