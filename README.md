# Hey, I'm Spillai

I build personal tools to pressure-test my mental models and stay sharp on where AI adds leverage and where it breaks down. By trade, I'm a product leader with a decade across business, product, and engineering — focused on shipping products that create value.

---

## What I Build & Why

**Building forces clarity that thinking alone doesn't.** Every project requires making assumptions explicit — what does good look like, which tradeoffs matter, where AI helps vs. misleads. That accumulates into judgment you can't get any other way.

**Good decisions are rarely a single moment.** They're the result of deep thinking, translating an observation into a hypothesis, testing it against reality, and iterating. Most tools deliver an answer. The ones worth building support the full cycle — from a messy observation to a confident, well-reasoned action.

**People rarely ask for the right thing.** They ask for relief from a symptom. The real problem is usually one layer deeper — a workaround everyone has stopped questioning, a spreadsheet doing the job of a system. That gap between what exists and what should exist is where I look.

The hardest part of building isn't the build — it's knowing which problem is worth solving.

→ [Full framework: How and What I Build](PHILOSOPHY.md)

---

## Projects

### Real Estate

**Real Estate Investment Analysis Platform**
Ranks zip codes across a four-tier city system using statistical clustering on Zillow's ZHVI dataset, producing a prioritized investment shortlist with automated email reporting.
`Python` `pandas` `statsmodels` `SQLite/PostgreSQL` `Tableau`

**Real Estate Partnership Portfolio Dashboard**
20-year projection engine for a 7-partner investment partnership — models equity contributions, ARV acquisitions, rental income, debt paydown, and reinvestment cycles with real-time sliders.
`React` `Vite` `Recharts` `JavaScript`

<table width="100%">
  <tr>
    <td align="center"><img src="screenshots/RealEstate_PortfolioPlanner1.png" height="200"/></td>
  </tr>
</table>

---

### Quantitative & Personal Finance

**Quantitative Stock Trading System**
End-to-end pipeline: value screener → 20+ technical indicators → walk-forward backtesting across 1,000+ strategy combinations → live paper trading via Alpaca with Telegram alerts.
`Python` `Alpaca API` `PostgreSQL` `SQLAlchemy` `Telegram`

**Multi-Agent Qualitative Stock Research**
LLM-powered research framework evaluating companies across competitive positioning, management quality, and industry dynamics — designed to scale into a full multi-agent pipeline with Bull vs. Bear debate.
`Python` `Google Gemini` `PostgreSQL` `Alembic` `Click`

**Scenario-Based Retirement Calculator**
Models net worth to age 100 from a YAML-defined balance sheet. Supports discrete scenario toggles, Monte Carlo simulation over 1,000 iterations, and strategy presets.
`Python` `Streamlit` `Plotly` `Monte Carlo`

<table width="100%">
  <tr>
    <td width="50%" align="center"><img src="screenshots/Stock1.png" height="200"/></td>
    <td width="50%" align="center"><img src="screenshots/stock2.png" height="200"/></td>
  </tr>
</table>

---

### Interview Prep

**Job Search & Interview Funnel**
End-to-end pipeline for tracking job applications, managing interview stages, and surfacing conversion patterns across the funnel.

**AI-Powered PM Interview Evaluator**
Rubric-driven evaluation framework for PM interviews spanning APM through VP PM. Scores responses and generates calibrated feedback with level assessments using GPT and Gemini.
`Python` `OpenAI` `Google Gemini`

<table width="100%">
  <tr>
    <td width="50%" align="center"><img src="screenshots/JobSearch_InterviewFunnel_1.png" height="200"/></td>
    <td width="50%" align="center"><img src="screenshots/JobSearch_InterviewFunnel_3.png" height="200"/></td>
  </tr>
</table>

---

### Other

**Productivity: Google Calendar Aggregation & Notifications**
OAuth2 utility that aggregates Google Calendar events and routes alerts through Telegram. Built as a reusable foundation for calendar-driven automation.
`Python` `Google Calendar API` `Telegram`

**Automotive Depreciation & Cost-of-Ownership Analysis**
Depreciation curves and brand prestige rankings across a 100+ attribute vehicle dataset, surfacing true cost-of-ownership trade-offs.
`Python` `Tableau`

---

*Last updated: April 2026*
