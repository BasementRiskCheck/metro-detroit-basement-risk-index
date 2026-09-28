# Data dictionary, Metro Detroit Basement Risk Index

File: `metro-detroit-basement-risk-index.csv`
Rows: 116 communities across Wayne, Oakland, and Macomb counties, Michigan.
One row per community, sorted by Basement Risk Index from highest risk to lowest.

| Column | Type | Description |
|---|---|---|
| `rank` | integer | Rank by Basement Risk Index, 1 = highest modeled basement-flood risk among the 116 communities. |
| `community` | text | Community name (city, village, or township). |
| `bri_score` | integer 0 to 100 | Basement Risk Index. A relative score of structural basement-flood exposure, rescaled 0 to 100 across metro Detroit (metro median is about 37). Higher means greater modeled risk. |
| `pct_homes_pre_1960` | integer (percent) | Share of housing units built before 1960, from U.S. Census ACS. Older housing stock is the single largest driver of basement-water risk in this region. |
| `median_home_value_usd` | integer (USD) | Median owner-occupied home value, U.S. Census ACS. Included to show that risk tracks housing age, not wealth. |
| `scoring_basis` | text | How the score was produced. Suburbs are modeled from U.S. Census housing data. Detroit additionally blends in City of Detroit 311 water-in-basement records. |
| `profile_url` | URL | Link to the full public community report on basementriskcheck.com. |
| `confidence` | text (A or C) | Data-confidence grade. A = local flood-incident records integrated (Detroit, from 311 today). C = modeled from housing-age measures, no local flood records integrated yet (all suburbs today). |

## How the Basement Risk Index is built

The index is an honest hybrid. The two largest inputs are U.S. Census measures of housing age: the share of homes built before 1960 (about 60 percent of the weight) and the median year built (about 40 percent). Detroit's score also reflects its real flood record from the City of Detroit's Improve Detroit / 311 system (the live record passed 13,900 water-in-basement reports by September 2026). Scores are rescaled 0 to 100 across the metro.

Suburban scores are modeled from housing data and are labeled as modeled. They are not claims of observed flooding. Detroit's score is the one that blends modeled housing data with observed 311 flood records.

## Sources

- U.S. Census American Community Survey (ACS), 2020-2024 5-year estimates: housing age, median year built, home value, tenure. Cities are measured as whole census places (a city can span two counties), townships as county subdivisions.
- City of Detroit, Improve Detroit / 311 service requests: water-in-basement records, 2023 to present (a live, growing dataset).
- U.S. Census TIGER/Line: community and tract boundaries.

## Scope and limitations

- Coverage is the metro Detroit beachhead: Wayne, Oakland, and Macomb counties (116 communities, and about 1,100 census-tract neighborhoods in the underlying model).
- The index measures structural exposure (housing age and, for Detroit, observed flood reports), not a prediction of any individual property flooding.
- Suburban scores are modeled, not observed. Do not read a suburb's score as a count of real floods.
- The 311 figure is a dated snapshot of a live dataset. Cite it with its date.

## Attribution

Please credit "Basement Risk Check, a southeast Michigan homeowner resource" and link to https://basementriskcheck.com/report. Suggested license: Creative Commons Attribution 4.0 (CC BY 4.0).


# Data dictionary, ACS 2020-2024 refresh (what moved)

File: `metro-detroit-bri-2026-refresh.csv`
Rows: 116 communities. Old vs new after the July 2026 rescore from ACS 2018-2022 onto ACS 2020-2024 (model unchanged).

| Column | Type | Description |
|---|---|---|
| `community` / `slug` | text | Community name and its URL slug on basementriskcheck.com. |
| `old_score` / `new_score` / `delta` | integer | Basement Risk Index before and after the rescore, and the change in points. |
| `old_rank` / `new_rank` | integer | Rank among the 116 before and after. |
| `old_band` / `new_band` | text | Risk band (Very High / High / Elevated / Moderate / Lower) before and after. |
| `old_pre1960_pct` / `new_pre1960_pct` | integer (percent) | Share of homes built before 1960 on each vintage. |
| `old_myb` / `new_myb` | integer (year) | Median year built on each vintage. |
| `note` | text | Correction flags. Northville's published score had been built from only its Wayne County part (a two-county aggregation error, corrected here); Grosse Pointe Shores and Memphis carry smaller corrections of the same kind. Detroit's note records its unchanged 311 blend. |
