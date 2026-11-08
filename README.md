# State business fee dataset

The state filing and recurring fees for an LLC, a corporation and a nonprofit in all 51 jurisdictions (50 states and the District of Columbia), as open data. Each row carries the official source and the date.

Browse it, with the cost of each state worked out, at https://founditbusiness.com/data/

## Files

| File | Rows | What it holds |
|---|---|---|
| `state-business-fees.csv` | one per fee, state and entity | Every state fee the dataset tracks |
| `state-business-fees.json` | same rows | The same rows as JSON, with the license and generated date at the top |
| `llc-cost-summary.csv` | one per state | LLC formation fee, first-year, five-year and per-year totals, foreign registration fee and report cadence |

## Columns in the fee rows

- `state`, `state_code`
- `entity`: `llc`, `corporation`, `nonprofit`, or `any` for a fee that applies to every entity
- `fee`: what the fee is for
- `amount_usd`
- `period_years`: how often a recurring fee is due; blank for a one-time fee
- `minimum`: `true` when the amount is a floor, not a fixed charge
- `note`
- `official_source_url`: the state's own page for the figure
- `date`: the date on the row

## License

CC BY 4.0 (see `LICENSE`). Free to use, including commercially. A link back to https://founditbusiness.com/data/ is required.

## How to cite

FoundIt, "State business fee dataset," https://founditbusiness.com/data/ (CC BY 4.0).

## Updates

The copy on the site is the current one. This repository is refreshed from it.
