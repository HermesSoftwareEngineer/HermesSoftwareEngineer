# Hermes Barbosa

**Backend & AI engineer — Python, Flask, LangGraph.** Fortaleza, Brazil.

I lead the rental operations of a real estate agency and I build the software that runs it. Writing the requirements and then shipping the system is the core of how I work: everything below is used daily by real teams, with real contracts and real money behind it.

Currently focused on AI agents in production — LangGraph orchestration, MCP servers, and the unglamorous parts around them: queues, cold starts, multi-tenancy and cost per request.

Open to remote positions (mid-level backend / AI engineering).

---

## Featured work

**[Precifica](https://stylusprecifica.vercel.app/)** — AI-assisted property valuation SaaS *(client work, private repo)*
Generates PTAM technical appraisal reports compliant with ABNT NBR 14653-2 and COFECI Resolution 1.066/2007. A LangGraph pipeline handles comparable-sample discovery (neighborhood inference → scraping → filtering → expansion → persistence) as async Celery jobs with frontend polling; statistical treatment includes Chauvenet outlier removal, Ross-Heidecke depreciation and precision grading. Every report is reviewed and signed by a licensed appraiser — the AI drafts, a human is accountable.
`Flask` `LangGraph` `Celery` `Redis` `Supabase` `React` `Cloud Run`

**ObraLog** — multi-tenant SaaS for construction site diaries *(private)*
Field teams report through a Telegram agent; the system turns messages into structured daily logs (RDO). Built around a persistent job queue with a poll-worker thread so webhook latency stays low, plus lazy imports and always-allocated CPU to survive Cloud Run cold starts.
`FastAPI` `LangGraph` `Gemini` `Supabase` `Cloud Run`

**StylusBot** — internal WhatsApp operations platform *(private)*
Lets staff query CRM leads and dispatch approved WhatsApp templates in bulk, on top of a 178-endpoint real estate CRM API. JWT auth with a four-role permission matrix, in-platform Meta template management, and opt-out compliance enforced through webhook keyword detection.
`Flask` `Meta WhatsApp Cloud API` `Supabase` `React` `TypeScript`

**OzzyFlow** — multi-tenant clinic management with a WhatsApp assistant *(private)*
Designed around a parity principle: anything the AI can do over WhatsApp is fully available as manual CRUD in the web app. Clinical records, structured anamnesis and prescriptions — with mandatory human confirmation before any prescription PDF is generated.
`Flask` `Supabase` `React` `TypeScript` `Evolution API`

**Mercúrio / Projeto Olimpo** — self-hosted personal AI assistant *([Assistente-Mercurio](https://github.com/HermesSoftwareEngineer/Assistente-Mercurio))*
A WhatsApp agent with a proactive LangGraph heartbeat and an Obsidian vault as long-term memory through MCP, using a two-pass context loading pattern to keep prompts small. Runs on a self-hosted Docker stack (Evolution API, Nginx, Redis) that hosts several bots side by side.
`Python` `LangGraph` `MCP` `Docker` `Nginx`

### Open source

| Repo | What it is |
|---|---|
| [Organizze-MCP-Server](https://github.com/HermesSoftwareEngineer/Organizze-MCP-Server) | MCP server with full coverage of the Organizze personal finance API (28 tools) |
| [Trello-MCP-Server](https://github.com/HermesSoftwareEngineer/Trello-MCP-Server) | MCP server for Trello boards, cards and checklists |
| [Asafe-Finance](https://github.com/HermesSoftwareEngineer/Asafe-Finance) | Cash-flow system for a volunteer music ministry — FastAPI + HTMX + Jinja2 |
| [G8-ai](https://github.com/HermesSoftwareEngineer/G8-ai) | WhatsApp AI attendant for a barbershop, with scheduling-platform integration |

---

## Stack

| | |
|---|---|
| **Languages** | Python, TypeScript, JavaScript, SQL |
| **Backend** | Flask, FastAPI, Node.js, REST APIs, JWT |
| **AI** | LangGraph, LangChain, MCP servers, Gemini, DeepSeek, function calling |
| **Data** | PostgreSQL, Supabase, Redis, SQLite |
| **Frontend** | React, Vite, TypeScript, Tailwind CSS |
| **Infra** | Docker, Google Cloud Run, Celery, Nginx, GitHub Actions, Vercel |

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

**[LinkedIn](https://www.linkedin.com/in/hermes-barbosa-78840118a)** · hermesbarbosa9@gmail.com
