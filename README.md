# Relay CRM

Relay is an AI-native CRM where the inbox is the source of truth. Built as an interactive prototype, this application ingests mock email threads, extracts structured state (accounts, contacts, opportunities, and sentiment), scores every deal for health, drafts follow-ups, and pushes cross-functional context.

## Stack
- Next.js 15 (App Router, Server Components)
- SQLite (`better-sqlite3`) & Drizzle ORM
- Tailwind CSS v4 & shadcn/ui
- Generative AI via `@anthropic-ai/sdk`

## Running the Mock Prototype

Start the development server:

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser.

- **Seeded Data:** The first time it runs, `relay.db` is populated with mock accounts and deals.
- **Mock Mode:** If you do not have an `ANTHROPIC_API_KEY` defined in `.env.local`, the application runs in a deterministic mock mode—generating mock follow-ups and offline fallback chatbot modes so the demo remains fully runnable.

## Workflows Included
1. **Pipeline & Scoring:** Automatic intent and deal health calculation based on thread activity pacing, stakeholder mapping, and semantic extraction. Native drag and drop kanban updates.
2. **AI Action Queue:** Read-only drafting for follow-ups that sound like they came from the human assigned.
3. **Ask Relay Chatbot:** Drill into single accounts and threads with a slide-out assistant answering questions on current deal blockers or summaries.
4. **Handoffs & Settings:** Extensible workspace pack supporting specific terms, target ICPs, and organizational vernacular.
