# Data dictionary, Detroit basement-flood equity by ZIP

File: `detroit-flood-equity-by-zip.csv`
Rows: 28 City of Detroit ZIP codes with a sufficient sample of reports.
One row per ZIP. Pairs the documented water-in-basement rate with neighborhood income and demographics.

| Column | Type | Description |
|---|---|---|
| `zip` | text | 5-digit ZIP code within the City of Detroit. |
| `wib_rate_per_1000_homes` | decimal | Documented water-in-basement 311 reports per 1,000 housing units in the ZIP. Normalizing by housing units lets ZIPs of different sizes be compared fairly. |
| `median_household_income_usd` | integer (USD) | Median household income for the ZIP, U.S. Census ACS. |
| `pct_black` | integer (percent) | Share of residents who are Black or African American, U.S. Census ACS. |

## What this dataset shows

It places the City of Detroit's documented basement-flooding record next to neighborhood income and demographics, so the distribution of flood burden can be examined directly. The full writeup, including how to read it responsibly, is at https://basementriskcheck.com/detroit-flood-equity.

## Sources

- City of Detroit, Improve Detroit / 311 service requests: water-in-basement records. The full record is more than 13,400 reports (precise count 13,433 as of June 2026). This file reports a normalized rate per 1,000 homes, not raw counts.
- U.S. Census American Community Survey (ACS): median household income and race by ZIP.

## Scope and limitations

- Detroit only, and only ZIPs with a sufficient sample. Several low-count ZIPs are excluded to avoid unstable rates.
- 311 reports reflect what residents reported, not every flood event, so this is a measured floor on flooding, not a complete census of it.
- These are neighborhood-level (ZIP) associations. They describe how flood burden, income, and demographics line up across Detroit, and are not statements about any individual household.
- The 311 record is live and grows. Cite the figure with its date.

## Attribution

Please credit "Basement Risk Check, a southeast Michigan homeowner resource" and link to https://basementriskcheck.com/detroit-flood-equity. Suggested license: Creative Commons Attribution 4.0 (CC BY 4.0).
