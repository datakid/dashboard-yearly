# Dashboard Arena

Yearly pharmacy dashboard. Superseded by Alembic (dashboard2).

## What it does

- Reads the data from a Google Sheet as CSV and parses it with PapaParse.
- Single view: filters by region, pharmacy, month and class, over a set of years that you select (All, None, Apply Selection).
- Compare view: two sets of filters, A and B, each with its own year.
- Totals value, prescriptions and insurance-covered prescriptions, plus 18 category columns.
- Orders months from July and sorts years newest first by default.
- Exports the current numbers as CSV, or copies them to the clipboard.
- Syncs on demand. Auto-sync repeats every 5 minutes, and the choice is kept in `localStorage` under `da-auto-sync`.

## What it does not do

- It has no file upload. It reads one fixed Google Sheet.
- It is read-only and keeps no copy of the data. When the sheet cannot be reached the page shows "Error loading data".
- It is no longer developed. Alembic combines it with Lx Dashboard.

## Network and install

Calls Google Sheets for its data, and loads PapaParse and Font Awesome from cdnjs and Google Fonts. It makes no other requests. Not installable; no service worker.

## Built with

One HTML file, with no build step and no framework. PapaParse parses the CSV and Font Awesome supplies the icons.

## Run locally

Serve the folder with any static file server. The page needs a connection to reach the sheet.
