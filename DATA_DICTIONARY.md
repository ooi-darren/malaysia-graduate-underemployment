# Data Dictionary

This document defines every variable used in the "Malaysia's Graduate (Un)employment" analysis. Every dataset is classified as **PUBLIC** (published directly by an official source, fetched and read this session), **DERIVED** (calculated by this session from a PUBLIC source), or **ESTIMATED** (third-party or secondary-cited figures, not independently verified against a primary document this session could read).

**A separate "Why Is This Happening?" section at the end of most notebooks adds qualitative context** — secondary-sourced explanations (news reporting, academic analysis) for the mechanism behind each quantitative finding. That content is deliberately *not* classified PUBLIC/DERIVED/ESTIMATED like the datasets below, since it's explanatory reporting rather than a number this project is asserting — full citations are in [`references/SOURCES.md`](./references/SOURCES.md) under "Context / Secondary Sources."

---

## national_unemployment_1982_2023.csv

**Source:** DOSM, Annual Principal Labour Force Statistics (`lfs_year`), fetched directly from `storage.dosm.gov.my`.
**Classification:** PUBLIC
**Coverage:** 1982–2023, annual, national.
**Description:** Malaysia's labour force size, employment, unemployment, and unemployment rate, national level.

### Known limitations
- This series was not yet updated to 2024/2025 as of this session — the more recent national rate (3.2% in 2024, ~3.0% in 2025) is cited from secondary reporting in `graduate_vs_national_unemployment.csv` and in-notebook text, not from this file.

## graduate_vs_national_unemployment.csv

**Source:** DOSM, *Graduates Statistics 2024* (PDF report), cited via secondary web reporting — the primary PDF was fetched this session but could not be machine-read (binary/compressed format; no PDF-rendering tool was available in this environment).
**Classification:** DERIVED/ESTIMATED — real DOSM-reported figures, but sourced from a secondary summary rather than read page-by-page from the primary document.
**Coverage:** 2023, 2024 only — this is the full window DOSM's published comparison covers.
**Description:** Graduate-specific unemployment rate vs. the national unemployment rate, plus total graduate population and Graduate Labour Force Participation Rate (GLFPR) for 2024.

