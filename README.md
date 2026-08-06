# NOAA Climate Trends: Santa Clara County

Decades of daily weather records from fifteen Santa Clara County stations,
charted to answer one question: is the county actually getting hotter, or does
it just feel that way every August?

**View it:** https://biswas.net/sid/noaa/

## What's here

| Path | Contents |
|---|---|
| `index.html` | County overview and station picker |
| `station.html` | Per-station detail view |
| `script.js` | Loads the station records and drives the overview |
| `station_chart.js` | The charts, drawn directly on a `<canvas>` |
| `GHCND_*.json` | One file per station, from NOAA's Global Historical Climatology Network Daily |
| `data_summary.json` | Precomputed per-station summary statistics |
| `maps/` | Station location maps |

The charts are hand-drawn on canvas rather than pulled from a charting library,
so the axis, scaling and hover logic all live in `station_chart.js`.

## The data

NOAA GHCN-Daily, station records `USC00043417` through `USW00023293`, covering
Palo Alto, San Jose, Gilroy, Mount Hamilton and others. Coverage varies by
station: some run back to the 1890s, others only start in the 1990s, which is
worth keeping in mind when comparing them.
