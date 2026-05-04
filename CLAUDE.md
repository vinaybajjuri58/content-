# Instagram Content Vault — Claude Instructions

This is an Obsidian vault for planning and scripting Telugu Instagram content.

## Weekly Content Schedule

- **Day 1-4:** AI-related content — concepts, tools, ecosystem, agents, etc.
- **Day 5:** Money / Business topic — personal finance, business models, moats, investing concepts, etc.
- **Day 6:** Meme reel — for engagement, humor, relatable content
- **Day 7:** Broaden your thinking — one of three formats: (1) Business concept or framework, (2) Influencer / person to follow, (3) Book recommendation

## Content File Format

Each post lives in its own `.md` file with this frontmatter:
```
title, phase, topic, format, status, scheduled, tags, related, week, day, category
```

Sections in every file:
1. Hook
2. Core Idea
3. Details (facts, numbers, stats — always rich)
4. Breakdown
5. Caption
6. Visual Notes
7. Sources
8. Related Notes
9. Raw Notes (preserve user's Telugu script here exactly as written)

Template at: `Templates/Post Template.md`

## Folder Structure

- `AI ecosystem/` — AI series posts
- `Personal Finance/` — Day 5 finance/business posts
- `Memes/` — Day 6 meme reels
- `Recommendations/` — Day 7 content picks
- `Weeks/` — Weekly overview notes

## Writing Style

- Write so the user can directly use it as a Telugu reel script
- Always include a rich Details section with real facts, numbers, and stats
- No emojis unless asked
- Use `[[wikilinks]]` to connect related notes for Obsidian graph view

## Naming Convention

- AI posts: `00-intro-reel.md`, `01-topic-name.md`, etc.
- Other posts: `W{week}-D{day}-topic-name.md` (e.g. `W1-D5-personal-finance-101.md`)

## Completed Weeks

### Week 1
- Day 1: `AI ecosystem/00-intro-reel.md` — Intro reel
- Day 2: `AI ecosystem/01-five-layer-ai-stack.md` — Jensen Huang's 5-layer AI stack
- Day 3: `AI ecosystem/02-model-vs-agent.md` — Model vs Agent
- Day 4: `AI ecosystem/03-types-of-ai-models.md` — Types of AI models
- Day 5: `AI ecosystem/04-open-source-vs-closed-source.md` — Open Source vs Closed Source models + self-hosted business opportunity
- Day 6: `Memes/W1-D6-ai-business-ideas-meme.md` — AI Business Ideas meme
- Day 7: `Recommendations/W1-D7-bbwv-coconut-value-chain.md` — BBWV Coconut Value Chain

### Week 2
- Day 1: `AI ecosystem/04-why-prompting.md` — Why prompting matters (Chitti Robo hook)
- Day 2: `AI ecosystem/05-types-of-prompting.md` — Zero-shot, few-shot, chain-of-thought, role prompting (empty shell)
- Day 3: `AI ecosystem/06-ai-skills-hype-is-just-prompting.md` — "Life-changing AI skill" hype debunked (empty shell)
- Day 4: `AI ecosystem/07-ai-sycophancy-bias.md` — AI sycophancy and bias (empty shell)
- Day 5: `AI ecosystem/09-prompt-injection.md` — Prompt Injection (direct + indirect, real attacks)
- Day 6: *(Meme — TBD)*
- Day 7: `Recommendations/W2-D7-ai-value-chain-extension.md` — Business concept: AI value chain extension (Apollo, Claude Code, GitHub Copilot, Zoom, Gong)
- Unscheduled: `AI ecosystem/08-llm-poisoning.md` — LLM Poisoning (preserved for future)
- Unscheduled: `Personal Finance/W2-D5-compounding.md` — Compounding (preserved for finance week)

### Week 3
- Day 1: `AI ecosystem/10-knowledge-cutoff.md` — Knowledge cutoff, why AI needs tools
- Day 2: `AI ecosystem/11-what-is-a-tool.md` — What is a tool, Interface vs API, MCP
- Day 3: `AI ecosystem/12-cursor-tool-demo.md` — Demo: Cursor file + terminal tool calls
- Day 4: `AI ecosystem/13-customer-support-tool-demo.md` — Demo: customer support data fetching, human-in-the-loop
- Day 5: `AI ecosystem/14-remotion-skill-demo.md` — Demo: Remotion skill (tool chain → motion graphics)
- Day 6: `AI ecosystem/15-tools-gone-wrong.md` — Real AI failures (Air Canada, Chevrolet, UK discount, Supabase MCP)
- Day 7: `Recommendations/W3-D7-marc-andreessen.md` — Marc Andreessen + Truth Terminal $50K story

### Week 4
- Day 1: `AI ecosystem/16-context-window-memory.md` — Context window problem (Ghazini analogy)
- Day 2: `AI ecosystem/17-structured-unstructured-vector-db.md` — Structured vs Unstructured + Vector DB + Similarity Search (combined)
- Day 3: `AI ecosystem/18-rag-explained.md` — RAG: open book exam for AI
- Day 4: `AI ecosystem/19-chat-with-website-sitegpt.md` — Demo: Chat with Website using SiteGPT
- Day 5: `AI ecosystem/20-chat-with-video-notebooklm.md` — Demo: Chat with Video using NotebookLM
- Day 6: `Memes/W4-D6-memory-meme.md` — Memory meme (TBD)
- Day 7: `Recommendations/W4-D7-naval-ravikant.md` — Naval Ravikant (influencer): wealth, leverage, specific knowledge

### Week 5
- Day 1: `AI ecosystem/21-knowledge-graph-intro.md` — Knowledge Graph intro (childhood riddle analogy, nodes + edges, Google/Facebook/LinkedIn examples)
- Day 2: `AI ecosystem/22-knowledge-graph-legal-docs.md` — Legal Docs use case (Harvey AI $3B, Allen & Overy 3,500 lawyers, LexisNexis 9B docs)
- Day 3: `AI ecosystem/23-knowledge-graph-ecommerce.md` — E-commerce recommendations (Amazon 35% revenue, Flipkart, Meesho, Myntra)
- Day 4: `AI ecosystem/24-knowledge-graph-personality-analysis.md` — Concall + movie script + management analysis (Gong $7.25B, AlphaSense $4B, Microsoft Viva)
- Day 5: `AI ecosystem/25-memory-dark-side.md` — Dark side: memory poisoning (accidental, deliberate RAG poisoning, graph compounding, Samsung leak, Microsoft Recall)
- Day 6: `Memes/W5-D6-knowledge-graph-meme.md` — Meme placeholder
- Day 7: `Recommendations/W5-D7-alignment-problem.md` — "The Alignment Problem" by Brian Christian (RESEARCH READY — user hasn't read it, confirm before filming)

### Schedule Note
- Finance / Money posts (compounding, moats, investing) have not started — will be introduced as a proper dedicated week later
- All Week 3 and Week 4 content is reel format (video, not carousel)
- Week 2 D2–D4 files are empty shells still needing content: 05-types-of-prompting.md, 06-ai-skills-hype-is-just-prompting.md, 07-ai-sycophancy-bias.md
