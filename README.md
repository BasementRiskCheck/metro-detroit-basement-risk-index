# Metro Detroit Basement Risk Index

A free, public dataset scoring all 116 communities in metro Detroit (Wayne, Oakland, and Macomb counties) on basement-flood risk, built from U.S. Census housing data and City of Detroit flood records by Basement Risk Check, a southeast Michigan homeowner resource.

Full report and methodology: https://basementriskcheck.com/report
Methodology in detail: https://basementriskcheck.com/methodology

## What is in here

- `metro-detroit-basement-risk-index.csv`, 116 communities, ranked, with the Basement Risk Index score, the share of homes built before 1960, median home value, the scoring basis, and a link to each community's full report.
- `detroit-flood-equity-by-zip.csv`, a companion dataset for the City of Detroit: documented water-in-basement rate per 1,000 homes alongside median household income and demographics, by ZIP (28 ZIPs with a sufficient sample). Full writeup at https://basementriskcheck.com/detroit-flood-equity.
- `DATA-DICTIONARY.md` and `detroit-flood-equity-DATA-DICTIONARY.md`, every column defined, plus method, sources, and limitations for each dataset.
- `LICENSE.txt` (CC BY 4.0) and `PUBLISHING.md` (how to upload).

## The headline finding

In metro Detroit, the communities most at risk for basement flooding are the oldest, not the wealthiest. Grosse Pointe and Novi have nearly identical median home values, but Basement Risk Index scores of 96 and 3, because what drives basement water here is housing age and aging sewer infrastructure, not income. Detroit's older neighborhoods carry real, documented risk: more than 13,400 water-in-basement reports in the City of Detroit's 311 record, and the June 2021 storms brought a federal disaster declaration.

## Method, in brief

The index is an honest hybrid. The two largest inputs are U.S. Census measures of housing age (share of homes built before 1960, and median year built). Detroit's score additionally blends in its real 311 water-in-basement records. Suburban scores are modeled from housing data and are labeled as modeled, they are not claims of observed flooding. Scores are rescaled 0 to 100 across the metro (median about 36).

## Sources

- U.S. Census American Community Survey (ACS) 2022 5-year estimates.
- City of Detroit Improve Detroit / 311 water-in-basement service requests (2023 to present).
- U.S. Census TIGER/Line boundaries.

## License and attribution

Suggested license: Creative Commons Attribution 4.0 (CC BY 4.0). If you use or cite this data, please credit "Basement Risk Check" and link to https://basementriskcheck.com/report.
