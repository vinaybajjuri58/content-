---
title: Knowledge Graphs — When AI Needs to Understand Relationships, Not Just Text
phase: AI ecosystem
topic: knowledge graph, memory, graph database, entities, relationships
format: reel
status: draft
scheduled:
tags: [ai, memory, knowledge-graph, graph-database, neo4j, entities, relationships]
related: ["[[18-rag-explained]]", "[[22-knowledge-graph-legal-docs]]", "[[23-knowledge-graph-ecommerce]]", "[[AI Ecosystem Index]]"]
week: 5
day: 1
category: ai
---

# Hook
> Chinnappudu oka riddle: A is B's sister. B is the brother of C. Ante A ki C enti? Sister. Easy. Meeru oka chain of relationships traverse chesaaru. AI kuda exactly same way knowledge graphs tho work chestundi — relationships follow chesi answer kadugutuundi.

# Core Idea
_RAG finds relevant text chunks. Knowledge graphs understand how entities relate to each other. When the answer requires connecting multiple pieces of information — not just finding one passage — knowledge graphs are more powerful. Google Search Knowledge Panel, Facebook's social graph, LinkedIn's professional network — all knowledge graphs. Now AI uses the same structure to reason across complex, interconnected data._

---

# Details
_Research & facts to write a better script from_

## The Limitation of RAG

RAG is powerful — retrieve relevant text chunks, answer from them. But RAG has a fundamental limitation: it retrieves *passages*, not *relationships*.

**Example:**
You have a knowledge base with:
- Document A: "Rajesh is the CEO of Zomato"
- Document B: "Zomato acquired Blinkit in 2022"
- Document C: "Blinkit's warehouse network covers 12 cities"

Query: "How many cities does the CEO of Zomato's acquired company cover?"

RAG: searches for the query → might find Document B (Zomato acquired Blinkit) → but misses the chain: CEO → Zomato → Blinkit → warehouse coverage.

To answer this correctly, you need to *traverse relationships* — not retrieve a single passage.

Knowledge graph: CEO (Rajesh) → leads → Zomato → acquired → Blinkit → has → warehouse network → covers → 12 cities. One traversal. Correct answer.

## What Is a Knowledge Graph

A knowledge graph stores information as:
- **Nodes (Entities):** People, places, companies, products, concepts — anything that exists
- **Edges (Relationships):** The connections between entities — "works at," "acquired," "related to," "bought with," "mentioned in"
- **Properties:** Attributes of each node or edge — "CEO since 2015," "acquisition value $700M"

**Simple riddle as a graph:**
- Node: A (person)
- Node: B (person)
- Node: C (person)
- Edge: A → is sister of → B
- Edge: B → is brother of → C
- Query: what is A to C?
- Graph traversal: A is sister of B, B is brother of C → A is sister of C

A 10-year-old solves this intuitively. A knowledge graph solves it computationally — across millions of nodes.

## Knowledge Graphs Are Not New

Knowledge graphs have existed in tech for decades:

**Google Knowledge Graph (2012):**
- Launched May 2012
- Powers the information panel on the right side of Google Search
- When you search "Sachin Tendulkar" — you see his birthdate, wife, children, records, teams — all from a knowledge graph
- Contains over 500 billion facts about 5 billion entities (as of 2020)

**Facebook Social Graph:**
- Every person is a node. Every friendship is an edge. Every like, tag, group membership = relationship.
- Powers friend recommendations, content ranking, ad targeting
- As of 2024: ~3 billion users, tens of billions of edges

**LinkedIn Economic Graph:**
- 1 billion+ members, companies, skills, jobs as nodes
- "People also viewed," "You might know," job recommendations — all graph traversals

**Wikidata:**
- Free, open knowledge graph underlying Wikipedia
- 100 million+ items, 1.4 billion statements, in 300+ languages

## Knowledge Graph vs RAG — When to Use Which

| Scenario | RAG | Knowledge Graph |
|----------|-----|-----------------|
| "What is your return policy?" | Best | Overkill |
| "Which products were bought by customers who also bought X?" | Struggles | Built for this |
| "Who influences whom in this org chart?" | Cannot | Native |
| "Which legal clause does Section 4 reference?" | Can miss chains | Handles perfectly |
| "What did the CEO say about the CFO's department in Q3?" | Partial | Combines both |

Best enterprise systems combine both: knowledge graph for relationships, RAG for text retrieval within nodes.

## Graph Databases — The Technology

Knowledge graphs live in graph databases — specialized databases built for relationship traversal.

**Neo4j** — most popular graph database. Used by NASA, Walmart, eBay, UBS.
- Walmart uses Neo4j to power product recommendations — 250 million products, billions of "bought with" relationships
- NASA uses it to map dependencies between spacecraft components

**Amazon Neptune** — managed graph DB on AWS
**Microsoft Azure Cosmos DB** — multi-model, includes graph
**TigerGraph** — enterprise graph analytics
**ArangoDB** — open source multi-model

