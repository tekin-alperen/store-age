# Store Age

A free, open-source workspace for resellers. Track inventory, record expenses and business mileage, and estimate profit in a clean paper-and-cobalt interface. No account, build step, API key, or dependencies required.

## Run locally

Download this repository, or clone it:

```sh
git clone https://github.com/tekin-alperen/store-age.git
cd store-age
python3 -m http.server 4173 --directory dist
```

Open **http://localhost:4173**. Any static web server works. Keep the same origin and port to access the same browser-local records.

## Features

- Inventory creation and editing with an optional photo, category, source, storage location, price, fees and status
- Search, status filters and sorting
- Expense and mileage entries
- Profit and bulk-purchase calculators
- Goals and a simple, rule-based inventory coach
- CSV inventory import/export, including quoted fields
- Printable title and SKU labels
- Mobile navigation and responsive layouts
- Local browser storage

## Demo and data

This is an early prototype. The dashboard and charts include illustrative reference figures, and the report period controls are presentation-only. Recorded sales and expenses are included in the report summary, but it is not a complete accounting system. The mileage estimate uses an illustrative fixed rate of $0.70 per mile, not a verified tax rate.

Inventory, expenses, trips, photos and goals are stored in your browser's `localStorage`; they are not sent to a server. Clearing browser storage removes them. CSV export backs up inventory only, not expenses, trips or goals. There is no cloud sync, authentication, multi-user support, automatic receipt/barcode recognition, or connected marketplace integration. Price lookup opens eBay's public sold-listings search in a new tab.

## Project structure

```text
dist/
  index.html   Page shell and metadata
  style.css    Paper & Cobalt theme and responsive layout
  app.js       Views, interactions and browser-local data
LICENSE        MIT license
```

Deploy `dist/` to any static hosting service. Hash-based navigation works without rewrite rules. All runtime assets are included, with no external font or script requests.

## Contributing

Issues and pull requests are welcome. Keep the app dependency-free where practical, preserve accessible controls, and document any changes to storage or sample data. Before submitting, run:

```sh
node --check dist/app.js
```

Check the changed screen at desktop and mobile widths and verify that records persist after refreshing.

## License

[MIT](LICENSE). You may use, modify and redistribute the code, including commercially, under the license terms.

Store Age is an independent project inspired by reseller inventory workflows. It is not affiliated with or endorsed by Flippd. No Flippd logos, assets or source code are included.
