---
title: Knowledge Graph Use Case — Concall, Movie Script, and Personality Analysis
phase: AI ecosystem
topic: knowledge graph, personality analysis, concall, movie script, character analysis
format: reel
status: draft
scheduled:
tags: [ai, knowledge-graph, personality-analysis, concall, movie-script, management, sales-intelligence]
related: ["[[21-knowledge-graph-intro]]", "[[23-knowledge-graph-ecommerce]]", "[[25-memory-dark-side]]", "[[AI Ecosystem Index]]"]
week: 5
day: 4
category: ai
---

# Hook
> Oka movie lo — idi villain evadu? Protagonist ni ela influence chesaadu? Evaru allegiance change chesaadu? Script chadivite meeru intuitively answer chestamu. Knowledge graph same thing chestundi — characters nodes ga, relationships edges ga — scale lo.

# Core Idea
_The same knowledge graph structure that maps legal clause cross-references and product purchase relationships can map characters and their interactions in a movie script, speakers and their positions in an earnings call, or executives and their communication patterns in a company. Nodes are people. Edges are relationships — "agrees with," "contradicts," "influences," "mentions," "reports to." AI traverses these graphs to identify key influencers, detect conflict, surface personality patterns, and flag risk._

---

# Details
_Research & facts to write a better script from_

## Movie Script — Character Relationship Graph

A movie script is a structured document with characters, scenes, and dialogue. A knowledge graph maps it as:

**Nodes:**
- Characters (Protagonist, Antagonist, Mentor, Ally, Rival)
- Scenes (each scene = a node)
- Themes / Topics discussed in each scene

**Edges:**
- Character → appears_in → Scene
- Character → speaks_to → Character (in which scene)
- Character → influences → Character (tracks who shifts whose decisions)
- Character → conflicts_with → Character
- Character → changes_allegiance → other side (at which scene)
- Character → mentions → Theme (loyalty, revenge, money)

**Queries you can run:**
- "Who is the central influencer in the story?" → find the node with most incoming "influenced by" edges
- "At what point does X shift from ally to antagonist?" → find the scene where the allegiance edge changes direction
- "Which characters share the most scenes but have the most conflict?" → find high co-occurrence + conflict edge pairs
- "What theme drives the protagonist's decisions?" → most frequent theme node connected to protagonist's dialogue

**Real application:** Netflix and studios use graph-based script analysis to assess story structure, character arc completeness, and audience engagement prediction before production.

## Earnings Call / Concall Analysis

Every public company does quarterly earnings calls — 45-60 minutes of executives presenting results and analysts asking questions. Thousands of these happen every quarter. No human team can track them all.

**Knowledge graph of a concall:**

**Nodes:**
- Speakers (CEO, CFO, analysts)
- Topics (revenue growth, margin, guidance, competition, layoffs)
- Companies mentioned
- Products mentioned
- Time segments (Q1 results, Q2 outlook, Q&A)

**Edges:**
- Speaker → mentions → Topic
- Speaker → agrees_with → Speaker
- Speaker → contradicts → previous_statement
- Speaker → avoids_answering → Question (analyst asked, CEO pivoted)
- Topic → mentioned_by → Speaker (frequency weighted)
- Company → mentioned_as_competitor_by → Speaker

**Queries you can run:**
- "What topics did the CEO avoid answering directly?" → find question nodes where answer edge leads to a different topic
- "Which analyst asked the most aggressive questions?" → analyst node with most "challenged" edges
- "Did the CFO contradict the CEO on margin guidance?" → find contradiction edges between their statements on the same topic
- "Which competitor was mentioned most this quarter vs last quarter?" → compare edge weights across time

**Real product: Gong.io**
- Mentioned in Week 2 D7 (AI Value Chain Extension) — records sales calls
- Graph layer: speaker nodes, topic nodes, sentiment edges, objection patterns, competitor mentions
- Gong's "Deal Intelligence" identifies at-risk deals by analyzing relationship patterns in call transcripts
- Valuation: $7.25 billion (2021). The core product = knowledge graph on sales conversations.

**AlphaSense:**
- Enterprise search platform for financial research
- Knowledge graph across earnings calls, SEC filings, analyst reports, news
- "What has Tesla's CFO said about battery costs across the last 8 quarters?" → graph traversal across 8 call transcripts, CFO node, battery cost topic node
- Used by hedge funds, investment banks, Fortune 500 companies
- Raised $650M, valued at $4 billion (2024)

## Management / Org Analysis

Same graph, applied to internal company communications:

**Nodes:** Employees, Teams, Projects, Decisions, Meetings

**Edges:**
- Employee → reports_to → Manager
- Employee → collaborates_with → Employee (frequency, channel)
- Employee → initiates → Decision
- Employee → blocked_by → Employee (dependency)
- Team → owns → Project

**Queries:**
- "Who are the informal influencers outside the org chart?" → employees with high "consulted by" edges despite low hierarchy position
- "Which projects have the most dependencies?" → nodes with most incoming "blocked by" edges
- "Which manager has the highest communication centrality?" → most paths in the graph pass through this node

