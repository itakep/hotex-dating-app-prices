# Dating App Prices & Ratings — public dataset (Hotex.org)

A dated, public snapshot of **monthly premium prices (USD), public app-store star ratings and review counts** for 10 major dating platforms. Compiled from public App Store / Google Play listings and vendor pricing pages. Fields that could not be verified are `null` — never estimated.

- **Canonical source / human-readable report:** https://hotex.org/research/dating-app-prices/
- **Machine-readable:** https://hotex.org/dataset/app-prices.json · https://hotex.org/dataset/app-prices.csv
- **Methodology:** https://hotex.org/methodology/
- **Snapshot:** 2026-10 · **License:** CC BY 4.0 (free to cite with attribution to Hotex.org and the snapshot date)

## Why this dataset exists

Most "dating app cost" articles quote a single number with no date and no source. This snapshot is dated, source-stated, and conservative: where pricing trackers disagreed we kept the lower figure; where no month-to-month price could be confirmed (Badoo, Match, happn, eHarmony, Parship) the field stays `null` instead of carrying a guess. The same numbers power every comparison table on Hotex.org, so the machine-readable copy cannot drift from the visible one.

## Headline figures (snapshot 2026-10)

| Metric | Value |
| --- | --- |
| Platforms tracked | 10 |
| Platforms with a verified monthly premium price | 5 |
| Cheapest verified premium tier | Plenty of Fish — $9.99/month |
| Most expensive verified premium tier | Bumble Premium — $39.99/month |
| Average of the 5 verified prices | $26.99/month |
| Highest public store rating | Tinder — 4.4★ (9.14M reviews) |
| Free-to-use (freemium) platforms | 9 of 10 |

## Fields

| Field | Meaning |
| --- | --- |
| `slug` | Stable platform identifier |
| `name` | Display name |
| `model` | `freemium` (free tier + optional premium) or `paid` |
| `best_for` | Editorial niche tag (casual / serious / chat / seniors / international) |
| `launch_year` | Year the platform launched |
| `rating` | Public store star rating, one decimal (Google Play US; happn from US App Store). `null` if unavailable |
| `reviews_m` | Approximate public review count, millions, same storefront. `null` if unavailable |
| `price_usd_month` | Listed monthly USD price of the premium tier. `null` when no figure could be verified |

## Files

- `app-prices.json` — full snapshot with metadata, field semantics and per-app rows.
- `app-prices.csv` — the same rows as CSV (`slug,name,model,best_for,launch_year,rating,reviews_m,price_usd_month`).

## Citation

> Hotex Editorial Team (2026). *Dating App Prices 2026* (snapshot 2026-10). Hotex.org. https://hotex.org/research/dating-app-prices/

## Update cadence

The snapshot is re-verified against independent pricing trackers and rebuilt daily from the same source that powers the site. The `snapshot` and `built` fields travel with every file so any citation is dated.

## Independence

Hotex is an editorial guide; it does not host profiles or chat. Outbound links to platforms on the site are affiliate links and are disclosed on-page. No platform reviewed this dataset before publication.