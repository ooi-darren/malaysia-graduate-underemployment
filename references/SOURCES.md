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

## Context / Secondary Sources (Qualitative)

These support the "Why Is This Happening?" sections in the notebooks — they explain the mechanism behind the quantitative findings above but are not themselves PUBLIC/DERIVED/ESTIMATED datasets, so they're kept separate here rather than mixed into the tables above.

- Khazanah Research Institute, ["The School-to-Work Transition Survey (SWTS) of Young Malaysians"](https://www.krinstitute.org/publications/the-school-to-work-transition-survey-swts-of-young-malaysian) — used in Notebook 02.
- Human Resources Online, ["Malaysia faces graduate oversupply, skilled job shortage, and a growing 'gaji cukup makan' reality"](https://www.humanresourcesonline.net/malaysia-faces-graduate-oversupply-skilled-job-shortage-and-a-growing-gaji-cukup-makan-reality) — used in Notebook 03.
- The Star, ["Skills mismatch or graduate oversupply?"](https://www.thestar.com.my/news/education/2023/12/17/skills-mismatch-or-graduate-oversupply) (17 December 2023) — used in Notebook 03.
- New Malaysia Herald, ["Sleepless in Unemployment — Klang Valley Saw 7,000 Jobs Lost in a Month"](https://newmalaysiaherald.com/2026/05/30/sleepless-in-unemployment-klang-valley-saw-7000-jobs-lost-in-a-month/) (30 May 2026) — used in Notebook 05.
- BERNAMA, ["Insights Into Sabah's Rural And Interior Poverty"](https://www.bernama.com/en/news.php/bfokus/news.php?id=2364927) — used in Notebook 06.
- BERNAMA, ["Remote Nabawan Villages Still Without Road Access Since Independence, Sabah State Assembly Told"](https://www.bernama.com/en/region/news.php?id=2583976) — used in Notebook 06.
