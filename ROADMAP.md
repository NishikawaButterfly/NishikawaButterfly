# Engineering Software Portfolio Roadmap

Last reviewed: 2026-08-01

## Purpose

This roadmap coordinates a portfolio of engineering software products covering electrical asset data, renewable-energy optimization, critical-infrastructure simulation, investment analysis, and facilities operations. Every public artifact uses US English and only fictional or explicitly redistributable data.

## Current portfolio

| Product | Status | Current outcome | Next gate |
| --- | --- | --- | --- |
| [Sudoku PWA](https://github.com/NishikawaButterfly/sudoku-pwa) | Released | Installable, offline-capable PWA with tested state handling and accessible keyboard workflows | Maintain through versioned fixes |
| [Electrical Asset Validator](https://github.com/NishikawaButterfly/electrical-asset-validator) | Released MVP | CSV/XLSX validation, revision comparison, persisted history, reports, Docker Compose, and CI | Collect evidence before expanding scope |
| [PV-BESS Hybrid Optimization](https://github.com/NishikawaButterfly/pv-bess-hibridacion) | Active modernization | Existing analytical prototype | Deliver an auditable hourly dispatch and investment-analysis release |
| Data Center Electrical Digital Twin | Planned | Product definition | Build the flagship deterministic simulation MVP |
| Energy Asset Investment Lab | Planned | Product definition | Extract reusable, independently tested financial-analysis workflows |
| Critical Facilities Operations Platform | Planned | Product definition | Build traceable operational workflows after shared domain patterns stabilize |
| Quantitative Portfolio & Risk Engine | Planned | Product definition | Build a reproducible market-risk and portfolio-research engine |
| Professional Portfolio Website | Planned | Product definition | Consolidate verified releases into evidence-led case studies |

## Phase 1 — PV-BESS Hybrid Optimization

### Product outcome

An auditable application that evaluates photovoltaic generation and battery dispatch under explicit technical, operational, and commercial assumptions.

### Minimum professional release

- hourly time-series ingestion with schema, timezone, unit, and gap validation;
- PV production, curtailment, grid import/export, and battery state-of-charge accounting;
- power, energy, efficiency, reserve, cycle, and operating-window constraints;
- transparent dispatch objectives and solver-status reporting;
- degradation-aware usable capacity and throughput metrics;
- CAPEX, OPEX, revenue, NPV, IRR, payback, LCOE, and LCOS calculations;
- deterministic scenarios plus sensitivity and stress testing;
- fictional, reproducible sample datasets with provenance metadata;
- API, responsive review interface, downloadable results, and documented assumptions;
- unit, property, integration, and end-to-end tests; locked dependencies; Docker and CI.

### Exit gate

Energy balance closes within a documented numerical tolerance, financial metrics reconcile against independent fixtures, infeasible cases fail explicitly, CI is green, and a complete sample workflow can be reproduced from a clean checkout.

## Phase 2 — Data Center Electrical Digital Twin

### Product outcome

A deterministic simulation platform for data-center electrical architectures and failure-response analysis.

### Minimum professional release

- topology model for utility supplies, switchgear, transformers, generators, UPS, ATS/STS, PDUs, and IT loads;
- N, N+1, and 2N redundancy configurations;
- component states, dependencies, switching rules, capacity limits, and protection-oriented constraints;
- event-driven failure, maintenance, restoration, and transfer scenarios;
- timeline, alarm, load-flow summary, stranded-capacity, and served-load outputs;
- synthetic Modbus/SCADA telemetry derived from the same simulation state;
- scenario comparison, replay, export, and explicit model limitations;
- versioned API, interactive topology and timeline views, PostgreSQL persistence, Docker, and CI.

### Exit gate

Reference scenarios have independently calculated expected outcomes, state transitions are deterministic and replayable, impossible topologies are rejected, and every displayed metric is traceable to a simulation event or input.

## Phase 3 — Energy Asset Investment Lab

### Product outcome

A reusable technical investment-analysis platform for renewable generation, BESS, pumped-storage hydro, hybrid assets, and selected critical-infrastructure investments.

### Minimum professional release

- explicit project, operating, financing, tax, inflation, and discount-rate assumptions;
- annual and sub-annual cash-flow models;
- NPV, IRR, MIRR, payback, discounted payback, LCOE, and LCOS;
- debt schedules, covenant indicators, and equity/project return separation;
- scenario comparison, one- and two-way sensitivities, stress cases, and seeded Monte Carlo analysis;
- transparent unit conventions, sign conventions, numerical tolerances, and reconciliation fixtures;
- versioned calculations, downloadable workbooks/reports, API, review interface, Docker, and CI.

### Exit gate

Every metric reconciles against an independent reference calculation, stochastic results are reproducible from recorded seeds, and invalid financing or cash-flow configurations fail with actionable explanations.

## Phase 4 — Critical Facilities Operations Platform

### Product outcome

A traceable workflow platform for operating and commissioning critical facilities.

### Minimum professional release

- asset hierarchy and location model;
- preventive and corrective maintenance workflows;
- versioned MOP, SOP, and EOP procedures with approvals;
- work permits, operational constraints, incidents, punch lists, and commissioning evidence;
- role-based access, immutable audit events, attachments, due dates, and escalation states;
- dashboards that separate operational facts from derived indicators;
- API, responsive interface, PostgreSQL, migrations, backups guidance, Docker, and CI.

### Exit gate

Authorization is enforced server-side, every workflow transition is auditable, concurrent updates are safe, retained evidence is integrity-checked, and recovery procedures are documented and tested.

## Phase 5 — Quantitative Portfolio & Risk Engine

### Product outcome

A reproducible research and risk engine for listed infrastructure, utilities, renewables, electrical manufacturers, and data-center securities.

### Minimum professional release

- licensed or explicitly redistributable market-data adapters plus deterministic synthetic fixtures;
- point-in-time universe construction and corporate-action-aware return series;
- transaction costs, turnover, rebalancing, and benchmark-aware backtesting without look-ahead or survivorship bias;
- volatility, drawdown, Sharpe, Sortino, VaR, CVaR, correlation, factor exposure, and contribution-to-risk analysis;
- constrained portfolio optimization, efficient-frontier analysis, seeded Monte Carlo, and documented stress scenarios;
- experiment manifests that record data versions, assumptions, parameters, software versions, and random seeds;
- versioned API, review interface, downloadable research report, Docker, and CI.

### Exit gate

Reference metrics reconcile against independent fixtures, anti-bias tests fail deliberately contaminated strategies, every result is reproducible from its experiment manifest, and no output is presented as personalized investment advice.

The engine covers liquid-market portfolio research. The Energy Asset Investment Lab remains the source for project-finance cash flows, debt structures, and asset-level techno-economics; neither product shares a database or domain model.

## Phase 6 — Professional Portfolio Website

### Product outcome

An accessible, fast, evidence-led website that presents the released portfolio through verified case studies rather than unsupported capability claims.

### Minimum professional release

- home, about, engineering experience, software skills, project index, case studies, résumé, and contact views;
- case studies with problem, constraints, architecture, decisions, validated outcomes, limitations, screenshots, and repository or demo links;
- content sourced from a versioned manifest pinned to public repository releases;
- responsive layout, keyboard support, semantic structure, reduced-motion support, and WCAG 2.2 AA checks;
- privacy-conscious analytics or no analytics, a minimal contact surface, security headers, dependency locking, and CI;
- automated link, accessibility, performance, and production-build checks plus documented deployment and rollback.

### Exit gate

Every project claim links to public evidence, all links and downloads resolve, the production build passes accessibility and performance budgets, no repository secrets or unpublished client material are bundled, and deployment is reproducible from a clean checkout.

The website is a presentation layer, not a second source of truth. Technical documentation, releases, and issue history remain in their product repositories; the GitHub profile stays the concise index.

## Portfolio-wide engineering standard

### Data and domain integrity

- Use SI units internally and display conversion explicitly.
- Record timezone, currency, price basis, and unit metadata with every dataset.
- Reject ambiguous, incomplete, duplicate, or non-finite inputs before calculation.
- Keep source inputs, normalized data, assumptions, outputs, and audit metadata distinguishable.
- Never present a data-quality or simulation tool as a substitute for licensed engineering judgment, applicable codes, studies, or site verification.

### Architecture

- Keep domain logic independent from web frameworks and presentation code.
- Use versioned REST APIs with generated OpenAPI contracts.
- Return machine-readable RFC 9457 Problem Details with stable error codes and request identifiers.
- Use PostgreSQL for durable application state and SQLite only for bounded local development or tests.
- Prefer deterministic request-lifecycle processing for small bounded workloads; introduce jobs and object storage only when justified by measured scale.
- Use `202 Accepted` job resources with immutable results for workloads that exceed the documented synchronous envelope.
- Apply SemVer to software releases and version data schemas and scientific models independently.
- Use Alembic from the first release that persists mutable application data.
- Share conventions and validated concepts across repositories, but do not create a common package until at least two products require the same stable implementation.
- Integrate products through versioned files or APIs; never share databases, ORM models, or migrations across repositories.

### Quality and security

- Lock dependencies and audit them in CI.
- Test domain invariants, boundary conditions, failure paths, API contracts, persistence, reports, and key browser workflows.
- Target at least 90% branch coverage in scientific and financial kernels, while treating uncovered invariants—not aggregate coverage—as the blocking signal.
- Build and smoke-test production containers against PostgreSQL in CI.
- Run formatting, linting, type checks, secret scanning, static analysis, dependency/license checks, and container scanning without unresolved critical or high findings.
- Bind local stacks to loopback by default and document authentication, TLS, secrets, retention, backup, and deployment responsibilities.
- Run application containers as non-root users and provide readiness and health checks.
- Bound uploads, expanded workloads, result sizes, numerical iterations, and generated reports.
- Keep secrets, personal operational data, client documents, and non-redistributable datasets out of public repositories.

### Documentation and product evidence

Every release must include:

- problem statement, intended users, non-goals, and engineering disclaimer;
- architecture and request or calculation flows;
- input/output contract, assumptions, units, rules, and limitations;
- fictional quick-start data and expected results;
- local and containerized setup;
- test and CI instructions;
- security and privacy notes;
- threat model, support policy, and vulnerability-reporting process;
- screenshots produced from real application state;
- a safe public demo and short demonstration video when the product can be hosted without exposing protected data;
- a versioned roadmap, changelog, release notes, SBOM, and artifact checksums.

## Definition of done

A project is not considered released until:

1. its primary workflow works from a clean checkout;
2. calculations and state transitions have independent reference fixtures;
3. tests cover success, boundary, malformed-input, and failure paths;
4. CI builds and tests the advertised deployment path;
5. documentation matches actual behavior;
6. sample data is fictional and reproducible;
7. security and resource limits are explicit and tested;
8. the interface has keyboard, responsive, empty, loading, error, and success states;
9. an independent read-only audit has no unresolved high-severity findings;
10. the release branch and public profile accurately describe its status.
