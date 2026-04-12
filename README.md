# Spillai

AI product leader with a decade building enterprise AI/ML products — bridging business strategy, data science, and systems architecture to drive measurable outcomes. I build personal tools at the intersection of AI and finance to pressure-test my mental models and stay sharp on where AI adds leverage and where it breaks down.

---

## What I Build & Why

I don't build to explore technology. I build to collapse the gap between a problem I understand deeply and a solution that didn't exist before.

**How I decide what to build**
- **Personal domain fluency first** — I only build in domains where I have enough context to know when the output is wrong. Real estate, quant finance, and PM workflows are areas I've operated in, not researched.
- **Structural problems over surface pain** — The signal is when a spreadsheet is load-bearing. If someone's critical decision-making lives in a fragile, manual artifact, there's a product gap.
- **Insight as the moat** — AI levels implementation. What it can't replicate is judgment about which problem is worth solving, which tradeoff matters, and what "good" looks like in a specific domain.
- **Compounding over features** — Each tool I build feeds the next. The stock screener informs the retirement model. The interview evaluator informs how I think about PM judgment frameworks.

**The test I apply before building**
> *If a capable engineer had infinite time, would they build this for themselves?* If yes, it's probably not differentiated. The interesting problems are the ones where domain knowledge — not engineering skill — is the bottleneck.

→ [Full framework: How I Build with AI](PHILOSOPHY.md)

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
