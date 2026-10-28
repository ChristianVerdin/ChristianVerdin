# Christian Verdin

**AI engineer and senior data scientist who ships agentic systems to production and keeps them running.**

Eight years of production ML at Fortune 500 scale. By day I lead production AI for a Fortune 500 data science team: a multi-agent analytics platform on Databricks used by hundreds of business users, the evaluation and observability layer behind it, and the MCP surface that lets other AI clients call it. By night I ship the projects below: production-deployed, written outside work hours, built end to end by me, and run through real platform reviews (Apple App Store, Amazon Ring Appstore).


[![LinkedIn](https://img.shields.io/badge/LinkedIn-christian--verdin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Email](https://img.shields.io/badge/Email-christiandverdin%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:christiandverdin@gmail.com)
[![Live](https://img.shields.io/badge/Live-312deals.com-0F6E6E?style=for-the-badge&logo=google-chrome&logoColor=white)](https://312deals.com)
[![App Store](https://img.shields.io/badge/App_Store-CFB_GameDay_Board-0D96F6?style=for-the-badge&logo=apple&logoColor=white)](https://apps.apple.com/us/app/cfb-gameday-board/id6809035228)

---

## Projects

| Project | What it does | Status | Stack | Code |
| --- | --- | --- | --- | --- |
| [**312Deals**](#312deals-chicago-food--drink-deals) | Chicago food & drink deals: 83,000+ active deals across 12,000+ venues and 149 neighborhoods from 20,000+ tracked sources, ingested by an LLM extraction pipeline. Agent-first surface: REST API · 11-tool MCP server · 18 WebMCP tools · custom GPT · in-app chat | **Live** | Next.js · FastAPI · SQLite on Cloudflare R2 · MCP | [312deals-webmcp](https://github.com/ChristianVerdin/312deals-webmcp) · MIT (WebMCP Challenge entry) |
| [**CFB GameDay Board**](#cfb-gameday-board-college-football-slate-on-web-and-ios) | Every FBS game on one screen: kickoff-hour stadium weather, TV, and rivalry trophies, then live scores and a game sheet with drives, box score, and win probability. Version 1.1 adds a Today's Games widget and universal links. Stdlib Python, vanilla JS, zero dependencies, SwiftUI app for iPhone, iPad, and Mac | **Live · App Store** | Python · JavaScript · SwiftUI · Vercel | [cfb-gameday-board](https://github.com/ChristianVerdin/cfb-gameday-board) · MIT |
| [**Camera Recall**](#camera-recall-natural-language-qa-over-smart-camera-events) | Private Ring app for personal use: natural-language Q&A over my own camera event history. Deliberately metadata-only (no video, clip, or snapshot scopes). Passed Ring Appstore certification on first submission | Certified · personal | FastAPI · Postgres · Railway · 300+ tests | private |
| [**World Cup bracket tracker**](#world-cup-bracket-tracker) | Twice-daily auto-updating tracker for an AgentMail World Cup 2026 bracket. GitHub Actions + AgentMail API, no servers | Complete | Python · GitHub Actions | [worldcup_agentcup-tracker](https://github.com/ChristianVerdin/worldcup_agentcup-tracker) · MIT |

### Where to start reading

- **[312deals-webmcp](https://github.com/ChristianVerdin/312deals-webmcp)**: how a data platform exposes itself to browser-native agents. 17 tools on `document.modelContext`, a "Tonight" planner a person and their agent build together, write-with-consent tips routed to human review. Start at `docs/04-WEBMCP-ARCHITECTURE.md`.
- **[cfb-gameday-board](https://github.com/ChristianVerdin/cfb-gameday-board)**: the cleanest end-to-end example. Zero-dependency Python server and snapshot builder, vanilla JS client, SwiftUI app and WidgetKit widget, scripted App Store Connect release pipeline, self-healing GitHub Action that rebuilds the slate seven times a week. Start at `docs/ARCHITECTURE.md`, then `ios/APP_STORE.md`.

---

## 312Deals: Chicago Food & Drink Deals
**LLM extraction pipeline + agent-first distribution for local commerce**

A production platform aggregating **83,000+ active deals** across **12,000+ venues** and **149 neighborhoods** across Chicagoland, read from **20,000+ tracked sources**. The pipeline runs venue web pages, newsletters, and submissions through LLM extraction with schema validation, content hashing, adaptive scheduling with exponential backoff, and automated 0 to 100 quality scoring, at **under a cent of Claude spend per extracted deal**. Distribution is agent-first: an 18-endpoint REST API, an 11-tool MCP server, 18 in-page WebMCP tools (entered in OpenAI's WebMCP Challenge, Sept 2026), a custom GPT, in-app chat, and a machine-readable `llms.txt` scoring **96/100 on Mintlify's Agent Score**. Programmatic SEO (100+ landing pages) took organic search from an average position of about 24 at launch to page one by June. Since the February 2026 launch: **39,000+ visitors, 9,800+ in the last 28 days**, with no paid traffic. Search Console shows **26,000+ clicks and 2.3M+ impressions at an average position of 7.0**. Traffic figures run through October 27, 2026.

**Live:** [312deals.com](https://312deals.com) · **Public code:** [312deals-webmcp](https://github.com/ChristianVerdin/312deals-webmcp)

<p align="center">
  <img src="./images/312deals/2026-10-28_homepage-desktop.png" width="800" alt="312Deals homepage, October 28, 2026: search with day and neighborhood filters, Active Now, AI prompt chips, and 12,000+ venues, 83,000+ deals, 149 neighborhoods">
</p>
<p align="center">
  <img src="./images/312deals/2026-10-28_map.png" width="400" alt="312Deals map, October 28, 2026: deal pins across Chicago and the suburbs, 33 active now, with the deal list beside it">
  <img src="./images/312deals/2026-10-28_ai-chat.png" width="400" alt="312Deals AI Guide, October 28, 2026: asked what happy hours are in Wicker Park tonight, it answers with four venues, their hours and their prices">
</p>

<details>
<summary><b>More screenshots</b></summary>
<br>
<p align="center"><img src="./images/312deals/2026-10-28_guide-halloween.png" width="800" alt="312Deals Halloween in Chicago 2026 guide: three bar crawls with times, prices and organizer links"></p>
<p align="center"><img src="./images/312deals/plausible_312_since_launch.png" width="800" alt="312Deals Plausible traffic, March 1 to September 17, 2026"></p>
<p align="center"><sub>Plausible, March 1 to September 17, 2026. Older than the figures above.</sub></p>
<p align="center"><img src="./images/312deals/gsc_312_since_launch.png" width="800" alt="312Deals Google Search Console, March 1 to mid-September 2026"></p>
<p align="center"><sub>Google Search Console, March 1 to mid-September 2026, captured September 17. Older than the figures above.</sub></p>
</details>

**What's interesting technically**
- **Agent surface as a first-class product:** the same tool definitions serve the MCP server, the WebMCP registration, and the custom GPT, so a person, a browser agent, and a desktop agent get identical capabilities.
- **Extraction economics:** content hashing and adaptive scheduling turned an LLM-per-page pipeline into something that costs under a cent of Claude spend per extracted deal.
- **Eval before edit:** the extraction prompt has a hand-labeled test set and a held-out set, and changes ship only when they hold on pages the prompt has never seen. That's how a cheaper model got in without a quality loss.
- **Data as a distributed artifact:** SQLite with WAL and FTS5, distributed through Cloudflare R2 with If-Match ETag guards, so the read path never blocks on the write path.
- **Quality loop:** automated 0 to 100 scoring plus a user-driven review queue, and public venue payloads are sanitized through an explicit allow-list.

**Built with:** `Next.js` `TypeScript` `FastAPI` `Python` `SQLite` `Cloudflare R2` `MCP / FastMCP` `WebMCP` `Railway` `Vercel` `Plausible`

---

## CFB GameDay Board: College Football Slate on Web and iOS
**One screen for every FBS Saturday | Live on the web and the App Store for iPhone, iPad, and Mac | Public, MIT**

Venue, kickoff-hour stadium weather, and TV and streaming for every FBS game, then live score, clock, and down and distance once games kick, refreshed every 30 seconds while games run. Tap any live or final game for a game sheet with the scoring summary, box score, leaders, drives, and ESPN win probability. Named rivalries carry their trophy on the card, and a Rivalry filter pulls them together. Built with a deliberately small footprint: a standard-library Python server and snapshot builder, a vanilla JavaScript client with no framework and no build step, and a native SwiftUI app. Built, deployed to the web, and submitted to App Review in a single day. Free, no ads, no account, and Apple's privacy label reads **Data Not Collected**.

**Version 1.1** (on the App Store since October 22, 2026) adds a **Today's Games widget** for the Home Screen and Lock Screen in small, medium, and large sizes, set to all games, the Top 25, or rivalry games. **Universal links** open cfbgameday.app links straight in the app. Long-press the icon for quick actions, including **Rivalry Games**, and six **in-app events** on the App Store cover rivalry Saturdays, Rivalry Week, and the postseason. The same app runs on **iPhone, iPad, and Mac**, where the window resizes.

**Live:** [cfbgameday.app](https://cfbgameday.app) · [App Store](https://apps.apple.com/us/app/cfb-gameday-board/id6809035228) · **Source:** [cfb-gameday-board](https://github.com/ChristianVerdin/cfb-gameday-board)

<p align="center">
  <img src="./images/cfb_gameday/2026-10-28_week9-saturday-desktop.png" width="800" alt="CFB GameDay Board, Week 9 Saturday on desktop: a rivalry desk with five trophy games, including Notre Dame vs Navy and Florida vs Georgia, above the weather and travel desk">
</p>
<p align="center">
  <img src="./images/cfb_gameday/2026-10-21_iphone-widget.png" width="300" alt="CFB GameDay Board's large Today's Games widget on the iPhone Home Screen: Saturday's Top 25 games with weather, kickoff time and network">
</p>

**What's interesting technically**
- **Weather at the kick hour:** Open-Meteo forecast for each venue city, with rain, wind, heat, and altitude flags and an impact read per game.
- **A refresh that heals itself:** a GitHub Action rebuilds the slate seven times a week, each run scheduled hours early because GitHub starts scheduled runs late. A run that loses kickoff forecasts retries and heals itself, and it fails loudly only when it can't.
- **One snapshot, every surface:** the site, the app, and the WidgetKit widget all read the same weekly snapshot and live feed, and unit tests render the widget against a frozen week of real games.
- **Release pipeline as code:** archive, export, validate, upload, attach, and submit through the App Store Connect API from one script, and the same pattern is reusable for the next iOS app.

**Built with:** `Python (stdlib)` `JavaScript` `SwiftUI` `WidgetKit` `WKWebView` `Vercel` `GitHub Actions` `Open-Meteo`

---

## Camera Recall: Natural-Language Q&A over Smart-Camera Events
**Certified on the Amazon Ring Appstore | metadata-only by design**

A private Ring app I built for personal use: it answers questions like "did the dog walker come today, and how long did they stay?" over my own camera event history. The architecture deliberately holds **no live-video, clip, or snapshot scopes**, so it never touches footage. **Passed Ring Appstore certification on the first submission** (Aug 2026) and a second re-validation round (Sept 2026), with a published architecture page, a reviewer demo environment, and a versioned privacy-and-legal questionnaire. Production answers are deterministic today. An LLM agent layer is staged behind re-certification, because certified answers state exactly what the system does.

**Stack:** `FastAPI` `PostgreSQL` `Railway` `300+ tests` `GitHub Actions`. Private repository.

---

## World Cup bracket tracker
**Scheduled agent automation with no servers**

A twice-daily auto-updating tracker for an AgentMail World Cup 2026 bracket: a GitHub Action pulls results through the AgentMail API, recomputes standings, and commits the refreshed page. Small on purpose: a compact, readable example of cron-style agent automation that runs entirely on GitHub infrastructure.

**Source:** [worldcup_agentcup-tracker](https://github.com/ChristianVerdin/worldcup_agentcup-tracker) · `Python` `GitHub Actions` `AgentMail`

**Earlier projects:** [LakeshoreIQ](https://lakeshoreiq.com), Illinois property search and neighborhood data built on public sources.

---

## How I build

- **Production first.** Every flagship project has real users or a real platform review behind it. A demo is the starting line.
- **Measure before optimizing.** I build the tracing and evaluation layer first and let the evidence pick the re-architecture.
- **Safety as architecture.** Metadata-only scopes, least-privilege grants, copy-on-write test branches, and rollback paths are design inputs, not afterthoughts.
- **Agent-first surfaces.** Anything I build for people also gets an MCP or WebMCP surface so other agents can use it.
- **Documentation that survives handoff.** Every repo carries a `CLAUDE.md`/`CONTEXT.md` with verified state, constraints, and gotchas, written for the next engineer and for AI coding agents alike.

---

## Technical skills

**Agentic AI & LLM systems:** multi-agent supervisor/router architectures, parallel fan-out and answer composition, text-to-SQL and retrieval-grounded agents, MCP server development (cloud-deployed and local stdio), WebMCP, tool design for long-running agent operations, LLM document intelligence, prompt engineering and agent steering · Claude · GPT-4/5 · Gemini · Amazon Bedrock · Mosaic AI · LangChain/LangGraph

**LLMOps, observability & evaluation:** MLflow 3 tracing and evaluation, Langfuse, trace ETL and span/session/token analysis, ground-truth success metrics, LLM-as-judge, source-attribution checks, token cost and latency optimization, human-feedback instrumentation

**Machine learning & statistics:** LightGBM, XGBoost, CatBoost, NLP and sentiment classification, time-series forecasting, A/B testing and experimental design, causal inference, survival analysis, model calibration

**Data & platform:** Databricks (Apps, Genie, Mosaic AI agents, Unity Catalog, Lakebase, Delta Lake, serverless jobs, Asset Bundles), Spark/PySpark, PostgreSQL, Supabase, Redis, SQLite/FTS5, streaming and medallion pipelines

**Engineering & release:** Python, TypeScript/JavaScript, SQL, R, Swift/SwiftUI · React, Node/Express, FastAPI, Next.js · AWS (Bedrock, SageMaker, S3, Lambda), Cloudflare (DNS, R2), Vercel, Railway, Docker, GitHub Actions · service-principal and OAuth auth, least-privilege grant design, copy-on-write DB branching, deploy-source verification, feature-flag rollback · App Store and Ring Appstore certification

---

## Let's connect

Always open to collaborating and/or connecting. Chicago-based, remote or relocation welcome.

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/">LinkedIn</a> · <a href="mailto:christiandverdin@gmail.com">christiandverdin@gmail.com</a> · <a href="https://medium.com/@cver123/about">Medium</a>
</p>
