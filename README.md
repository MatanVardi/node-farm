# 🥑 Node Farm

A small Node.js web app for a fictional farm shop, built while learning Node.js core modules — no frameworks, just `http`, `fs`, and `url`.

## Features

- **Overview page** (`/` or `/overview`) — lists all products as cards
- **Product page** (`/product?id=<n>`) — detailed view of a single product
- **JSON API** (`/api`) — returns the raw product data
- **404 handling** for unknown routes
- Simple HTML templating with `{%PLACEHOLDER%}` replacement (see `mymodules/replaceTemplate.js`)
- URL slugs generated with [`slugify`](https://www.npmjs.com/package/slugify)

## Project structure

```
.
├── index.js                  # HTTP server and routing
├── mymodules/
│   └── replaceTemplate.js    # Fills HTML templates with product data
├── templates/                # HTML templates (overview, card, product)
├── dev-data/
│   └── data.json             # Product data
└── txt/                      # Sample files for fs sync/async exercises
```

## Getting started

**Prerequisites:** [Node.js](https://nodejs.org/) installed.

```bash
npm install
node index.js
```

Or, for auto-reload during development:

```bash
npx nodemon index.js
```

Then open <http://127.0.0.1:8000> in your browser.

## Routes

| Route              | Description                  |
| ------------------ | ---------------------------- |
| `/`, `/overview`   | Product overview page        |
| `/product?id=0`    | Single product page          |
| `/api`             | Product data as JSON         |
| anything else      | 404 page                     |

## Author

Matan Vardi
