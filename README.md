# Football Hunter

> Football data collection, historical analysis, odds research, model discovery and prospective decision support in a dedicated .NET desktop application.

![VB.NET](https://img.shields.io/badge/VB.NET-.NET%2010-512BD4?logo=dotnet&logoColor=white)
![WinForms](https://img.shields.io/badge/UI-WinForms-512BD4)
![API](https://img.shields.io/badge/data-API--driven-0A66C2)
![Version](https://img.shields.io/badge/validated-v1.04-16A34A)
![Status](https://img.shields.io/badge/status-active%20development-orange)

## About the project

**Football Hunter** is a desktop research application I am building to collect, organise and analyse football data at scale.

The project combines historical match data, pre-match information and betting-market data with tools for statistical analysis, model discovery, prospective validation and decision support. Its purpose is not simply to display scores or odds: the application is being designed as a controlled research environment for testing whether repeatable, explainable patterns exist in football markets.

This repository is the **public showcase** for the project. The application source code, local data store, API credentials and proprietary datasets remain private.

## Current milestone — v1.04

The latest validated milestone introduces a **Daily Betting Desk** that brings several previously separate research layers into one operational workflow.

The user can choose a date/time interval — with a quick preset for the **next 168 hours** — and run a single analysis that combines:

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

### Example validated run

During validation of v1.04, a 168-hour analysis covered **1,716 scheduled matches**, found **66 with usable odds**, produced **30 candidates** and promoted **12** to the final analytical shortlist. A shorter ~24-hour test correctly reduced the universe to **42 matches**, **31 with odds**, **3 candidates** and **2 promoted selections**, confirming that the configurable time window is applied to the complete pipeline.

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

A validated calibration cohort currently contains **6,302 frozen predictions across 1,714 matches and four Champion models**, with the cohort audit reporting **0 critical integrity issues and 0 warnings** at the time of validation.

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
| **v1.04** | **Configurable Daily Betting Desk and ranked period shortlist** |

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

Running the validated prediction, odds, opportunity and simulated-risk pipeline over a user-selected time interval and presenting the strongest current candidates in one place.

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

🟠 **Active development — latest validated milestone: v1.04**

The application is already being used to collect and analyse real football data, run model searches, freeze prospective predictions and generate simulated analytical shortlists from current odds.

The next development stages continue to focus on model-health monitoring, prospective evidence and stronger decision auditing before any consideration of real-money automation.

## Screenshots

Selected screenshots will be added to this showcase as the public presentation evolves. They will focus on the interface, analysis workflows, prospective validation and Daily Betting Desk without exposing private credentials, source code or sensitive local data.

## About this repository

This repository intentionally contains **no application source code, API keys, private databases or proprietary datasets**. It exists to document and present Football Hunter publicly while development continues privately.

---

Built by [David Almeida](https://github.com/dmalmeida).
