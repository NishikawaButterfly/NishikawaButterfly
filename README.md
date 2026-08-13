# Ricardo — Electrical Engineer & Engineering Software Developer

I build tested software for data-center electrical systems, critical
facilities, energy storage and quantitative analysis.

[Portfolio](https://nishikawabutterfly.github.io/) · [All projects](https://github.com/NishikawaButterfly?tab=repositories) · [Contact](mailto:nishikawa.butterfly@gmail.com)

## Selected work

### [dc-twin](https://github.com/NishikawaButterfly/dc-twin)

A deterministic capacity simulator for data-center electrical
architectures. You describe a topology — utility feeds, generators, UPS,
transfer switches, PDUs, loads — and a scenario of failures and
maintenance windows, and it returns which loads stayed served, when each
UPS ran down, and what caused every alarm. The same inputs always
produce the same result hash, the reference scenarios are checked
against hand calculations, and there is a live explorer at
https://dc-twin.fly.dev/.

### [Critical Facilities Manager](https://github.com/NishikawaButterfly/critical-facilities-manager)

An operations and commissioning platform for critical facilities.
Locations, assets, and maintenance orders move through validated state
machines; procedures carry four-eyes approval; work permits and
mutual-exclusion constraints block unsafe combinations, like simultaneous
maintenance on redundant equipment. Write authority is scoped per site,
evidence files are stored under their content hash and re-verified on
every download, and the audit trail is append-only in the database
itself — triggers refuse to update or delete it, not just the
application. It runs on PostgreSQL or SQLite, the schema is under
migrations, and a small web interface ships with it: the asset tree, the
order board, and the audit timeline.

### [Electrical Asset Validator](https://github.com/NishikawaButterfly/electrical-asset-validator)

A web app for checking electrical asset registers before they get handed
between teams. You upload a CSV or XLSX file — mapping nonstandard
columns if needed — and it flags duplicate tags, missing panel or
circuit references, and out-of-range voltage and power values. It can
also diff two revisions of the same register by asset tag, and results
export to PDF or XLSX reports. Uploads stay private to the browser
session that made them, and the public demo deletes them after thirty
minutes. There is a live demo at
https://electrical-asset-validator.fly.dev/.

### [PV-BESS Dispatch Model](https://github.com/NishikawaButterfly/pv-bess-hybrid)

A Python model for solar plants with battery storage. It reads hourly PV
production and market prices, computes the battery's dispatch schedule
as a mixed-integer program solved with HiGHS, and works out NPV, IRR,
payback and LCOS for the scenario. I rebuilt it from an older prototype
after finding calculation errors in the original, so it is deliberately
small and heavily tested, with solver benchmarks in the docs and a live
explorer at https://pv-bess-hybrid.fly.dev/.

## Other projects

[Energy Investment Lab](https://github.com/NishikawaButterfly/energy-investment-lab) · [Quant Risk Engine](https://github.com/NishikawaButterfly/quant-risk-engine) · [Sudoku Instant](https://github.com/NishikawaButterfly/sudoku-pwa) — a cash-flow and financing model for energy assets, a portfolio-analytics and risk engine, and a finished offline-capable sudoku PWA.

Everything public here has a tagged release, and all sample data is fictional.
