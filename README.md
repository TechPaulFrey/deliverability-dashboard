# Deliverability Dashboard

A self-contained, single-file HTML dashboard for tracking email inbox placement
across a multi-account, multi-lane warm-up program (built for the AI Work
sender-reputation pipeline).

## Features

- **Filters** — account, sender/channel, and rolling time window (7 / 30 / 90 days)
- **Key metrics** — total emails checked, spam rate, deliverability rate, primary
  placement rate, unique accounts seen, silent accounts (vs. an editable expected
  count), days tracked, avg emails/account
- **Inbox — channel breakdown** — stacked bar of Primary/Updates/Promotions/Social/
  Forums/Spam per sending lane, plus a category doughnut with percentage labels
- **Trends** — daily inbox vs. spam volume, and a spam-rate trend line
- **Spam rate by account** — sorted bar chart, worst offenders first
- **Account Health** and **Channel Detail** tables — sortable
- **Dark / light mode** toggle
- **Refresh** button to reset filters and re-render

## Usage

Open `index.html` directly in any browser — no server or build step required.
All data is embedded in the file at build time (see below), and Chart.js /
chartjs-plugin-datalabels load from a CDN.

## Updating the data

The dashboard's dataset is baked into `index.html` as a `SOURCE` JS object at
build time from an `Inbox_Placement_Tracker.xlsx` export (columns:
`recipient_email`, `subject`, `from`, `category`, `checked_at`). To refresh
with a new export, regenerate `index.html` from that source file and replace
it here.

## Hosting on GitHub Pages (optional)

1. Push this repo to GitHub (see below).
2. In the repo's **Settings → Pages**, set the source to the `main` branch,
   root folder.
3. The dashboard will be live at `https://<your-username>.github.io/<repo-name>/`.

## Pushing this repo to GitHub

```bash
# from inside this folder
git init
git add .
git commit -m "Initial commit: deliverability dashboard"
git branch -M main

# create an empty repo on GitHub first (e.g. via github.com/new), then:
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
