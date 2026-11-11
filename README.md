# Christian Verdin

**Data scientist and AI engineer: statistics, data pipelines and LLM systems, measured before they ship.**

I build data products end to end and test them the way I'd want them tested: held-out evaluations for LLM changes, proper scoring rules and calibration checks for models, natural experiments where the data allows one, and null results reported next to the wins. Everything below was built outside work hours, deployed, and kept running, including an iOS app that went through Apple's App Store review.


[![LinkedIn](https://img.shields.io/badge/LinkedIn-christian--verdin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/christian-verdin/)
[![Live](https://img.shields.io/badge/Live-312deals.com-0F6E6E?style=for-the-badge&logo=google-chrome&logoColor=white)](https://312deals.com)
[![App Store](https://img.shields.io/badge/App_Store-CFB_GameDay_Board-0D96F6?style=for-the-badge&logo=apple&logoColor=white)](https://apps.apple.com/us/app/cfb-gameday-board/id6809035228)

---

## Projects

| Project | What it is | Status | Link |
| --- | --- | --- | --- |
| [**312Deals**](#312deals) | Chicago food and drink deals, kept current by an LLM pipeline and searchable by people and AI agents | **Live** | [312deals.com](https://312deals.com) |
| [**NFL advanced metrics**](#nfl-advanced-metrics) | 32 R charts of the 2026 season and 2018-2025 patterns, each titled with its finding, rebuilt weekly with one command | **Public** | [nfl-advanced-metrics](https://github.com/ChristianVerdin/nfl-advanced-metrics) |
| [**CFB GameDay Board**](#cfb-gameday-board) | Every college football game on one screen, on the web and in an iPhone, iPad and Mac app | **Live · App Store** | [cfbgameday.app](https://cfbgameday.app) · [code](https://github.com/ChristianVerdin/cfb-gameday-board) |
| [**Page Grabber**](#page-grabber) | Captures any web page as clean Markdown into a searchable archive an AI assistant can read | Daily use | private |
| [**World Cup bracket tracker**](#world-cup-bracket-tracker) | A small tracker that updated itself twice a day through the 2026 World Cup | Complete | [worldcup_agentcup-tracker](https://github.com/ChristianVerdin/worldcup_agentcup-tracker) |
| [**College basketball analytics**](#college-basketball-analytics) | 13 short studies, each answering one question about men's college basketball with a number and its uncertainty | **Public** | [ncaab-analytics-case-studies](https://github.com/ChristianVerdin/ncaab-analytics-case-studies) |

<p align="center">
  <a href="#312deals"><img src="./images/312deals/2026-11-05_homepage-desktop.png" width="200" alt="312Deals homepage"></a>
  <a href="#nfl-advanced-metrics"><img src="./images/nfl/caleb-williams-epa-rank.png" width="200" alt="NFL: Caleb Williams went from 30th to 14th to 6th in EPA per dropback"></a>
  <a href="#cfb-gameday-board"><img src="./images/cfb_gameday/2026-10-28_game-sheet-desktop.png" width="200" alt="CFB GameDay Board game sheet"></a>
  <a href="#college-basketball-analytics"><img src="./images/ncaab/home-court-by-season.png" width="200" alt="College basketball: home-court advantage by season, 2001-02 to 2025-26"></a>
</p>

**In progress:** a pre-registered entry for the NFL Big Data Bowl 2027 on Kaggle. Results follow the January 2027 deadline.

### Where to start reading

- **[nfl-advanced-metrics](https://github.com/ChristianVerdin/nfl-advanced-metrics)**: the quickest read. Every chart's title states its finding, so the first screen of the README is the result.
- **[cfb-gameday-board](https://github.com/ChristianVerdin/cfb-gameday-board)**: the cleanest end-to-end example, a website, an iOS app and a widget from one small codebase. Start with the [five-minute case study](https://github.com/ChristianVerdin/cfb-gameday-board/blob/main/docs/CASE_STUDY.md).
- **[312deals-webmcp](https://github.com/ChristianVerdin/312deals-webmcp)**: how a live data site exposes itself to browser-based AI agents.
- **[ncaab-analytics-case-studies](https://github.com/ChristianVerdin/ncaab-analytics-case-studies)**: statistics first. Its README lists which studies to read for data science, analytics, AI engineering or management roles.

---

## 312Deals
**Chicago food and drink deals · live**

A free site that collects Chicago food and drink deals, 75,000+ across 12,000+ venues, from venue websites, newsletters and submissions. An LLM pipeline reads each source and turns it into structured deals, which people can search by neighborhood, day and time, or ask the AI Guide about. AI agents can use the same search through MCP and WebMCP tools.

<p align="center">
  <img src="./images/312deals/2026-11-05_homepage-desktop.png" width="800" alt="312Deals homepage, November 5, 2026: search with day and neighborhood filters, Active Now, AI prompt chips, and 12,000+ venues, 75,000+ deals, 149 neighborhoods">
</p>

Since the February 2026 launch: **45,000+ visitors** and **30,000+ Google clicks from 2.5M+ impressions**, as of November 2026.

<p align="center">
  <img src="./images/312deals/plausible-since-launch-2026-11-10.png" width="49%" alt="Plausible, all time: daily visitors climbing from February to November 2026, 45,000+ visitors in total">
  <img src="./images/312deals/search-console-since-launch-2026-11-10.png" width="49%" alt="Google Search Console since launch: 30,000+ clicks from 2.5M+ impressions">
</p>

<details>
<summary><b>More screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/312deals/2026-10-28_ai-chat.png" width="700" alt="312Deals AI Guide: asked what happy hours are in Wicker Park tonight, it answers with four venues, their hours and their prices">
</p>
<p align="center">
  <img src="./images/312deals/2026-11-10_guide-black-friday.png" width="49%" alt="312Deals guide to Black Friday in Chicago 2026: Thanksgiving dinners, turkey to go and deals near the malls, built from the deal data">
  <img src="./images/312deals/2026-11-10_neighborhoods.jpg" width="49%" alt="312Deals neighborhoods page: Chicago neighborhoods with photos, deal counts and how many deals are active now">
</p>
<p align="center">
  <img src="./images/312deals/plausible-last-30-days-2026-11-10.png" width="47%" alt="Plausible, last 30 days to November 10, 2026: 12k unique visitors, up 10%">
  <img src="./images/312deals/search-console-last-28-days-2026-11-10.png" width="51%" alt="Google Search Console, last 28 days to November 8, 2026: 7,500+ clicks from 420,000+ impressions">
</p>
</details>

**Live:** [312deals.com](https://312deals.com) · **Public code:** [312deals-webmcp](https://github.com/ChristianVerdin/312deals-webmcp) · `Next.js` `FastAPI` `Python` `SQLite` `MCP` `WebMCP`

---

## NFL advanced metrics
**32 charts · open nflverse data · Public, MIT**

Charts meant to be read in five seconds: the title states the finding, team logos and player headshots replace legends, and every title is computed from the data, so a weekly rerun can't leave a stale headline. Caleb Williams went from 30th to 14th to 6th in EPA per dropback over three seasons. Touchdown luck doesn't carry over from the first half of a season to the second (r = 0.04), but touchdown opportunity does (r = 0.44). The new kickoff rule gave every offense about five yards of field position.

<p align="center">
  <img src="./images/nfl/caleb-williams-epa-rank.png" width="800" alt="Caleb Williams went from 30th to 14th to 6th in EPA per dropback over three seasons">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/P2_touchdown_regression.png" width="53%" alt="Touchdown luck doesn't carry over from the first half of a season to the second, but touchdown opportunity does: running backs, receivers and tight ends, 2018-2025">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/P3_early_weeks_vs_rest.png" width="45%" alt="Three weeks of football explain only 18% of how a team plays the rest of the season: net EPA per play, Weeks 1-3 vs Weeks 4-18, 2018-2025">
</p>

<details>
<summary><b>More charts</b></summary>
<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/P1_kickoff_rule_field_position.png" width="54%" alt="Average starting field position after a kickoff, 2018-2026: drives start at the 30 under the new kickoff rule, up from the 25">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/T4_rank_bump_chart.png" width="44%" alt="Net EPA per play rank in three stretches of the 2026 season for the biggest risers and fallers, with team logos">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/01_team_epa_landscape.png" width="57%" alt="Every team's 2026 EPA per play on offense and allowed on defense, plotted with team logos">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/nfl-advanced-metrics/main/out/08_qb_air_yards_ridges.png" width="41%" alt="Air yards on every attempt for the 16 busiest quarterbacks of 2026, as ridgelines with headshots">
</p>
<p align="center"><sub>All 32 charts are in <a href="https://github.com/ChristianVerdin/nfl-advanced-metrics/tree/main/out">out/</a>.</sub></p>
</details>

**Read:** [nfl-advanced-metrics](https://github.com/ChristianVerdin/nfl-advanced-metrics) · `R` `ggplot2` `nflverse` `gt`

---

## CFB GameDay Board
**Web and App Store · Public, MIT**

Every FBS game of the week on one screen: venue, kickoff-hour weather and TV, then live scores and a game sheet with the box score, drives and win probability. It runs on the web and as a free app for iPhone, iPad and Mac, with a Home Screen widget. No ads, no account, and no data collected.

<p align="center">
  <img src="./images/cfb_gameday/2026-10-28_game-sheet-desktop.png" width="700" alt="CFB GameDay Board game sheet on desktop: Delaware 35, Western Kentucky 21, final, with the line score by quarter and every scoring play">
</p>
<p align="center">
  <img src="./images/cfb_gameday/2026-10-21_iphone-widget.png" width="300" alt="CFB GameDay Board's large Today's Games widget on the iPhone Home Screen: Saturday's Top 25 games with weather, kickoff time and network">
  <img src="./images/cfb_gameday/game_sheet_drives.png" width="300" alt="CFB GameDay Board game sheet on a phone: North Texas 45, Tulsa 44 in overtime, with the win probability chart and the drive list">
</p>

<details>
<summary><b>More screenshots</b></summary>
<br>
<p align="center">
  <img src="./images/cfb_gameday/app-store_game-sheet-iphone.png" width="28%" alt="App Store screenshot, iPhone: every score, drive and stat, shown on the game sheet's scoring tab for Southern Miss 34, Troy 55">
  <img src="./images/cfb_gameday/app-store_game-sheet-ipad.png" width="46%" alt="App Store screenshot, iPad: the same game sheet open over the board">
</p>
</details>

**Live:** [cfbgameday.app](https://cfbgameday.app) · [App Store](https://apps.apple.com/us/app/cfb-gameday-board/id6809035228) · **Source:** [cfb-gameday-board](https://github.com/ChristianVerdin/cfb-gameday-board) · **Read:** [five-minute case study](https://github.com/ChristianVerdin/cfb-gameday-board/blob/main/docs/CASE_STUDY.md) · `Python` `JavaScript` `SwiftUI` `WidgetKit`

---

## Page Grabber
**A tool I use every day · private repository**

Many pages build their content in the browser, so a plain download gets nothing. Page Grabber captures the full text from inside the browser after the page renders and saves it as clean Markdown in a searchable archive. An MCP server lets Claude search and read that archive.

`JavaScript` `Python` `SQLite` `MCP`

---

## World Cup bracket tracker
**Complete · Public, MIT**

A small tracker for an AgentMail World Cup 2026 bracket. Twice a day through the tournament, a GitHub Action pulled results, recomputed standings and published the page, with no servers.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./images/worldcup/rank-history-dark.svg">
    <img src="./images/worldcup/rank-history-light.svg" width="700" alt="Bracket leaderboard rank over the tournament: peaked at #1, fell to #46 after Portugal was eliminated, finished #35 of 62">
  </picture>
</p>

**Source:** [worldcup_agentcup-tracker](https://github.com/ChristianVerdin/worldcup_agentcup-tracker) · `Python` `GitHub Actions`

---

## College basketball analytics
**13 case studies · public data · Public, MIT**

Each study asks one question about men's college basketball, answers it with a number and its uncertainty, and shows the checks behind it. The questions range from how much home court is worth, and whether it's shrinking, to whether winning close games is a skill. Most studies run on public ESPN data and can be rerun; the few that use licensed ratings publish only summary results.

<p align="center">
  <img src="./images/ncaab/home-court-by-season.png" width="800" alt="Home-court advantage fell from 4.3 to 3.2 points over 25 seasons of men's college basketball, with 95% bootstrap intervals; 2020-21, when most arenas were empty, sits lowest">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/ncaab-analytics-case-studies/main/studies/08-luck-and-regression-to-the-mean/figures/01_regression_to_the_mean.png" width="49%" alt="The luckiest tenth of teams won 2.0 games more than expected in the first half of a season, then 0.1 more in the second half">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/ncaab-analytics-case-studies/main/studies/12-ask-the-season/figures/01_accuracy.png" width="49%" alt="Claude Haiku 4.5 turning questions about the season into SQL: column notes and rules lifted held-out accuracy from 47% to 95%, with 95% Wilson intervals">
</p>

<details>
<summary><b>More charts</b></summary>
<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/ncaab-analytics-case-studies/main/studies/06-forty-one-years-of-march/figures/03_champion_seeds.png" width="58%" alt="Champions and Final Four teams by seed, 1985-2026: 27 of 41 champions were 1 seeds, and none was seeded worse than 8">
  <img src="https://raw.githubusercontent.com/ChristianVerdin/ncaab-analytics-case-studies/main/studies/07-team-archetypes/figures/04_style_map.png" width="40%" alt="Team styles, 2007-08 to 2025-26: four archetypes that are regions of one continuous cloud, not separate clusters">
</p>
</details>

**Read:** [ncaab-analytics-case-studies](https://github.com/ChristianVerdin/ncaab-analytics-case-studies) · `R` `Python` `hoopR`

**Earlier projects:** [LakeshoreIQ](https://lakeshoreiq.com), Illinois property search and neighborhood data built on public sources.

---

## How I build

- **Production first.** Every flagship project has real users or a real platform review behind it. A demo is the starting line.
- **Measure before optimizing.** I build the tracing and evaluation layer first and let the evidence pick the re-architecture.
- **Safety as architecture.** Least-privilege access, publish checks and rollback paths are design inputs, not afterthoughts.
- **Agent-first surfaces.** Anything I build for people also gets an MCP or WebMCP surface so other agents can use it.
- **Documentation that survives handoff.** Each project's README says how to run it, where the data comes from and where the results are weak, written for the next engineer and for AI coding agents alike.

---

## Technical skills

**Statistics:** calibration and proper scoring rules (Brier, log loss, reliability diagrams), walk-forward and held-out evaluation, bootstrap intervals, McNemar, permutation and Holm-corrected tests, natural experiments and fixed effects, ridge regression, Monte Carlo simulation, pre-registration

**Machine learning:** LightGBM, XGBoost, isotonic calibration, clustering with stability checks, NLP and LLM extraction

**LLM systems:** Claude API, prompt caching, eval harnesses with labeled and held-out sets, cost metering from reported usage, MCP and WebMCP servers, text-to-SQL, multi-agent work with guardrails

**Data & engineering:** Python, R, SQL, TypeScript/JavaScript, Swift/SwiftUI · SQLite/FTS5, PostgreSQL · FastAPI, Next.js · Cloudflare (Workers, R2, D1), Vercel, Railway, GitHub Actions, Playwright · App Store release and review

**Data visualization:** R (ggplot2, gt, ggtext), computed chart titles, logo and headshot pipelines, Playwright screenshots

---

## Let's connect

Always open to collaborating and/or connecting. Chicago-based, remote or relocation welcome.

<p align="center">
  <a href="https://www.linkedin.com/in/christian-verdin/">LinkedIn</a>
</p>
