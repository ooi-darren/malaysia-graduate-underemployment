# Sources

Full citations for every figure used in this case study. See `DATA_DICTIONARY.md` for how each was used and its specific limitations.

## National

- DOSM (Department of Statistics Malaysia). *Graduates Statistics 2024.* https://www.dosm.gov.my/uploads/release-content/file_20260401145140.pdf — fetched this session; could not be machine-read (binary/compressed PDF, no rendering tool available). Figures used are DERIVED from secondary reporting of this release.
- DOSM, OpenDOSM Data Catalogue — Annual Principal Labour Force Statistics (`lfs_year`): https://open.dosm.gov.my/data-catalogue/lfs_year — fetched and read directly.
- DOSM, OpenDOSM Data Catalogue — Monthly Youth Unemployment (`lfs_month_youth`): https://open.dosm.gov.my/data-catalogue/lfs_month_youth — fetched and read directly; see DATA_DICTIONARY.md for a column-mapping issue found and corrected this session.
- DOSM, OpenDOSM Data Catalogue — Skills-Related Underemployment by Age (`lfs_qtr_sru_age`) and by Sex (`lfs_qtr_sru_sex`): https://open.dosm.gov.my/data-catalogue/lfs_qtr_sru_age — fetched and read directly.

## Regional (state)

- DOSM, OpenDOSM Data Catalogue — Quarterly Principal Labour Force Statistics by State (`lfs_qtr_state`): https://open.dosm.gov.my/data-catalogue/lfs_qtr_state — fetched and read directly.
- DOSM, OpenDOSM Data Catalogue — Annual Principal Labour Force Statistics by State & Sex (`lfs_state_sex`): https://open.dosm.gov.my/data-catalogue/lfs_state_sex — fetched; not used in the final notebooks (superseded by `lfs_qtr_state` for recency).
- DOSM, OpenDOSM Data Catalogue — State GDP by Sector (`gdp_state_real_supply`) and sector lookup table (`gdp_lookup`): https://open.dosm.gov.my/data-catalogue/gdp_state_real_supply — fetched and read directly.
- DOSM, OpenDOSM Data Catalogue — Lecturers in Public Universities (`lecturers_uni`): https://open.dosm.gov.my/data-catalogue/lecturers_uni — fetched and read directly.

## Local (district)

- DOSM, OpenDOSM Data Catalogue — Annual Principal Labour Force Statistics by District (`lfs_district`): https://open.dosm.gov.my/data-catalogue/lfs_district — fetched and read directly.

## Wages and field-of-study (DERIVED/ESTIMATED — no PUBLIC dataset found)

- DOSM, *Salaries & Wages Survey Report 2024*: https://www.dosm.gov.my/portal-main/release-content/salaries-and-wages-survey-report-2024 — cited via secondary reporting, not read directly this session. Used in Notebook 07.
- The Edge Malaysia / PNB Research Institute, ["Minimum wage growth narrows Malaysia's education-based pay gap"](https://theedgemalaysia.com/node/755858) — analysis based on 26 editions of the MEF Salary Survey (1997–2022). Used in Notebook 07.
- Ministry of Higher Education (MOHE), Graduate Tracer Study, cited via secondary reporting on field-of-study unemployment figures — not accessed directly this session (see [GREaT portal](https://www.mohe.gov.my/en/services/graduate-employability), an interactive institution-level search tool rather than a bulk dataset). Used in Notebook 08.

## Context / Secondary Sources (Qualitative)

These support the "Why Is This Happening?" sections in the notebooks — they explain the mechanism behind the quantitative findings above but are not themselves PUBLIC/DERIVED/ESTIMATED datasets, so they're kept separate here rather than mixed into the tables above.

- Khazanah Research Institute, ["The School-to-Work Transition Survey (SWTS) of Young Malaysians"](https://www.krinstitute.org/publications/the-school-to-work-transition-survey-swts-of-young-malaysian) — used in Notebook 02.
- Human Resources Online, ["Malaysia faces graduate oversupply, skilled job shortage, and a growing 'gaji cukup makan' reality"](https://www.humanresourcesonline.net/malaysia-faces-graduate-oversupply-skilled-job-shortage-and-a-growing-gaji-cukup-makan-reality) — used in Notebook 03.
- The Star, ["Skills mismatch or graduate oversupply?"](https://www.thestar.com.my/news/education/2023/12/17/skills-mismatch-or-graduate-oversupply) (17 December 2023) — used in Notebook 03.
- New Malaysia Herald, ["Sleepless in Unemployment — Klang Valley Saw 7,000 Jobs Lost in a Month"](https://newmalaysiaherald.com/2026/05/30/sleepless-in-unemployment-klang-valley-saw-7000-jobs-lost-in-a-month/) (30 May 2026) — used in Notebook 05.
- BERNAMA, ["Insights Into Sabah's Rural And Interior Poverty"](https://www.bernama.com/en/news.php/bfokus/news.php?id=2364927) — used in Notebook 06.
- BERNAMA, ["Remote Nabawan Villages Still Without Road Access Since Independence, Sabah State Assembly Told"](https://www.bernama.com/en/region/news.php?id=2583976) — used in Notebook 06.
- Malay Mail, ["HR Minister: 42pc of graduates take skills mismatch jobs on MyFutureJobs"](https://www.malaymail.com/amp/news/malaysia/2023/07/31/hr-minister-42pc-of-graduates-take-skills-mismatch-jobs-on-myfuturejobs/82829) (31 July 2023) — used in Notebook 07.
