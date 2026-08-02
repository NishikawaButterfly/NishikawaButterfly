# Hi

I'm an electrical engineer. Most of my day job is around data centers and energy projects, and I write software to take the tedious parts out of that work. Most of what's here is finished; one project is still in progress. Everything public uses made-up sample data.

## [Data center electrical simulator](https://github.com/NishikawaButterfly/dc-twin)

A deterministic capacity simulator for data-center electrical architectures. You describe a topology (utility feeds, generators, UPS, transfer switches, PDUs, loads) and a scenario of failures and maintenance windows, and it returns a timeline of which loads stayed served, when each UPS ran down, and what caused every alarm. The same inputs always produce the same result hash, so any run can be replayed and verified. The reference scenario's numbers are checked against a hand calculation, and all of the data is synthetic.

Python, FastAPI for the read-only API, a plain JavaScript web explorer, PostgreSQL for stored runs. Ships with Docker Compose, and there is a live explorer at https://dc-twin.fly.dev/ with the reference scenarios.

## [Electrical Asset Validator](https://github.com/NishikawaButterfly/electrical-asset-validator)

A web app for checking electrical asset registers before they get handed between teams. You upload a CSV or XLSX file, it validates a nine-column format and flags duplicate tags, missing panel or circuit references, and out-of-range voltage and power values. It can also diff two revisions of the same register by asset tag, so you can see exactly which assets were added, removed or changed. Results export to PDF or XLSX.

FastAPI backend, React + TypeScript frontend, PostgreSQL. Starts with one `docker compose up`. Sample registers with deliberate errors are included so you can try it without your own data, or you can use the live demo at https://electrical-asset-validator.fly.dev/.

## [Sudoku PWA](https://github.com/NishikawaButterfly/sudoku-pwa)

A sudoku game as an installable progressive web app. The first version was a single HTML file, but some messaging apps opened it in a restricted preview where the JavaScript couldn't run, so I rebuilt it as a proper PWA.

Six difficulty levels, 24 puzzles (each checked to have exactly one solution), notes, hints, undo. Works offline and saves progress locally. No accounts, no tracking. Plain JavaScript, no framework. Tested with Playwright.

## [PV-BESS dispatch model](https://github.com/NishikawaButterfly/pv-bess-hybrid)

A Python model for solar plants with battery storage. It reads hourly PV production and market prices, computes a dispatch schedule for the battery (a mixed-integer program solved with HiGHS), and works out NPV, IRR, payback and LCOS for the scenario. I rebuilt it from an older prototype after finding calculation errors in the original, so it is deliberately small and heavily tested. It now has an API and a small web page that renders the result as charts; there is a live explorer at https://pv-bess-hybrid.fly.dev/ and solver benchmarks in the docs.

## [Critical Facilities Manager](https://github.com/NishikawaButterfly/critical-facilities-manager)

An operations and commissioning platform for critical facilities, developed
and tested privately and now public. Locations, assets, and maintenance
orders with validated state machines; MOP/SOP/EOP procedures with four-eyes
approval; work permits that block completing an order while one is open;
mutual-exclusion constraints that stop simultaneous maintenance on redundant
equipment; commissioning tests with witnessed evidence; and an append-only
audit trail behind every write. Bearer-token auth with roles. FastAPI,
SQLAlchemy, 237 tests, all sample data synthetic.

## In progress: [Energy Investment Lab](https://github.com/NishikawaButterfly/energy-investment-lab)

A cash-flow and financing model for energy assets, in plain Python with no
runtime dependencies. It handles escalated revenues and costs, annuity debt
with DSCR, corporate tax with depreciation and loss carryforward, MIRR,
levelized cost, one-at-a-time sensitivities, and a seeded Monte Carlo whose
results are reproducible to the byte. One scenario file in, a results file
and a committee-style report out. Every worked example in the docs is
hand-calculated and pinned by tests.

## Tools

Python (pandas, FastAPI), TypeScript and React for frontends, plain JavaScript when a framework would be overkill, PostgreSQL, Docker, GitHub Actions for CI.

## Contact

nishikawa.butterfly@gmail.com
