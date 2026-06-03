# Hi there, I'm Christian Verdin

**Senior Data Scientist & AI/ML Engineer** with 7+ years of experience designing, developing, and deploying end-to-end ML/AI systems, from data pipelines and production models to complete applications that drive real business impact.

I build production-grade systems that integrate LLMs, real-time data pipelines, and modern web frameworks to solve complex analytical problems.

> The projects below are personal builds — production-deployed, written outside of work hours, and built end-to-end by me.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:christiandverdin@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-dailylocks.ai-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dailylocks.ai)
[![Medium](https://img.shields.io/badge/Medium-Articles-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@cver123/about)

---

## Projects at a Glance

| Project | What it does | Status | Stack |
| --- | --- | --- | --- |
| [**312Deals**](#312deals---chicago-food--drink-deals) | Chicago food & drink deals, 12,700+ venues, 36,000+ deals, 137 neighborhoods, multi-channel agent surface (REST · 11-tool MCP · custom GPT · in-app AI chat) | Live | Next.js · FastAPI · SQLite · MCP |
| [**LakeshoreIQ**](#lakeshoreiq---illinois-real-estate-intelligence) | Illinois real estate intelligence, 9 data sources spanning real estate, government open data, school data, demographics, and crime/safety; 50+ neighborhoods; B2B API; 10-tool MCP server | Live · Open Beta | Next.js · FastAPI · PostgreSQL |
| [**Daily Locks AI**](#daily-locks-ai) | An AI multi-agent orchestrator and full-stack application that turns pitcher stats, batting metrics, park factors, and live odds into model-driven daily MLB insights, player-prop analysis, and live in-game value detection. Includes a natural-language chat agent with multi-model LLM routing and tracing/observability on the chat path. (currently MLB; prior NFL & NCAAB seasons archived) | Live · Open Beta | Next.js · FastAPI · Python · LLM API |
| [**NFL Analytics**](#nfl-analytics-engine) | Pure R analytics engine — full-season game & player processing, quarter-by-quarter scoring models, automated matchup reports, and a custom playoff visualization suite | 2025-26 Complete | R · ggplot2 · SQLite |
| **MLB 2026** | Production modeling pipeline, daily run cadence, alpha-pattern detection across historical splits, automated third-party odds verification, auto-deploy | Live (in-season) | R · Python · PostgreSQL |

### Popular Use Cases

- **LakeshoreIQ**: Property evaluation with AVM + rent estimates, side-by-side ZIP-code market comparison, school district analysis, investment cash-flow modeling, daily first-mover listing alerts via automated email
- **312Deals**: Real-time "happening now" deal discovery, neighborhood and cuisine filtering, seasonal event guides (St. Patrick's Day, Mother's Day), university-area deal browsing, AI agent integration via MCP and custom GPT
- **Daily Locks AI**: Model-driven daily picks and best bets, player-prop & first-5-innings analysis, live in-game value detection, and a natural-language AI chat for matchup and betting-angle questions
- **NFL Analytics**: Automated per-game matchup intelligence reports, playoff scenario simulation, player trend & breakout detection, and custom multi-panel dashboards for skill-position analysis
- **MLB 2026**: Daily pregame model predictions, alpha-pattern detection across historical splits, third-party odds verification before publish, automated deploy

---

## Featured Projects

### 312Deals - Chicago Food & Drink Deals
**AI-Powered Restaurant Deal Intelligence Platform with Multi-Agent Pipeline & MCP Server**

A production platform aggregating **12,700+ venues**, **36,000+ active deals**, and **137 neighborhoods** across Chicagoland. Multi-channel delivery (18-endpoint REST API, 11-tool MCP Server, custom GPT, in-app AI chat) all backed by a single SQLite database. Features an automated deal collection pipeline using LLM extraction across web, social media, and email-based content sources, with content hashing (~60-80% API cost savings), adaptive scheduling, and **5,810 tracked deal sources**. Weekly "Deal Sheet" newsletter via authenticated transactional email (DKIM/SPF/DMARC). Multi-select filters for neighborhoods, cuisines, and deal types with collapsible sidebar. Seasonal content guides (St. Patrick's Day) and active SEO campaign with 2,520+ Google-indexed pages.

**Live:** [312deals.com](https://312deals.com)

<p align="center">
  <img src="./images/312deals/plausible_312_april.png" width="800" alt="312Deals - Plausible Analytics (April Traffic)">
</p>

<p align="center">
  <img src="./images/312deals/09_search-results.png" width="800" alt="312Deals - Search Results with Filters">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/312deals/desktop-home-fresh.png" width="800" alt="312Deals - Homepage">
</p>
<p align="center">
  <img src="./images/312deals/1_Neighborhoods.png" width="800" alt="312Deals - Neighborhoods Browser">
</p>
<p align="center">
  <img src="./images/312deals/04_Patio_DrinkCategory_1.png" width="800" alt="312Deals - Patio & Drink Category Filtering">
</p>
<p align="center">
  <img src="./images/312deals/07_Wings_TR.png" width="800" alt="312Deals - Cuisine-Specific Deal Discovery">
</p>
<p align="center">
  <img src="./images/312deals/02_MothersDay_1.png" width="800" alt="312Deals - Mother's Day Seasonal Guide">
</p>
<p align="center">
  <img src="./images/312deals/02_MothersDay_2.png" width="800" alt="312Deals - Mother's Day Seasonal Guide (cont.)">
</p>
</details>

**Key Capabilities:**
- **18-Endpoint REST API**: Geo-proximity search, multi-faceted filters, autocomplete, and a multi-stop bar crawl planner
- **11-Tool MCP Server + Custom GPT + AI Chat**: Deal search, neighborhood comparison, featured picks, and weekly digests exposed as agent-callable tools, plus an in-app `/chat` interface
- **Multi-Source Deal Pipeline**: 5,810+ tracked sources with content hashing for ~60-80% cost savings and adaptive scheduling with exponential backoff
- **AI Extraction Pipeline**: LLM parses unstructured content into structured deals with schema validation and automated quality scoring (0-100)
- **Time-Aware Search & Community Verification**: Timezone-aware "happening now" filtering plus user-driven verification queue
- **Seasonal Content Guides + 100+ SEO Landing Pages**: Programmatic event, neighborhood, university, and cuisine pages with structured-data markup
- **PWA with Offline Support**: Installable mobile app with service-worker caching

**Architecture & Technical Highlights:**
- **Frontend:** Next.js + TypeScript with Tailwind, server-state library, dark mode, PWA
- **Backend:** Async Python (FastAPI) with 18 endpoints, rate limiting, and retry logic
- **Database:** SQLite with WAL mode and full-text search, 80+ venue metadata columns
- **AI:** LLM-based extraction and verification with schema-validated outputs and automated quality scoring
- **Pipeline:** Multi-source content ingestion → LLM extraction → quality scoring → publish (weekly automated refresh, 7 phases)
- **Deployment:** Serverless frontend + managed backend, scheduled cron via CI
- **Email:** Authenticated transactional + newsletter delivery with one-click unsubscribe

**Built With:**

`Next.js` `TypeScript` `FastAPI` `Python` `SQLite` `LLM API` `MCP / FastMCP` `Tailwind CSS`

---

### LakeshoreIQ - Illinois Real Estate Intelligence
**Full-Stack Property Search, Valuation & Market Analysis Platform**

A production SaaS application aggregating **9 real-time data sources** to deliver property search, automated valuations, market analysis, and neighborhood intelligence across **150+ Illinois cities** and **50+ Chicago neighborhoods**. Integrates census demographics, school quality ratings, crime statistics, development activity tracking, and economic indicators into a unified property analysis experience. Features a **B2B API** with tiered pricing, **10-tool MCP server**, and **15+ backend services**.

**Live:** [lakeshoreiq.com](https://lakeshoreiq.com)

<p align="center">
  <img src="./images/illinois_real_estate/property_details.png" width="800" alt="LakeshoreIQ - Property Details with Neighborhood Intelligence">
</p>

<p align="center">
  <img src="./images/illinois_real_estate/amenity_drilldown.png" width="800" alt="LakeshoreIQ - Amenity Drilldown">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/illinois_real_estate/crime_safety.png" width="800" alt="LakeshoreIQ - Crime & Safety Analysis">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/FirstMover_1.png" width="800" alt="LakeshoreIQ - First-Mover Daily Email">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/FirstMover_2.png" width="800" alt="LakeshoreIQ - First-Mover Detail View">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/landing_hero_1.png" width="800" alt="LakeshoreIQ - Landing">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/school_ratings.png" width="800" alt="LakeshoreIQ - School Ratings">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/search_results.png" width="800" alt="LakeshoreIQ - Property Search Results">
</p>
<p align="center">
  <img src="./images/illinois_real_estate/valuation_calculator.png" width="800" alt="LakeshoreIQ - Valuation & Investment Calculator">
</p>
</details>

**Key Capabilities:**
- **Property Search Engine**: Multi-faceted filters across location, property type, size, price, and listing-age dimensions with imagery
- **Automated Valuations & Investment Modeling**: AVM with confidence scoring, rent comparables, and full investment calculator (cash flow, cap rate, cash-on-cash, 5-year ROI)
- **Market & Neighborhood Intelligence**: ZIP-level sale/rental metrics, side-by-side comparisons, multi-category amenity scoring with walkability proxy and drilldown
- **Public-Data Layers**: Crime/safety scoring with trend detection, development activity tracking, 5,000+ school quality ratings, county-level economic indicators, ZIP-level demographics
- **SaaS Monetization**: Tiered subscription model with usage metering and feature gating, plus a B2B API tier with developer portal
- **10-Tool MCP Server**: Property, market, and intelligence layers exposed as agent-callable tools

**Architecture & Technical Highlights:**
- **Frontend:** Next.js + React + TypeScript with Tailwind, charts, and lightweight state management
- **Backend:** Async Python (FastAPI) with tiered Redis caching and schema-validated request/response handling
- **Database:** Managed PostgreSQL with row-level security; SQLite for static reference data
- **Auth & Billing:** JWT-based auth with email verification; subscription billing with webhooks and customer portal
- **Data Layer:** 9 third-party / public data sources with usage-aware caching strategy
- **Deployment:** Serverless frontend + managed backend, env-driven config

**Built With:**

`Next.js` `React` `TypeScript` `FastAPI` `Python` `PostgreSQL` `Redis` `SQLite` `Tailwind CSS`

---

### NFL Analytics Engine
**Statistical Intelligence & Visualization Platform** | *2025-26 Season Complete ✅*

A comprehensive analytics system for NFL game prediction, processing full-season game, player-quarter, snap-count, and touchdown data through Super Bowl LX (SEA over NE). Features automated matchup reports, real-time visualization generation, and predictive pattern recognition across multiple seasons of historical game outcomes.

<p align="center">
  <img src="./images/nfl_analytics/02_quarter_predictions.png" width="800" alt="NFL Analytics - Quarter-by-Quarter Score Predictions">
</p>

<p align="center">
  <img src="./images/nfl_analytics/20_skill_position_matchups.png" width="800" alt="NFL Analytics - Skill Position Matchups Dashboard">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/nfl_analytics/2_efficiency_matrix.png" width="800" alt="NFL Analytics - Team Efficiency Matrix">
</p>
<p align="center">
  <img src="./images/nfl_analytics/1_playoff_epa_comparison.png" width="800" alt="NFL Analytics - EPA Comparison Analysis">
</p>
<p align="center">
  <img src="./images/nfl_analytics/3_quarter_scoring_heatmap.png" width="800" alt="NFL Analytics - Quarter Scoring Heatmap">
</p>
</details>

**Key Capabilities:**
- **Matchup Intelligence System**: Multi-page reports per game with player trends, red-zone efficiency, and situational analysis
- **Quarter-by-Quarter Tracking**: Touchdown events and player stat records with Q1–Q4 breakdowns
- **Visualization Engine**: Custom playoff visualizations including skill-position dashboards, TD probability gauges, and clutch performer analysis
- **Playoff Scenario Simulator**: Win/loss impact modeling for seeding and elimination risk
- **Player Trend Analysis**: Usage-shift detection and breakout identification

**Technical Highlights:**
- **Data Pipeline:** R-based ETL processing a broad set of metrics per game with SQLite persistence
- **Statistical Modeling:** EPA calculations, efficiency matrices, trend detection
- **Visualization:** ggplot2 with custom theming and multi-panel dashboards
- **Database & Automation:** Core and quarter-level tracking tables; parallel batch matchup processing

**Built With:**

`R` `tidyverse` `ggplot2` `SQLite`

---

### Daily Locks AI
**AI Sports-Betting Analytics Agent with LLM-Powered Chat & Model-Driven Daily Picks**

A full-stack application featuring an agentic AI system that turns pitcher stats, batting metrics, park factors, and sportsbook odds into model-generated daily predictions — positioned as "your research, done." Currently focused on MLB for the 2026 season, with prior NFL and NCAAB seasons archived (code preserved in-repo). Delivers confidence-tiered picks with edge-vs-Vegas analysis, player-prop coverage (home runs, hits, total bases, walks, strikeouts), first-5-innings plays, team power rankings, live in-game value detection, and a natural-language chat agent.

**Live:** [dailylocks.ai](https://dailylocks.ai)

<p align="center">
  <img src="./images/dailylocks/desktop-conference-tournaments.png" width="800" alt="Daily Locks AI - Conference Tournament Tracker">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/dailylocks/desktop-ai-chat.png" width="800" alt="Daily Locks AI - AI Chat Interface">
</p>
<p align="center">
  <img src="./images/dailylocks/mlb-picks.png" width="800" alt="Daily Locks AI - MLB Picks">
</p>
<p align="center">
  <img src="./images/dailylocks/mlb-props.png" width="800" alt="Daily Locks AI - MLB Props">
</p>
</details>

**Key Features:**
- **Model-Driven Daily Picks**: Confidence-tiered recommendations with positive-edge detection against sportsbook lines
- **Player Prop & First-5 Analysis**: HR, hits, total bases, walks, and strikeout markets plus starter-quality first-5-innings plays
- **Live In-Game Value Detection**: Real-time score monitoring with game-state-aware recommendation adjustments
- **Natural-Language Chat Agent**: Reasoning-shaped questions route to an LLM with the full daily research bundle as cached context; fast deterministic handlers answer list/table lookups at zero model cost
- **Subscription Tiers**: Freemium access with metered AI usage and tiered model access, billed via Stripe
- **Archived Seasons**: NFL and NCAAB engines preserved in-repo from prior seasons

**Architecture & Technical Highlights:**
- **Frontend:** Next.js + React + TypeScript with state management and analytics
- **Backend:** Async Python (FastAPI) on a Dockerized service with intelligent query routing
- **AI:** LLM-powered chat with cached research context, multi-model routing by tier, and deterministic handler bypass for cost-zero queries
- **Live Data:** Public sports-API integration with periodic polling and game-state matching
- **Database & Auth:** Supabase (PostgreSQL) with row-level security; JWT auth and Stripe subscription billing with webhooks
- **Data Pipeline:** Automated daily R model pipeline → CSV sync → frontend deploy
- **Observability:** LLM tracing and usage analytics on the chat path

**Built With:**

`Next.js` `React` `TypeScript` `FastAPI` `Python` `LLM API` `PostgreSQL` `Tailwind CSS`

---

### NCAAB Analytics
**College Basketball Prediction System** | *2025-26 Season Complete*

A production-grade analytics pipeline for NCAA Men's Basketball that combined possession-based efficiency metrics with real-time Vegas odds to generate daily game predictions, second-half scoring models, race-to-points analysis, and conference tournament intelligence — with fatigue modeling, rest-day adjustments, and head-to-head context for tournament play. Powered the Daily Locks AI prediction engine during the 2025-26 season; the full season is finished and the model is archived.

<p align="center">
  <img src="./images/ncaab_architecture.svg" width="800" alt="NCAAB Analytics Architecture"/>
</p>

**Key Capabilities:**
- Possession-based efficiency metrics (KenPom-style) normalized per 100 possessions
- Iterative strength-of-schedule calculation
- Volatility detection for high-variance matchups
- +EV edge detection comparing model probability vs. implied probability
- Conference tournament analysis with fatigue, rest, and head-to-head modeling
- Pick review system for tracking agent picks by tier
- Automated daily pipeline: data import → odds fetch → predictions → CSV sync

**Technical Highlights:**
- **Data Pipeline:** R-based ETL processing full NCAA Division I team and game data with daily incremental updates
- **Statistical Modeling:** Four-factor analysis, adaptive recency weighting, form detection
- **Odds Integration:** Real-time third-party odds with consensus aggregation
- **Database:** SQLite with optimized analytical schema
- **Agent Integration:** Daily CSV exports synced to Daily Locks AI

**Built With:**

`R` `tidyverse` `SQLite` `Statistical Modeling`

---

## Technical Skills

<table>
<tr>
<td valign="top" width="33%">

### Languages
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

</td>
<td valign="top" width="33%">

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

</td>
<td valign="top" width="33%">

### Backend & Data
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

</td>
</tr>
<tr>
<td valign="top" width="33%">

### AI & ML
![LLM_API](https://img.shields.io/badge/LLM_API-191919?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP/FastMCP-191919?style=flat-square&logo=anthropic&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=flat-square&logo=chainlink&logoColor=white)
![Prompt_Engineering](https://img.shields.io/badge/Prompt_Engineering-4F46E5?style=flat-square&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-7C3AED?style=flat-square&logoColor=white)

</td>
<td valign="top" width="33%">

### Infrastructure
![Serverless](https://img.shields.io/badge/Serverless-FD5750?style=flat-square&logo=serverless&logoColor=white)
![REST_API](https://img.shields.io/badge/REST_API-009688?style=flat-square&logoColor=white)
![Webhooks](https://img.shields.io/badge/Webhooks-1A73E8?style=flat-square&logoColor=white)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=flat-square&logo=telegram&logoColor=white)

</td>
<td valign="top" width="33%">

### Tools
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

</td>
</tr>
</table>

---

## Let's Connect

I'm always open to collaborating on projects together so feel free to reach out!

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/"><img src='https://img.icons8.com/color/2x/linkedin.png' alt='linkedin' height='40'></a>
  <a href="https://github.com/ChristianVerdin"><img src='https://img.icons8.com/material-outlined/24/000000/github.png' alt='github' height='40'></a>
  <a href="https://medium.com/@cver123/about"><img src='https://img.icons8.com/color/2x/medium-logo.png' alt='Medium' height='40'></a>
</p>

<p align="center">
  <i>Building AI-powered products across real estate, local commerce, and sports analytics.</i>
</p>

<p align="center">
  <a href="mailto:christiandverdin@gmail.com">christiandverdin@gmail.com</a>
</p>