### Known limitations
- **Only two years are available.** DOSM's Graduates Statistics report is annual; this session could not access a longer back-series in machine-readable form.
- **The primary PDF could not be independently verified this session** — figures are as reported by secondary sources (DOSM's own press materials, cited in web search results), not cross-checked against the original document's tables directly.

## youth_unemployment_2016_2026.csv

**Source:** DOSM, Monthly Youth Unemployment (`lfs_month_youth`), fetched directly from `storage.dosm.gov.my`.
**Classification:** PUBLIC, with a corrected column mapping (see below).
**Coverage:** January 2016 – June 2026, monthly, national.
**Description:** Unemployed persons and unemployment rate for the 15–24 and 15–30 age bands.

### Known limitations — a real data-quality issue, verified and corrected
**The published CSV's column headers do not match its actual data**, specifically for the second and third columns. The source file's header reads `unemployed_15_24, u_rate_15_24, unemployed_15_30, u_rate_15_30`, but the *values* in the `u_rate_15_24` and `unemployed_15_30` positions are swapped relative to those labels — confirmed by cross-checking against independently reported figures:
- December 2024: the value in the `u_rate_15_24`-labelled column reads 400.7 (impossible as a percentage); the value in the `unemployed_15_30`-labelled column reads 10.4 — which matches DOSM's own press-reported "10.3% youth (15–24) unemployment rate for 2024" almost exactly.
- October 2025: the same swapped-position value reads 10.1, matching DOSM's own press-reported "10.1% in October 2025" for the 15–24 rate exactly.

This project's processed file (`youth_unemployment_2016_2026.csv`) uses the **corrected** mapping: `unemployed_15_24_thousand`, `unemployed_15_30_thousand` (from the mislabeled `u_rate_15_24` position), `u_rate_15_24_pct` (from the mislabeled `unemployed_15_30` position), `u_rate_15_30_pct`. The raw, uncorrected file is preserved in `data/raw/` for anyone who wants to verify this independently.

## skills_underemployment_by_age.csv

**Source:** DOSM, Skills-Related Underemployment by Age (`lfs_qtr_sru_age`), fetched directly from `storage.dosm.gov.my`.
**Classification:** PUBLIC
**Coverage:** Q1 2017 – Q3 2025, quarterly, national, by age band (15–24, 25–34, 35–44, 45+, overall).
**Description:** Share of employed, tertiary-educated workers in a semi-skilled or low-skilled occupation (DOSM's own occupational classification).

### Known limitations
- **This is quarter-to-quarter volatile, not a smooth trend** — the 15–24 series swung from 58.1% to 80.0% within four quarters (2022 Q2 to 2023 Q4). This project reports the range and the persistent gap versus the overall rate rather than overstating a single before/after comparison as a clean trend.
- **"Semi-skilled or low-skilled" is an occupational classification, not a judgment about job quality or satisfaction** — see Notebook 03's Confidence & Caveats.

## state_unemployment_quarterly.csv

**Source:** DOSM, Quarterly Principal Labour Force Statistics by State (`lfs_qtr_state`), fetched directly from `storage.dosm.gov.my`.
**Classification:** PUBLIC
**Coverage:** Q1 2017 – Q3 2025, quarterly, all 16 states/federal territories.
**Description:** Labour force, employment, unemployment, and participation rate by state.

## state_gdp_sector_2024.csv

**Source:** DOSM, State GDP by Sector at constant prices (`gdp_state_real_supply`), plus the sector code lookup table (`gdp_lookup`), fetched directly from `storage.dosm.gov.my`.
**Classification:** DERIVED — the six top-level sector values (Total, Agriculture, Mining, Manufacturing, Construction, Services) were filtered from a much larger sub-sector file and pivoted to wide format; manufacturing and services shares were then calculated by this session.
**Coverage:** 2024, all 16 states/federal territories.
**Description:** Each state's GDP by top-level economic sector, plus manufacturing and services share of total state GDP.

## state_lecturers_2023.csv

**Source:** DOSM, Lecturers in Public Universities by state (`lecturers_uni`), fetched directly from `storage.data.gov.my`.
**Classification:** DERIVED — summed by this session across every individually named public university per state (the source file's own "All Universities" subtotal rows are only populated for 4 of 14 states, so a full-coverage total had to be built by summing named-university rows directly).
**Coverage:** 2023, 14 states with at least one public university (Labuan and Putrajaya have none).
**Description:** Total public-university lecturer count per state — used in this project as a rough proxy for local higher-education institutional presence, not as a direct measure of graduate output or student enrolment (no public, state-level dataset for either was found this session).

## district_unemployment_2024.csv

**Source:** DOSM, Annual Principal Labour Force Statistics by District (`lfs_district`), fetched directly from `storage.dosm.gov.my`.
**Classification:** PUBLIC
**Coverage:** 2024, 162 districts across 12 states (Perlis, W.P. Kuala Lumpur, W.P. Labuan, and W.P. Putrajaya have no separate district-level breakdown in this dataset).
**Description:** Labour force, unemployment rate, and participation rate by administrative district — the finest geographic grain Malaysia's official labour statistics publish. There is no published city-level series; a city such as Petaling Jaya or Kota Kinabalu sits inside a larger administrative district and is not separately surveyed.

### Known limitations
- **6 districts (1 in Sabah, 5 in Sarawak) have no 2024 figure at all** in the source file — a genuine publication gap, not a processing error. These are excluded from Notebook 06's charts (see the notebook for the exact list).
- **DOSM's own Labour Force Survey methodology states it is designed for national and state-level reliability first.** District-level figures, especially for smaller or more remote districts, should be read as directional rather than precise to a decimal point.