Microsoft Viva (workplace analytics tool) does exactly this — using anonymized communication graph data from Teams, email, and calendar to show managers communication health, collaboration patterns, and potential burnout signals.

## The Pattern Across All Three

| Use Case | Nodes | Key Edges | Key Queries |
|----------|-------|-----------|-------------|
| Movie Script | Characters, Scenes | influences, conflicts_with, appears_in | Who's central? When did allegiance shift? |
| Concall | Speakers, Topics | mentions, avoids, contradicts | What's being hidden? Who's aggressive? |
| Management | Employees, Teams | reports_to, collaborates_with, blocked_by | Who are real influencers? Where are bottlenecks? |

Same graph. Different domain. Same traversal logic.

---

# Breakdown
_Reel script_

1. **Hook** — "Movie script lo villain evadu? Protagonist ni ela influence chesaadu? Meeru intuitively answer chestamu — characters, relationships, scenes mentally map chestamu. Knowledge graph same thing chestundi — scale lo. Thousands of scripts, hundreds of calls."

2. **Movie script graph** — "Characters = nodes. Scenes = nodes. Edges: 'speaks to,' 'influences,' 'conflicts with,' 'allegiance change.' Query: 'eppudu X ally nunchi antagonist ayyadu?' → scene node where allegiance edge reverses. 'Central influencer evadu?' → most incoming influence edges. Netflix adi uses to analyze story structure before production."

3. **Concall analysis** — "Quarterly earnings call — CEO, CFO, analysts, 60 minutes. Thousands of calls per quarter. Graph: speakers = nodes, topics = nodes. Edges: 'mentions,' 'avoids answering,' 'contradicts.' Query: 'CEO emi questions avoid chesaadu?' → question node, answer edge different topic ki points. 'CFO CEO tho contradict ayyada?' → graph check."

4. **Gong and AlphaSense** — "Gong: sales calls record chestundi, graph layer add chestundi — topic nodes, competitor mentions, objection patterns, deal risk signals. $7.25 billion valuation. AlphaSense: 8 quarters of Tesla CFO battery cost statements → one graph query. Hedge funds use this. $4 billion valuation."

5. **Management graph** — "Org chart = graph. Employee nodes, 'reports to' edges. But real influence: 'consulted by' edges. Informal leaders — low hierarchy, high 'consulted by' count. Microsoft Viva: anonymized Teams + email + calendar graph → collaboration health, burnout signals, hidden bottlenecks."

6. **Bridge to dark side** — "Anni use cases: same graph, different domain. Kaani oka question: idi wrong data tho build chesthe? Wrong relationships, wrong nodes? D5 lo — memory poisoning. Wrong memory fed to AI = wrong outputs. Scale lo."

---

# Caption

```
Movie script lo villain evadu? eppudu allegiance change chesaadu?

Knowledge graph: characters = nodes, relationships = edges.
"influences," "conflicts with," "allegiance change scene."

Same logic — concall analysis:
CEO, CFO, analysts = speaker nodes. Topics = nodes.
"CEO emi questions avoid chesaadu?" → question node → answer goes different direction.
"CFO margin lo contradict ayyada?" → graph check.

Gong: sales calls lo speaker + topic + objection graph → deal risk prediction. $7.25B valuation.
AlphaSense: 8 quarters Tesla CFO battery statements → one graph query. Hedge funds use this.

Management: org chart = graph. Informal leaders = high "consulted by" edges, low hierarchy position.
Microsoft Viva: Teams + email graph → collaboration health.

Same graph. Different domain. Movie, business, management — anni same traversal logic.

.
.
.
#ai #knowledgegraph #analytics #gong #concall #management #telugu #telugutech
```

# Visual Notes
- Open with a movie (relatable — Baahubali or RRR character web)
- Character relationship web: protagonist, antagonist, mentor, ally — nodes with labeled edges
- "Allegiance shift" — edge direction reversal at a specific scene node
- Concall graph: speaker nodes + topic bubbles + avoidance arrow (question → pivot to different topic)
- Gong logo + "$7.25B" stat. AlphaSense logo + "$4B"
- Org chart → real influence graph (formal hierarchy vs actual communication graph)
- Microsoft Viva dashboard screenshot (publicly available)
- Tone: mind-expanding. Same tool, three completely different worlds.

# Sources / Links
- Gong.io — valuation $7.25B (2021), deal intelligence features
- AlphaSense — $650M raise, $4B valuation (2024), alphase.com
- Microsoft Viva — microsoft.com/en-us/microsoft-viva
- Netflix script analysis — various tech blog posts on graph-based story analysis
- Organizational network analysis (ONA) — Rob Cross research, Connected Commons

# Related Notes
- [[21-knowledge-graph-intro]]
- [[23-knowledge-graph-ecommerce]]
- [[25-memory-dark-side]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

one more example like using knowledge graph in analysing management of a company or concall or even a movie script so we can identify the personalities
