# Football Hunter

> Football data collection, historical analysis, odds research, model discovery and prospective decision support in a dedicated .NET desktop application.

![VB.NET](https://img.shields.io/badge/VB.NET-.NET%2010-512BD4?logo=dotnet&logoColor=white)
![WinForms](https://img.shields.io/badge/UI-WinForms-512BD4)
![API](https://img.shields.io/badge/data-API--driven-0A66C2)
![Version](https://img.shields.io/badge/validated-v1.05-16A34A)
![Status](https://img.shields.io/badge/status-active%20development-orange)

## About the project

**Football Hunter** is a desktop research application I am building to collect, organise and analyse football data at scale.

The project combines historical match data, pre-match information and betting-market data with tools for statistical analysis, model discovery, prospective validation and decision support. Its purpose is not simply to display scores or odds: the application is being designed as a controlled research environment for testing whether repeatable, explainable patterns exist in football markets.

This repository is the **public showcase** for the project. The application source code, local data store, API credentials and proprietary datasets remain private.

## Current milestone — v1.05

The latest validated milestone turns Football Hunter's growing set of research tools into a clearer, observable daily workflow.

The main navigation is now organised around three distinct areas:

- **Day to day** — Dashboard, Daily Betting Desk, opportunity exploration and Auto Pilot;
- **Data and maintenance** — coverage, catalogue, historical imports, odds collection and data-source configuration;
- **Laboratory** — historical statistics, pre-match context, odds movement, backtesting and model discovery.

Long-running local operations now expose visible progress, elapsed time and the current processing stage instead of leaving the user uncertain about whether the application is still working.

### Daily Betting Desk and smart odds refresh

The **Daily Betting Desk** brings several previously separate research layers into one operational workflow. The user can choose a date/time interval — with a quick preset for the **next 168 hours** — and run a single analysis that combines:

1. validated model predictions;
2. current odds and fair-price analysis;
3. price and market-quality auditing;
4. opportunity scoring and filtering;
5. simulated risk/stake controls;
6. a ranked shortlist for the selected period.

The result is split between:

- **recommended candidates** — signals that pass the current model, market-quality and risk rules;
- **watch / not promoted** — signals that are retained with an explicit reason for exclusion or caution.

The Daily Betting Desk remains a **research and paper-simulation layer**. It does not place real bets.

Version 1.05 adds a **smart odds-refresh pipeline** that prioritises the most relevant Scanner signals and prices closest to expiry while protecting the API quota. It also makes the relationship between a new period analysis and previously frozen results explicit: a new analysis creates a fresh shortlist, while saved prospective observations can be consulted independently at any time.

### Prospective ledger and Champion health

The milestone also adds:

- a prospective ledger that freezes each shortlist before the match and resolves it later against real results;
- first-recommendation and first-strong-signal views without backfilling earlier history;
- per-Champion health screens covering calibration, maturity, drift, coverage and integrity;
- a simplified related-tools menu for reaching calibration, cohort audit, policy and correlation analysis without navigating through a long chain of windows.

### Example validated run

During validation of v1.05, one 168-hour analysis covered **1,703 scheduled matches**, found **185 with usable odds**, produced **41 candidates** and retained **10 recommendations** after the current market-quality and risk rules. The complete pipeline remained observable while running and the resulting shortlist was stored independently for later prospective resolution.

These figures are examples from one local validation run, not expected performance claims.

## Prospective validation

A major change in the project since the early backtesting stages is the addition of a prospective research workflow.

Football Hunter can now freeze model predictions before matches and follow them forward without rewriting the historical decision. This allows the application to compare what a model actually said in advance with what happened later.

The current workflow includes:

- immutable validated-model snapshots;
- prospective prediction capture;
- shadow validation;
- paper-betting simulation;
- risk and stake simulation;
- portfolio stress testing;
- policy comparison;
- prospective evidence tracking;
- calibration monitoring;
- cohort-integrity auditing.

A validated calibration cohort currently contains **6,418 frozen predictions across 1,750 matches and four Champion models**, with **68 resolved observations**. The cohort audit reported **0 critical integrity issues and 0 warnings** at the time of v1.05 validation.

## Model discovery and Champion workflow

The **Opportunity Hunter** workflow automatically explores combinations of pre-match features, windows and weights instead of relying only on manual filter-by-filter testing.

Model discovery is deliberately separated from final evaluation. Candidate models move through controlled stages before a model can be treated as a validated **Champion**.

Examples of pre-match features used or explored include:

- recent home and away performance;
- points-per-game and win/loss form;
- goals scored and conceded;
- overall recent form;
- opponent strength and scheduling context;
- market-specific goal and BTTS statistics;
- attacking and defensive interactions;
- derived home/away strength indicators.

The current validated set covers four targets across **1X2** and **Over/Under 2.5** markets.

## Model evaluation

Football Hunter is built around a strict separation between **model discovery**, **out-of-sample validation**, **sealed final evaluation** and **prospective observation**.

Important evaluation concepts include:

- out-of-sample testing;
- sealed final samples;
- immutable model snapshots;
- estimated probability;
- fair odds;
- edge versus market price;
- expected value;
- calibration metrics such as Brier score and ECE;
- ROI and robustness;
- minimum sample-size requirements;
- prevention of data leakage.

A high historical hit rate by itself is not considered sufficient evidence that a model is useful.

## Risk and portfolio research

The project also includes a fully simulated portfolio layer so that model quality can be studied separately from money management.

Current research components include:

- Kelly-based stake simulation with conservative caps;
- per-signal, per-market/day and daily exposure limits;
- portfolio stress simulations;
- correlation stress scenarios;
- guardrail-policy comparison;
- prospective A/B policy evaluation.

These layers are deliberately read-only or simulated and do not alter historical model decisions.

## What Football Hunter is designed to do

- Collect football competitions, teams, fixtures and historical results.
- Import and organise large volumes of historical match data.
- Work with pre-match odds across markets such as **1X2** and **Over/Under**.
- Analyse home/away form, goals, results and other pre-match features.
- Compare historical patterns across leagues, countries and seasons.
- Search automatically for promising statistical models.
- Evaluate models on genuinely separated samples.
- Freeze prospective predictions and audit their integrity later.
- Compare model probability with fair and available market prices.
- Rank current opportunities while explaining why alternatives were rejected.
- Keep historical calculations free from future information.

## Selected development milestones

| Version | Milestone |
| --- | --- |
| v0.94 | Initial Git baseline for the private application repository |
| v0.95 | Paper-betting simulation |
| v0.96 | Risk and stake simulation |
| v0.97 | Portfolio stress analysis |
| v0.98 | Correlation-stress scenarios |
| v0.99 | Portfolio guardrail Policy Lab |
| v1.00 | Prospective Policy A/B pilot |
| v1.01 | Prospective evidence monitoring |
| v1.02 | Prospective calibration workflow |
| v1.03 | Calibration-cohort integrity audit |
| v1.04 | Configurable Daily Betting Desk and ranked period shortlist |
| **v1.05** | **Smart odds refresh, prospective ledger, Champion health, observable progress and simplified navigation** |

## Application areas

### Data collection

Collection and maintenance of competitions, seasons, fixtures, results and related historical information.

### Odds research

Importing and analysing pre-match market data, comparing market probabilities, available prices, price quality and bookmaker coverage.

### Historical analysis

Exploring performance and event patterns across leagues, countries, seasons and match contexts.

### Backtesting

Testing hypotheses against historical data with an emphasis on chronological correctness and strict sample separation.

### Opportunity discovery

Automatically searching a much larger model space than would be practical through manual dropdown-by-dropdown testing.

### Prospective monitoring

Freezing model outputs before matches and tracking their subsequent performance, calibration and stability.

### Daily Betting Desk

Running the validated prediction, smart odds-refresh, opportunity and simulated-risk pipeline over a user-selected time interval, presenting the strongest current candidates and preserving their prospective observations for later resolution.

## Technology

| Area | Technology |
| --- | --- |
| Language | VB.NET |
| Runtime | .NET 10 |
| Desktop UI | Windows Forms |
| Data sources | Football APIs and odds data |
| Analysis | Statistical feature engineering, backtesting and prospective validation |
| Architecture | Local desktop research application |
| Versioning | Git/GitHub with validated annotated release tags |

## Engineering challenges

The project deals with practical engineering problems that become important once football data grows beyond a small prototype:

- importing large historical datasets without freezing the user interface;
- handling API quotas and interrupted imports safely;
- keeping long-running operations observable through progress indicators and elapsed-time feedback;
- normalising high-volume odds data to control database growth;
- distinguishing genuine missing data from incomplete provider coverage;
- preventing historical analysis from using information unavailable before a match;
- preserving immutable prospective decisions;
- keeping the desktop interface responsive while analysis runs in the background;
- combining model, price, risk and portfolio layers without silently changing the underlying model output.

## Development approach

Football Hunter is developed iteratively, with frequent small releases and direct validation of each workflow.

The current approach emphasises:

- **data integrity first** — statistical conclusions are only as good as the underlying data;
- **explainability** — useful models should be understandable, not just numerically attractive;
- **out-of-sample discipline** — model selection and final evaluation remain separate;
- **prospective evidence** — historical backtests are supplemented by frozen forward observations;
- **responsive UX** — long operations need progress, cancellation where appropriate and clear state feedback;
- **scalability** — data structures and imports must remain workable as the database grows;
- **incremental refinement** — new capabilities are added and validated in controlled steps.

## Project status

🟠 **Active development — latest validated milestone: v1.05**

The application is already being used to collect and analyse real football data, run model searches, freeze prospective predictions and generate simulated analytical shortlists from current odds.

The next development stages continue to focus on accumulating prospective evidence, monitoring Champion health and strengthening decision auditing before any consideration of real-money automation.

## Screenshots

### Daily workflow and reorganised navigation

The main interface separates daily decisions from data maintenance and research tools, keeping advanced screens available without crowding the primary workflow.

![Football Hunter v1.05 dashboard and reorganised navigation](docs/images/v105-navigation-dashboard.png)

### Observable long-running operations

Coverage and other heavy local analyses now show the current stage, elapsed time and visible progress while keeping the interface responsive.

![Football Hunter v1.05 coverage analysis with visible progress](docs/images/v105-coverage-progress.png)

### Daily Betting Desk

The Daily Betting Desk ranks the best current analytical candidates and retains alternatives with an explicit reason for not promoting them.

![Football Hunter v1.05 Daily Betting Desk](docs/images/v105-daily-betting-desk.png)

### Prospective research laboratory

The laboratory keeps real prospective records, model calibration, fair-price analysis, shadow validation, paper simulation and risk research separate but accessible from one workspace.

![Football Hunter v1.05 prospective research laboratory](docs/images/v105-prospective-lab.png)

## About this repository

This repository intentionally contains **no application source code, API keys, private databases or proprietary datasets**. It exists to document and present Football Hunter publicly while development continues privately.

---

Built by [David Almeida](https://github.com/dmalmeida).
