# Hermes Barbosa

**Full-stack developer — Python, JavaScript, Flask, React, Node, LangGraph.** Fortaleza, Brazil.

I build software with real users behind it. Most of what I ship runs inside a real estate company where I also lead the rental operations — internal systems, AI tools, dashboards and automations that replaced manual processes for the whole team. Writing the requirements and then shipping the system is the core of how I work.

Beyond the code, I care about the business model behind it: what actually produces results for the people using the software.

Currently focused on AI agents in production — LangGraph orchestration, MCP servers, and the unglamorous parts around them: queues, cold starts, multi-tenancy and cost per request.

🌐 **Portfolio: [hermesdev.vercel.app](https://hermesdev.vercel.app)** · Open to remote positions (mid-level backend / AI engineering).

---

## Featured work

**ObraLog** — B2B SaaS for construction site diaries (RDO)
Field supervisors talk to *Tião*, an AI agent, over WhatsApp or Telegram to log what happened on site. The system compiles those messages into structured daily PDF reports that engineers and managers read through a web dashboard. Built around a persistent job queue with a poll worker to keep webhook latency low, plus lazy imports and always-allocated CPU to survive Cloud Run cold starts.
`Python` `Flask` `LangGraph` `Gemini` `PostgreSQL` `Supabase` `React` `WhatsApp API` `Telegram`

**[Precifica](https://stylusprecifica.vercel.app/)** — AI-assisted property valuation SaaS
Two modes: quick sample-average appraisals and full PTAM technical reports for autonomous brokers, CNAI appraisers and agencies. The AI searches comparable listings on real estate portals, applies the legal homogenization methodology (ABNT NBR 14653-2), removes outliers by Chauvenet's criterion and generates professional PDF reports — while a licensed broker reviews and signs. Sample search runs as async Celery jobs driven by a LangGraph pipeline. Already validated in production with agencies in Fortaleza, CE.
`Python` `Flask` `LangGraph` `Gemini` `Celery` `Redis` `BeautifulSoup` `Supabase` `React`

**Dashboard de Indicadores** — internal productivity platform, used daily company-wide
Centralizes what used to be scattered across tools: Trello workflows, contract data from the Imoview CRM, service calls, collections, inspections and SLA. Adds AI-generated productivity scoring and meeting-ready reports, with period filters and historical evolution. It changed how each sector spots bottlenecks, redistributes work and reports results.
`React` `Vite` `TailwindCSS` `Chart.js` `Recharts` `Supabase` `Trello API` `Imoview API` `Gemini` `LangSmith`

**Mercúrio** — self-hosted personal AI assistant on WhatsApp
Manages communications and proactively runs recurring tasks, with persistent memory kept in an Obsidian vault through MCP and a two-pass context loading pattern that keeps prompts small. Part of *Projeto Olimpo*, running 24/7 on my own infrastructure.
`Python` `Flask` `LangGraph` `DeepSeek` `Evolution API` `Docker` `Redis` `Nginx`

**Asafe Finance** — financial control platform for a volunteer music ministry
Replaces loose spreadsheets with a single panel: income and expenses with hierarchical categories, recurring and installment entries, OFX bank statement import with automatic reconciliation by value and date, and cash-flow / budget-vs-actual / cost-center reports exported to PDF and Excel — ready for leadership accountability meetings.
`Python` `FastAPI` `SQLAlchemy` `Alembic` `PostgreSQL` `Supabase` `ReportLab` `openpyxl` `React`

Also in progress: **StylusBot** (WhatsApp operations platform on the Meta Cloud API, with role-based access and opt-out compliance), **OzzyFlow** (multi-tenant clinic management with a WhatsApp assistant, where every AI action has a manual CRUD equivalent) and **Ekklesia** (event registration system for religious events).

### Open source

| Repo | What it is |
|---|---|
| [Organizze-MCP-Server](https://github.com/HermesSoftwareEngineer/Organizze-MCP-Server) | MCP server with full coverage of the Organizze personal finance API (28 tools) |
| [Trello-MCP-Server](https://github.com/HermesSoftwareEngineer/Trello-MCP-Server) | MCP server for Trello boards, cards and checklists |
| [Asafe-Finance](https://github.com/HermesSoftwareEngineer/Asafe-Finance) | Backend of the ministry finance platform — FastAPI + SQLAlchemy |
| [G8-ai](https://github.com/HermesSoftwareEngineer/G8-ai) | WhatsApp AI attendant for a barbershop, with scheduling-platform integration |

---

## Stack

| | |
|---|---|
| **Languages** | Python, TypeScript, JavaScript, SQL |
| **Backend** | Flask, FastAPI, Django, Node.js, Express, Sequelize, REST APIs, JWT |
| **AI** | LangGraph, LangChain, MCP servers, Gemini, DeepSeek, LangSmith |
| **Data** | PostgreSQL, Supabase, Redis, SQLite, SQLAlchemy |
| **Frontend** | React, Vite, TypeScript, Tailwind CSS |
| **Infra** | Docker, Google Cloud Run, Celery, Nginx, Git, Vercel |

---

## A few things I've learned the hard way

- On serverless, **cold start is an architecture decision**: heavy import trees plus request-based CPU billing turned a startup into minutes, not seconds. Lazy imports and always-allocated CPU fixed it.
- **Never run migrations on connect.** DDL on every DB connection cost 26–36s of startup latency until it went behind a flag.
- **Model routing beats model loyalty.** Assigning different models to planning, extraction and generation phases keeps agent costs sane without hurting output quality.
- **Multi-tenancy from day one**, even with a single tenant. Retrofitting it is a rewrite.
- Where the output carries legal or clinical weight, **the AI drafts and a licensed human signs** — a design constraint, not a disclaimer.

---

## Currently

Computer Science student, working through a structured mid-level roadmap — SQL & Postgres, automated testing, Docker, CI/CD, AWS, system design — toward a capstone Flask API serving a LangGraph agent, dockerized, tested and deployed, with the architectural decisions documented.

Portuguese (native) · English (conversational)

## Contact

[Portfolio](https://hermesdev.vercel.app) · [LinkedIn](https://www.linkedin.com/in/hermes-barbosa-78840118a) · [YouTube](https://www.youtube.com/@respostaexata7724) · [Instagram](https://instagram.com/hermess.dev) · dev.hbp@gmail.com
