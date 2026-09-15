# data/

## `agi-forecasts.csv`

One row per publicly stated AGI timeline prediction.

| Column | Meaning |
|---|---|
| `source_name` | Person or group making the prediction |
| `affiliation` | Organization they're associated with |
| `source_type` | Lab CEO, independent forecaster, researcher survey, etc. — use this to weigh commercial incentive against independence |
| `stated_prediction` | The prediction in their own terms |
| `prediction_date` | When the prediction was made or last confirmed (YYYY-MM, or a range for surveys) |
| `notes` | Context needed to interpret the number correctly |

**On self-reported figures:** predictions from lab CEOs (Altman, Amodei, Hassabis, Musk, Suleyman) are stated by parties with a direct commercial and fundraising interest in the outcome. Independent forecasts (Metaculus, AI Impacts) carry no such incentive but are also less certain of unreleased lab capabilities. Neither category is "more correct" by default — read both alongside `source_type`.

**Sources:** compiled from public statements, interviews, and formal policy submissions cited in the [main README](../README.md#sources--deeper-reading). Each row traces to a specific public statement; see the linked source articles for direct citations and dates.

**Freshness:** this file is a snapshot as of September 2026. Lab timelines shift often — see [Contributing / corrections](../README.md#contributing--corrections) in the main README for how to flag an outdated row.
