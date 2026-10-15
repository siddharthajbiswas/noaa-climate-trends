# NOAA Climate Trends: Santa Clara County

Decades of daily weather records from fifteen Santa Clara County stations,
charted to answer one question: is the county actually getting hotter, or does
it just feel that way every August?

**View it:** https://biswas.net/sid/noaa/

## The answer

Yes, inland. The two stations with records back to 1893 both got hotter:
San Jose went from about 10 days a year at or above 90°F in its first decade to
about 20 in its last, and Los Gatos from 18 to 26. Moffett Field, on the bay
shore, gained roughly 10 days a year above 70°F per decade from 1946 to 2017.
But Palo Alto and Santa Clara University, both close to the bay, show no rise
in either measure, so how much warmer it feels depends on where in the county
you live.

| Station | Years | 90°F+ days/yr, first decade → last decade |
|---|---|---|
| San Jose | 1893–2006 | 10 → 20 |
| Los Gatos | 1893–2010 | 18 → 26 |
| Gilroy | 1958–2021 | 48 → 51 |
| Moffett Field | 1946–2017 | 4 → 7 |
| Mount Hamilton | 1952–2024 | 4 → 7 |
| Palo Alto | 1954–2012 | 9 → 9 |
| Santa Clara University | 1904–1975 | 18 → 17 |

Counts are annual totals from GHCN-D, so a year with missing days counts low;
the trend lines on each station page use every year on record.

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
