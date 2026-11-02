# TicketDraft

Support inbox copilot for a fictional notes SaaS (**NoteFlow**).

Paste an incoming support email → get **intent / priority / sentiment**, a short summary, and a **draft reply grounded in similar past tickets**. A human reviews and accepts the draft before anything is treated as a good answer.

## Why this exists

Small teams answer the same billing, access, and how-to questions every week. Old replies already exist, but finding them is slower than rewriting from scratch. TicketDraft turns closed tickets into searchable context for the next draft.

## Current status

Early scaffold:

- Seed data: [`fixtures/tickets.json`](fixtures/tickets.json) (20 closed NoteFlow tickets)
- Env template: [`.env.example`](.env.example) (Anthropic / Claude)

App code (CLI triage → FastAPI → UI → RAG → evals → agent → MCP → deploy) will land step by step.

## Stack (planned)

| Layer | Choice |
| --- | --- |
| LLM | Anthropic Claude API |
| API | Python, FastAPI, Pydantic |
| Data | PostgreSQL + pgvector |
| UI | Next.js |
| Ops | Docker Compose, then a public deploy |

## Setup

```bash
cp .env.example .env
# put your Anthropic API key in .env
```

Further run instructions will appear here as each stage ships.

## License

MIT
