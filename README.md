# Hi there, I'm Christian Verdin

**Data Scientist & Full-Stack Engineer** with 7+ years of experience designing, developing, and delivering end-to-end data science, ML, and AI solutions that drive real business impact.

I build production-grade applications that integrate LLMs, real-time data pipelines, and modern web frameworks to solve complex analytical problems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:christiandverdin@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-dailylocks.ai-4285F4?style=for-the-badge&logo=google-chrome&logoColor=white)](https://dailylocks.ai)
[![Medium](https://img.shields.io/badge/Medium-Articles-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@cver123/about)

---

## Featured Project

### NFL Analytics Engine
**Sports Performance Analytics & Data Engineering Platform**

A comprehensive analytics system processing 100,000+ NFL plays across 4 seasons (997 games), featuring automated ETL pipelines, EPA efficiency modeling, and statistical analysis for playoff scenario comparison.

<p align="center">
  <img src="./assets/nfl_analytics/2_efficiency_matrix.png" width="800" alt="NFL Analytics - Team Efficiency Matrix">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/nfl_analytics/1_playoff_epa_comparison.png" width="800" alt="NFL Analytics - EPA Comparison Analysis">
</p>
<p align="center">
  <img src="./assets/nfl_analytics/3_quarter_scoring_heatmap.png" width="800" alt="NFL Analytics - Quarter Scoring Heatmap">
</p>
<p align="center">
  <img src="./assets/nfl_analytics/6_red_zone_breakdown.png" width="800" alt="NFL Analytics - Red Zone Efficiency Analysis">
</p>
</details>

**Key Capabilities:**
- EPA (Expected Points Added) efficiency modeling across 997 games
- Quarter-by-quarter scoring pattern analysis with heatmap visualization
- Red zone and third-down conversion efficiency breakdowns
- Automated report generation with CSV/PDF/SVG exports
- Risk-reward analysis for playoff matchup scenarios

**Sample Output:** [Divisional Round 2026 Analysis (PDF)](./assets/nfl_analytics/outputs/2026_nfl_divisional_round_analysis/nfl_divisional_round_complete_analysis.pdf)

**Technical Highlights:**
- **Data Pipeline:** R-based ETL processing 500+ metrics per game via nflreadr API
- **Statistical Modeling:** EPA calculations, efficiency matrices, regression analysis
- **Visualization:** ggplot2 with custom themes, multi-format exports (PNG/SVG/PDF)
- **Database:** SQLite with optimized aggregation queries across 4 seasons
- **Automation:** Scheduled analysis generating weekly intelligence reports

**Built With:**

`R` `tidyverse` `ggplot2` `SQLite` `nflreadr` `Cairo` `Markdown`

---

### AI Real Estate System
**Multi-Platform Property Aggregation & Analysis**

A full-stack application that aggregates real estate listings from 5 major platforms (Zillow, Redfin, Trulia, Realtor.com, Homes.com), applying AI-powered extraction to deliver unified property data with interactive mapping and investment analytics.

<p align="center">
  <img src="./assets/ai_real_estate/search_interface.png" width="800" alt="AI Real Estate - Search Interface">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/ai_real_estate/property_results.png" width="800" alt="AI Real Estate - Property Results">
</p>
<p align="center">
  <img src="./assets/ai_real_estate/map_view.png" width="800" alt="AI Real Estate - Interactive Map">
</p>
<p align="center">
  <img src="./assets/ai_real_estate/analytics_dashboard.png" width="800" alt="AI Real Estate - Analytics Dashboard">
</p>
</details>

**Key Features:**
- Multi-platform data aggregation from 5 real estate websites
- AI-powered property extraction using Firecrawl + OpenAI GPT
- Three-tier caching system (Memory -> Redis -> SQLite)
- Interactive mapping with geocoded property locations
- Investment analytics with ROI and cap rate calculations

**Technical Highlights:**
- **Frontend:** Streamlit with custom components, Plotly visualizations
- **Backend:** Python with async HTTP clients, circuit breaker pattern
- **AI/ML:** OpenAI GPT for intelligent data extraction and normalization
- **Caching:** Multi-tier LRU cache with 65-70% hit rate optimization
- **Data:** Pydantic schemas, pandas processing, multi-format exports

**Built With:**

`Python` `Streamlit` `OpenAI API` `Firecrawl` `Redis` `SQLite` `Pandas` `Folium` `Plotly`

---

### Daily Locks AI
**Production SaaS Platform with LLM-Powered Analytics**

A full-stack application featuring agentic AI that processes natural language queries against 15,000+ historical records, delivering structured insights with confidence scoring and real-time streaming responses.

**Live:** [dailylocks.ai](https://dailylocks.ai)

<p align="center">
  <img src="./assets/dailylocks/chat_interface.png" width="800" alt="Daily Locks AI - Chat Interface">
</p>

<details>
<summary><b>View More Screenshots</b></summary>
<br>
<p align="center">
  <img src="./assets/dailylocks/ai_response.png" width="800" alt="Daily Locks AI - Analysis Response">
</p>
<p align="center">
  <img src="./assets/dailylocks/games_dashboard.png" width="800" alt="Daily Locks AI - Games Dashboard">
</p>
<p align="center">
  <img src="./assets/dailylocks/settings_page.png" width="800" alt="Daily Locks AI - Settings & Billing">
</p>
</details>

**Key Features:**
- Natural language interface with context-aware prompt engineering
- Multi-model LLM routing (Claude Haiku/Sonnet/Opus) based on user tier
- Real-time streaming responses with Server-Sent Events
- Subscription management with Stripe Checkout & Customer Portal
- Persistent conversation history with full-text search

**Architecture & Technical Highlights:**
- **Frontend:** Next.js 15 App Router, React 19, TypeScript, Zustand state management
- **Backend:** FastAPI with async endpoints, intelligent agent routing system
- **AI/ML:** Anthropic Claude API, dynamic prompt construction, context windowing
- **Database:** Supabase (PostgreSQL) with Row-Level Security, real-time subscriptions
- **Auth:** JWT-based authentication with protected API routes
- **Payments:** Stripe integration (checkout sessions, webhooks, customer portal)
- **Data Pipeline:** Automated ETL processing 500+ records weekly via Playwright
- **Testing:** 116 automated tests with pytest

**Built With:**

`Next.js 15` `React 19` `TypeScript` `FastAPI` `Python` `Claude API` `Supabase` `Stripe` `Tailwind CSS` `Zustand` `Playwright`

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
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

</td>
</tr>
<tr>
<td valign="top" width="33%">

### AI & ML
![Claude](https://img.shields.io/badge/Claude_API-191919?style=flat-square&logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-121212?style=flat-square&logo=chainlink&logoColor=white)

</td>
<td valign="top" width="33%">

### Infrastructure
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?style=flat-square&logo=stripe&logoColor=white)

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
  <i>Open to opportunities in AI/ML engineering, full-stack development, and data-intensive applications.</i>
</p>

<p align="center">
  <a href="mailto:christiandverdin@gmail.com">christiandverdin@gmail.com</a>
</p>