**Cypher query language (Neo4j):**
```
MATCH (a:Person)-[:SISTER_OF]->(b:Person)-[:BROTHER_OF]->(c:Person)
RETURN a.name AS sister_of_c
```
This is exactly the riddle — written as a database query.

## How AI Uses Knowledge Graphs

Modern AI + knowledge graph integration:

1. **GraphRAG (Microsoft, 2024):** Combines knowledge graph + RAG. Build a graph from documents → use graph structure to guide retrieval. Microsoft open-sourced GraphRAG in July 2024. Shows significant improvement over standard RAG for complex multi-hop questions.

2. **Neo4j + LLM:** Store your data in Neo4j → LLM generates Cypher queries from natural language → query executes → LLM explains results in plain language.

3. **Google Gemini + Knowledge Graph:** Gemini can access Google's knowledge graph directly — powering factual grounding in answers.

---

# Breakdown
_Reel script_

1. **Hook** — "Chinnappudu riddle: A is B's sister. B is brother of C. A ki C enti? Sister — easy. Meeru chain of relationships follow chesaaru. AI kuda same way work chestundi — knowledge graphs tho. Idi explain chestanu."

2. **RAG limitation** — "RAG text chunks retrieve chestundi. Kaani 'CEO of Zomato's acquired company ki enni cities?' — idi oka chain question. Document lo single answer ledu. Rajesh → Zomato → Blinkit → 12 cities — relationships traverse cheyyali. RAG adi miss chestundi."

3. **What a knowledge graph is** — "Nodes: people, companies, products — entities. Edges: relationships between them — 'works at,' 'acquired,' 'bought with.' Riddle graph: A is sister of B → B is brother of C → traverse → A is sister of C. Computationally. Millions of nodes tho."

4. **Not new** — "Google Knowledge Graph: 2012. Sachin Tendulkar search chesthe right side lo anni details — graph. 500 billion facts, 5 billion entities. Facebook social graph: 3 billion users, every friendship an edge. LinkedIn economic graph: 1 billion members. Anni knowledge graphs."

5. **AI + graph** — "Microsoft 2024: GraphRAG — combines knowledge graph + RAG. Complex multi-hop questions lo significant improvement. Neo4j + LLM: natural language lo ask cheyyi → Cypher query generate avutundi → graph traverse → answer. Walmart uses this for 250 million product recommendations."

6. **Bridge** — "D2, D3, D4 lo 3 real use cases chudatamu — legal docs, e-commerce, concall analysis. Anni same structure: entities + relationships + AI traversal."

---

# Caption

```
Chinnappudu riddle: A is B's sister. B is C's brother. A ki C enti?

Sister. Easy. Meeru relationships chain follow chesaamu.

AI kuda same way work chestundi — knowledge graphs tho.

RAG: text chunks retrieve chestundi. Answer oka passage lo unte — perfect.
Knowledge Graph: answer multiple relationships lo spread ayyunte — idi.

Nodes = entities (people, companies, products)
Edges = relationships (works at, acquired, bought with)

Google Search right side panel — knowledge graph. 500 billion facts.
Facebook friend recommendations — social graph. 3 billion users.
Walmart product recommendations — graph. 250 million products.

Microsoft 2024: GraphRAG — combines both. Complex questions lo major improvement.

D2, D3, D4: 3 real use cases — legal docs, e-commerce, personality analysis.

.
.
.
#ai #knowledgegraph #graphdb #neo4j #memory #telugu #telugutech #aiexplained
```

# Visual Notes
- Open with the riddle on screen: A → sister → B → brother → C. Question mark: A to C?
- Graph visualization: nodes with labels, arrows showing relationships. Simple, clean.
- RAG vs Knowledge Graph comparison: RAG finds one passage. Graph traverses a chain.
- Google Knowledge Panel: screenshot of a search result showing the info panel
- Neo4j graph screenshot — colorful node-edge visualization
- GraphRAG: Microsoft announcement visual, July 2024
- Tone: start simple (riddle), build up. By the end, it should feel natural.

# Sources / Links
- Google Knowledge Graph — "Introducing the Knowledge Graph" Google Blog, May 2012
- Google Knowledge Graph scale — 500B facts, Google I/O 2020
- GraphRAG — Microsoft Research blog, July 2024, github.com/microsoft/graphrag
- Neo4j use cases — neo4j.com/customers (Walmart, NASA, eBay)
- Wikidata statistics — wikidata.org/wiki/Wikidata:Statistics
- Facebook Social Graph — Meta Engineering blog

# Related Notes
- [[18-rag-explained]]
- [[22-knowledge-graph-legal-docs]]
- [[23-knowledge-graph-ecommerce]]
- [[24-knowledge-graph-personality-analysis]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

then comes the knowledge graph explaination using the childhood games related to relations like if A is B's sister and And B is brother of C what A is to C
