# MtgoDecklistScraperDecks

Scraped MTGO decklist data, updated every 4 hours.

A GitHub Actions workflow downloads the latest [MtgoDecklistScraperNet](https://github.com/danzel/MtgoDecklistScraper) release, runs it, commits new event JSON files, and publishes them to GitHub Pages.

## Layout

- `output/months.json` — list of `"YYYY/MM"` strings for all months with data
- `output/YYYY/MM/events.json` — list of event filenames for that month
- `output/YYYY/MM/{event-slug}.json` — full deck data for one event

## Setup

1. Push this repo to GitHub
2. Repo Settings → Pages → Build and deployment → Source: **GitHub Actions**
3. Repo Settings → Actions → General → Workflow permissions: **Read and write permissions**
4. The workflow runs every 4 hours, or trigger manually from the Actions tab
