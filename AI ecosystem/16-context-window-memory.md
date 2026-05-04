---
title: Why AI Forgets — The Context Window Problem
phase: AI ecosystem
topic: memory, context window, AI limitations
format: reel
status: draft
scheduled:
tags: [ai, memory, context-window, llm, tokens, ghazini]
related: ["[[17-structured-unstructured-vector-db]]", "[[18-rag-explained]]", "[[11-what-is-a-tool]]", "[[AI Ecosystem Index]]"]
week: 4
day: 1
category: ai
---

# Hook
> Ghazini movie lo oka manishi prathi 30 minutes ki anni forget avutadu. Memory ledu. AI ki kuda same problem undi — context window. Daani fix cheyyakapothe, AI mee conversation history motham forget avutundi.

# Core Idea
_Every AI model has a context window — a fixed limit on how much text it can hold in "active memory" at once. Once the conversation exceeds that limit, the model starts losing earlier parts of the conversation. This is why long ChatGPT sessions feel like talking to someone who forgot what you said an hour ago. Understanding this is the foundation of everything in Week 4._

---

# Details
_Research & facts to write a better script from_

## What Is a Context Window

The context window is the maximum amount of text — measured in tokens — that a model can process at one time. Everything inside the window: the model "sees." Everything outside: gone.

- 1 token ≈ 0.75 English words (roughly 4 characters)
- "Hello, how are you?" = ~5 tokens
- A full novel = ~100,000–150,000 tokens

**Current context windows (2024–2025):**
- GPT-4o: 128,000 tokens (~96,000 words — roughly a full novel)
- Claude 3.5 Sonnet: 200,000 tokens (~150,000 words)
- Gemini 1.5 Pro: 1,000,000 tokens (1M — experimental)
- Llama 3.1 70B: 128,000 tokens

These sound large. But enterprise use cases — customer support histories, legal document review, long codebases — regularly exceed even 200K tokens.

## The Ghazini Analogy

In Ghazini (2008), Sanjay Singhania loses his short-term memory every 15 minutes due to brain damage. He survives by:
- Writing notes on paper
- Tattooing key facts on his body
- Taking Polaroid photos with labels

The model is Ghazini. The context window is his 15-minute memory. When a conversation exceeds the context limit, the model starts "forgetting" the earlier parts — exactly like the movie.

The notes, tattoos, and photos? That's the memory layer. External storage the model can retrieve from when its internal window runs out.

## Why This Matters in Practice

**Symptom 1 — Long ChatGPT conversations degrading:**
You've noticed this. You're 2 hours into a ChatGPT session, and it starts contradicting things it said earlier or forgetting your preferences. The early conversation has fallen out of the context window.

**Symptom 2 — "Lost the thread" in coding sessions:**
Cursor or Claude Code working on a large codebase — eventually the model can no longer "see" the file it edited 45 minutes ago. It starts making changes that break things it fixed earlier.

**Symptom 3 — Summarization degradation:**
Ask an LLM to summarize a 300-page document by pasting it in — if the document exceeds the context window, the model silently ignores the parts that don't fit. The summary is incomplete and the model won't tell you.

## Three Ways to Fix the Memory Problem

### 1. In-Context Memory (Short-term)
Just use a bigger context window. Works for single sessions. Doesn't persist across conversations. Expensive — every token costs money.

### 2. Retrieval (RAG)
Don't stuff everything into context. Instead, retrieve only the relevant pieces when needed. Like Ghazini checking his notes only when relevant, not carrying the full notebook open at all times. Week 4 D3–D5 cover this in depth.

### 3. External Memory (Persistent)
Store information in a database outside the model. The model reads and writes to it across sessions. This is how products like ChatGPT Memory, Mem.ai, and long-running AI agents maintain continuity. Week 5 (Knowledge Graphs) goes deeper on this.

## The Real Cost of Context

Context isn't free. Every token in your context window = compute used = money spent.

- GPT-4o: $5 per 1M input tokens (May 2025)
- Claude Sonnet: $3 per 1M input tokens
- Sending a 200-page PDF in every API call: expensive at scale

For consumer products (ChatGPT free tier), context is also limited by cost. OpenAI can't afford to give every free user a 1M token window. So they compress, summarize, or cut older context.

---

# Breakdown
_Reel script_

1. **Hook** — "Ghazini movie chusara? Aaaa hero prathi 15 minutes ki anni forget avutadu. AI ki kuda same problem undi. Idi context window."

2. **What it is** — "Model oka time lo limit amount of text matrame chudagaladu — adi tokens lo measure avutundi. 1 token ≈ 0.75 words. GPT-4: 128,000 tokens. Claude: 200,000. Sound chestundi large ga? Real use cases lo — legal docs, long code, customer history — idi quickly fill avutundi."

3. **The symptom** — "Meeru ChatGPT tho 2 hour conversation chesaru — later lo adi earlier things forget avutundi, contradict avutundi. That's not a bug. Context window filled up. Earlier conversation fell out."

4. **Ghazini fix** — "Ghazini ento chesadu? Notes raasadu. Tattoos chesadu. Photos teesukunadu. AI ki kuda same solution — external memory. Model context lo anni store cheyyakunda, outside DB lo store cheyyali, need ayyinappudu retrieve cheyyali."

5. **Three solutions** — "Three ways: 1) bigger context window — works, expensive. 2) RAG — retrieve only what's needed, not everything. 3) External persistent memory — across sessions. D2 lo data types, D3 lo RAG explain chestamu."

6. **Bridge** — "Memory problem understand chesamu. Ika next: model ki unstructured data — PDFs, videos, emails — ela feed cheyyali? Vector DB edi — daani next chuddam."

---

# Caption

```
Ghazini movie lo hero prathi 15 minutes ki anni forget avutadu.

AI ki kuda same problem undi. Context window.

Model oka limit of text matrame chudagaladu at once. Window fill avvadam start avvagane — earlier conversation gone.

Adey reason: long ChatGPT sessions lo AI earlier things forget chestundi, contradict avutundi.

Fix: external memory. Notes, tattoos, photos — Ghazini style. AI ki: RAG, vector DBs, persistent memory layers.

This week: idi ela work chestundi, real products chudatamu.

.
.
.
#ai #memory #contextwindow #llm #chatgpt #telugu #telugutech #aiexplained
```

# Visual Notes
- Open with Ghazini clip or still — the iconic "forget" scene
- Split screen: Ghazini's tattoo notes // AI context window visualization (sliding window of text)
- Show context window filling up — like a progress bar reaching 100%
- Long ChatGPT conversation screenshot — early messages grayed out / "forgotten"
- Three solution types: in-context (small box), RAG (retrieval arrow), external DB (cylinder icon)
- Tone: relatable, visual. Movie reference makes it instantly understood.

# Sources / Links
- OpenAI GPT-4o context window — platform.openai.com documentation
- Claude context window — Anthropic documentation
- Gemini 1.5 Pro 1M context — Google DeepMind blog
- Token pricing — OpenAI and Anthropic pricing pages (May 2025)
- Ghazini (2008) — Aamir Khan film (context window analogy, not official)

# Related Notes
- [[17-structured-unstructured-vector-db]]
- [[18-rag-explained]]
- [[11-what-is-a-tool]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

Ghazini movie in that movie that person forgets everything in every 30 mins like model has the context, so we need to add a memory layer so we can store data and refer to it
