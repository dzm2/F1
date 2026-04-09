# Sector Scope · F1 Dashboard

A live Formula 1 data dashboard for the 2026 season. Built as a single HTML file, hosted on GitHub Pages.

**[→ View the live dashboard](https://dzm2.github.io/F1/)**

---

![Sector Scope dashboard screenshot](Sector%20Scope.png)

---

## What it is

Sector Scope pulls live data from public F1 APIs and presents it as a clean, fast dashboard — no login, no ads, no install. It covers driver and constructor standings, the full race calendar with detailed results for every completed round, a season analysis tab, F1 news and podcasts, all-time records, and a plain-English explainer of how Formula 1 works.

The entire dashboard is a single `index.html` file — no frameworks, no build step, no dependencies. It runs entirely in the browser and is hosted as a static site on GitHub Pages.

## Data sources

| Source | What it provides |
|---|---|
| [Jolpica F1 API](https://api.jolpi.ca/ergast/f1/) | Standings, results, qualifying, pit stops, fastest laps |
| [OpenF1](https://openf1.org) | Driver headshots, tyre strategy, race control events |
| [Open-Meteo](https://open-meteo.com) | Current weather at the next race circuit |
| [rss2json](https://rss2json.com) | F1 news, podcasts, and video feeds |

All data sources are free and require no API key.

## Tech stack

- Vanilla HTML, CSS, and JavaScript — no frameworks
- [Chart.js](https://www.chartjs.org/) for data visualisation
- [Barlow](https://fonts.google.com/specimen/Barlow) typeface via Google Fonts
- Hosted on GitHub Pages as a static site

## Tabs

| Tab | What's inside |
|---|---|
| Drivers | 2026 standings, stats, charts, and race history per driver |
| Constructors | 2026 standings, reliability, points trends per team |
| Races | Full season calendar with detailed results for every completed round |
| Season | Championship progression, driver momentum, teammate head-to-head, team assessments |
| News | Latest F1 headlines, podcasts, and videos |
| Records | 18 all-time F1 records |
| Explainer | Plain-English guide to how Formula 1 works |

---

## Post-race update workflow

After each race weekend, the dashboard needs a small update. This is done with the help of Claude AI — no manual code editing required.

### Steps

1. Open a new Claude session with this project loaded
2. Tell Claude: **"Round X is done"** (Claude can look up the results, or you can provide them)
3. Claude will update team assessments, constructor win/podium counts, and produce a new `index.html`
4. Download the new `index.html` and push it to this repo
5. Visit the [live site](https://dzm2.github.io/F1/) and hit **↻ Refresh** to clear the cache
6. Replace `index.html` in Claude project settings with the new file
7. Replace the project knowledge file in Claude project settings with the updated version

### At the end of the season

1. If a constructor wins the championship, update `titles` in `TEAM_INFO` in the code
2. Update team assessments one final time
3. Push and refresh as above

---

## Project notes

- Built entirely through conversational prompting with [Claude](https://claude.ai) (Anthropic) — no code was written by hand
- This is a personal project and is not affiliated with Formula 1, the FIA, or any F1 team
- The repo is not set up to accept pull requests or contributions
- F1, FORMULA ONE, FORMULA 1, FIA FORMULA ONE WORLD CHAMPIONSHIP, GRAND PRIX and related marks are trade marks of Formula One Licensing B.V.
