# OptiDice — Case Study Reports

Public mirror of the rendered, interactive HTML reports for OptiDice's eight simulation case studies. Served via **GitHub Pages** and linked from [optidice.com](https://www.optidice.com).

**You probably want the landing page:** [`index.html`](./index.html) (or via Pages: <https://douglasfantini.github.io/optidice-reports/>).

## What is this repo?

This repo contains **only** the final rendered HTML reports — each one is a single-file, self-contained interactive dashboard (Chart.js, plain HTML, no build step) built from the Python simulators in the **private** companion repo [`VitorAN/Simulytica`](https://github.com/VitorAN/Simulytica). The source simulators, methodology guides, and the publish pipeline that mirrors files here live there.

This repo exists for one reason: GitHub Pages serves static HTML inline, free, on a CDN — which is what we need so the Portfolio cards on optidice.com can link to an interactive report without the source code being public.

## The case studies

| # | Slug | Domain | Report |
|---|---|---|---|
| 1 | `workforce-analytics`        | Labour Market & Organizational Economics | [Open ↗](./01_corporate_world/corporate_world_mc_report.html) |
| 2 | `smart-manufacturing`        | Manufacturing Operations & Production Planning | [Open ↗](./02_smart_factory/smart_factory_mc_report.html) |
| 3 | `supply-chain-resilience`    | Supply Chain Network & Inventory Management | [Open ↗](./03_supply_chain/supply_chain_mc_report.html) |
| 4 | `emergency-department`       | Healthcare Operations & Patient Flow | [Open ↗](./04_emergency_department/ed_patient_flow_report.html) |
| 5 | `urban-traffic`              | Traffic Engineering & Intersection Control | [Open ↗](./05_urban_traffic/urban_traffic_mc_report.html) |
| 6 | `portfolio-risk-analysis`    | Financial Risk Analysis & Asset Allocation | [Open ↗](./06_portfolio_risk/portfolio_risk_mc_report.html) |
| 7 | `call-center-operations`     | Contact Center Operations & Workforce Management | [Open ↗](./07_call_center/call_center_mc_report.html) |
| 8 | `supermarket-operations`     | Retail Operations & Checkout Resilience | [Open ↗](./08_supermarket_test/supermarket_mc_report.html) |

## How files get here

This repo is **not authored by hand**. The publish pipeline in [`VitorAN/Simulytica`](https://github.com/VitorAN/Simulytica) (specifically `tools/publish_case_study.py`) reads each case-study folder's `case-study.yml`, locates the rendered report HTML, and pushes it to this repo on every publish action. Do not commit changes here by hand — they'll be overwritten on the next publish.

## License

Reports are © OptiDice. Reuse permitted with attribution; for derivative or commercial use, get in touch at <https://www.optidice.com/contact>.

## Transferring ownership

This repo was initially created under the `DouglasFantini` account. If you want it to live under `VitorAN`, request a transfer at GitHub → Settings → Danger Zone → Transfer ownership. The GitHub Pages URL changes accordingly (`vitoran.github.io/optidice-reports/...`); the publish pipeline's `REPORTS_REPO` constant in `tools/publish_case_study.py` would need to be updated to match.
