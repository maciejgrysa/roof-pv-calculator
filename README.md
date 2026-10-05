> **Portfolio showcase** — the complete implementation is private. This public repository intentionally contains documentation only. A live demo or controlled private review is available for serious project discussions.

# RoofPVCalculator

RoofPVCalculator is a sanitized public portfolio edition of a web application for designing and evaluating photovoltaic roof configurations.

The repository demonstrates the engineering and product architecture of a real 3D configuration workflow while deliberately excluding customer branding, customer data, production catalogues, real prices, proprietary commercial documents, private infrastructure and production-only integrations.

## What the application demonstrates

- satellite-map based roof workflow
- interactive 3D roof creator
- multiple roof geometries and editable roof faces
- dormers, roof windows and chimneys
- PV roof-tile layout and bill-of-material calculations
- Standard vs Performance product variants
- active/passive roof coverage calculations
- PV power estimation
- automatic inverter and electrical-board selection
- optional energy-storage selection
- pallet and transport calculations
- project export/import to a local .roofpv file
- local CSV export
- local PDF engineering summary
- optional blueprint analysis workflow when an AI API key is supplied

## Public-demo data

All catalogue and price information in this repository is synthetic.

The public edition uses:
- Series A / Series B instead of commercial product lines
- generic Standard / Performance variants
- generic Graphite / Onyx / Terracotta finishes
- demo inverter and battery products
- demo pricing values
- demo logistics data
- procedural 3D materials instead of customer image assets

None of these values should be treated as product specifications or commercial pricing.

## Privacy

The portfolio edition does **not** include:
- customer CRM/lead tracking
- customer e-mail collection
- offer delivery by e-mail
- customer telemetry
- MongoDB project storage
- production customer catalogues
- production customer logos or marketing images
- customer addresses, domains or contact details

Project files are downloaded and loaded locally in the browser.

## Stack

- Python / FastAPI
- JavaScript
- Three.js
- Leaflet
- PDFLib
- OpenPyXL
- optional Google mapping/solar APIs
- optional Anthropic vision workflow

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
uvicorn main:app --host 127.0.0.1 --port 8001 --reload
```

Open:

```text
http://127.0.0.1:8001/
```

The 3D creator and synthetic catalogues can be inspected without production customer data. Features relying on external APIs require your own API keys.

## Security note

Do not commit API keys. Use `.env`, which is ignored by Git.

## Usage and licensing

This repository is source-available for portfolio evaluation. You may inspect the code and run an unmodified local copy for evaluation, but commercial use, redistribution, republishing and derivative distribution are not permitted without written permission. See [LICENSE.md](LICENSE.md).
