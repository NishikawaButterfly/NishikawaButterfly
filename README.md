# Hi

I'm an electrical engineer. Most of my day job is around data centers and energy projects, and I write software to take the tedious parts out of that work. A couple of things here are finished, one is still in progress. Everything public uses made-up sample data.

## [Electrical Asset Validator](https://github.com/NishikawaButterfly/electrical-asset-validator)

A web app for checking electrical asset registers before they get handed between teams. You upload a CSV or XLSX file, it validates a nine-column format and flags duplicate tags, missing panel or circuit references, and out-of-range voltage and power values. It can also diff two revisions of the same register by asset tag, so you can see exactly which assets were added, removed or changed. Results export to PDF or XLSX.

FastAPI backend, React + TypeScript frontend, PostgreSQL. Starts with one `docker compose up`. Sample registers with deliberate errors are included so you can try it without your own data.

## [Sudoku PWA](https://github.com/NishikawaButterfly/sudoku-pwa)

A sudoku game as an installable progressive web app. The first version was a single HTML file, but some messaging apps opened it in a restricted preview where the JavaScript couldn't run, so I rebuilt it as a proper PWA.

Six difficulty levels, 24 puzzles (each checked to have exactly one solution), notes, hints, undo. Works offline and saves progress locally. No accounts, no tracking. Plain JavaScript, no framework. Tested with Playwright.

## In progress: [PV-BESS dispatch model](https://github.com/NishikawaButterfly/pv-bess-hibridacion)

A Python model for solar plants with battery storage. It reads hourly PV production and market prices, computes a dispatch schedule for the battery (a small mixed-integer program solved with HiGHS), and works out NPV, IRR and payback for the scenario. I rebuilt it from an older prototype after finding calculation errors in the original, so the current version is deliberately small and has a proper test suite. Early alpha, command-line only, one scenario at a time.

## Tools

Python (pandas, FastAPI), TypeScript and React for frontends, plain JavaScript when a framework would be overkill, PostgreSQL, Docker, GitHub Actions for CI.

## Contact

nishikawa.butterfly@gmail.com
