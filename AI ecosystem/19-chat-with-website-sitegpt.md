---
title: Chat with Any Website — How SiteGPT Works
phase: AI ecosystem
topic: RAG use case, chat with website, SiteGPT, customer support AI
format: reel
status: draft
scheduled:
tags: [ai, rag, sitegpt, chatbot, customer-support, saas, business]
related: ["[[18-rag-explained]]", "[[20-chat-with-video-notebooklm]]", "[[13-customer-support-tool-demo]]", "[[AI Ecosystem Index]]"]
week: 4
day: 4
category: ai
---

# Hook
> Oka website ki vellav. 40 pages of documentation undi. Meeru search chesav, scroll chesav — answer దొరకలేదు. Ippudu same website lo oka chatbot undi: "What's your refund policy for annual plans?" → exact answer, 3 seconds lo. Idi RAG. Idi SiteGPT.

# Core Idea
_SiteGPT and products like it let any business turn their entire website — help articles, FAQs, product pages, policy docs — into a conversational AI chatbot. No more search. No more scrolling. Users ask questions in plain language and get exact answers. Under the hood: RAG. This episode shows how the D2 vector DB + D3 RAG concepts power a real product generating millions in revenue._

---

# Details
_Research & facts to write a better script from_

## The Problem This Solves

Every business has a website with information. FAQs, pricing pages, return policies, setup guides, troubleshooting docs. The problem:

**For users:** Finding the right answer requires knowing the right search terms, knowing which page to look at, and reading through long articles to find the one sentence that answers the question.

**For businesses:** Customer support teams spend 60–80% of their time answering the same 20 questions repeatedly. These are already answered in the documentation. People just don't find it.

**The cost:** According to Gartner, the average cost of a human-handled customer service interaction is $8–12. A digital (chatbot) interaction: $0.10. For companies with 10,000 support tickets/month, that's a $80,000–$120,000 per month problem vs a $1,000 problem.

## What SiteGPT Does

SiteGPT is a Y Combinator-backed product that lets businesses:
1. Paste their website URL
2. SiteGPT crawls every page and indexes the content
3. A chatbot is trained on that content using RAG
4. Business embeds the chatbot widget on their website
5. Users can now ask any question in plain language and get grounded answers from the actual website content

**Key products in this space:**
- SiteGPT — YC-backed, fast deployment, no-code
- Chatbase — reportedly crossed $3M ARR within months of launch (2023). Simple UI, widely used.
- DocsBot AI — focused on documentation-heavy products (developer tools, SaaS)
- CustomGPT.ai — enterprise-focused, supports private document uploads
- Intercom Fin — Intercom's AI layer built on GPT-4, launched 2023. Intercom charges $0.99 per resolved conversation.

## How It Works Under the Hood (RAG)

**Indexing phase:**
1. Crawler visits every page on the website
2. Content extracted from each page (text, headings, FAQs)
3. Content split into chunks (~300-500 words each)
4. Each chunk converted to a vector embedding
5. All vectors stored in a vector database

**Chat phase (every user message):**
1. User types: "Can I get a refund if I cancel my annual plan mid-year?"
2. That message → vector embedding
3. Vector DB similarity search → finds top 3-5 chunks most relevant to "annual plan refund cancellation"
4. Those chunks injected into LLM prompt
5. LLM reads the chunks → generates a specific, grounded answer
6. Sources cited: "Based on our Refund Policy page: ..."

The chatbot never guesses. Every answer is grounded in the actual website content.

## What Businesses Use This For

**E-commerce:** Product FAQs, return policies, shipping times, size guides. Reduce support volume.

**SaaS companies:** Documentation chatbots. Instead of searching through 500 help articles, developers ask questions directly. DocsBot targets this segment.

**Real estate:** Property listings as a knowledge base — prospects ask "show me 3BHK flats under ₹80L in Hyderabad" and get matches.

**Healthcare:** Hospital websites — "what documents do I need for admission?" → answer from their own admissions guide.

**Education:** University websites — admission process, fee structure, hostel availability — all answerable without calling the office.

## The Business Model

SiteGPT pricing (approximate, 2024):
- Starts ~$19–49/month for small businesses
- Scales by number of pages indexed and conversations per month
- Enterprise plans: custom

Chatbase monetization strategy: freemium → viral → convert. Free tier for small sites → users see the product working → upgrade or share with others. This is how it hit $3M ARR quickly.

Intercom Fin: $0.99 per *resolved* conversation. No resolution = no charge. High-confidence business model. Intercom reported Fin resolves ~50% of incoming support questions autonomously.

## The Broader Market

The AI customer support market was valued at $2.5 billion in 2023 and projected to reach $8.2 billion by 2028 (MarketsandMarkets). Every company with a website and a support team is a potential customer.

Indian context: Companies like Freshdesk (Chennai-based, acquired by Freshworks) are adding AI layers. Zoho launched Zia AI assistant. The Indian SaaS market is adopting these tools rapidly.

---

# Breakdown
_Reel script_

1. **Hook** — "40 pages of documentation. User question ki answer search cheyyadam annoying. Same website lo oka chatbot unte: 'annual plan refund cheyyocha?' — 3 seconds lo exact answer. Scroll ledu. Search ledu. Idi RAG powered website chatbot. SiteGPT."

2. **The problem** — "Every business has docs — FAQs, policies, product pages. Problem: users don't find answers. Support teams repeat same answers 100 times a day. Gartner: human support call = $8–$12. Chatbot interaction = $0.10. 10,000 tickets/month company: $100K vs $1K."

3. **How SiteGPT works** — "URL paste cheyyi → SiteGPT website crawl chestundi → content chunks lo split chestundi → vectors ga convert chesaaka vector DB lo store chestundi. User question → similarity search → relevant chunks → LLM reads → grounded answer. Guess kaadu — actual website content chaduvutundi."

4. **Real products** — "SiteGPT — YC backed. Chatbase — $3M ARR in months of launch. Intercom Fin — GPT-4 powered, $0.99 per resolved conversation, 50% of support tickets automatically resolved. DocsBot — developer documentation. Idi already running businesses."

5. **Use cases** — "E-commerce return policies. SaaS documentation. Real estate listings. Hospital admission process. University fee structure. Anni cases lo same thing: website content → chatbot → user gets answer without waiting for human support."

6. **Bridge** — "Website RAG chusamu. Next: same logic, different media — Video. NotebookLM tho 3-hour podcast upload chesthe — 10 minutes lo entire summary, questions, insights. D5 lo."

---

# Caption

```
40 pages of docs. User scrolls 10 minutes. Answer దొరకలేదు.

SiteGPT tho: same website, chatbot lo ask chesthe → 3 seconds lo exact answer.

Ela work chestundi — RAG:
Website crawl → chunks → vectors → vector DB
User question → similarity search → relevant chunks → LLM reads → grounded answer

Real products running on this:
Chatbase — $3M ARR in months
Intercom Fin — resolves 50% of support tickets automatically, $0.99/resolved conversation
SiteGPT — YC backed

Gartner: human support call = $8-12. Chatbot = $0.10.
10,000 tickets/month lo adi $100K vs $1K difference.

Every website ki idi possible. Customer support + RAG = product.

.
.
.
#ai #rag #chatbot #customersupport #sitegpt #saas #telugu #telugutech #aiproducts
```

# Visual Notes
- Open with frustrating website search experience — multiple clicks, no answer found
- Cut to: chatbot widget, one question, instant answer with source cited
- RAG pipeline visual: website pages → crawl → chunks → vector DB → user query → answer
- Product logos: SiteGPT, Chatbase, Intercom Fin, DocsBot
- Cost comparison visual: $8-12 (human) vs $0.10 (chatbot) — per conversation
- Intercom Fin stat: "50% of support tickets resolved autonomously"
- Tone: business-focused. Show the ROI, not just the tech.

# Sources / Links
- SiteGPT — sitegpt.ai (YC W23)
- Chatbase $3M ARR — reported in indie hacker communities, 2023
- Intercom Fin launch — intercom.com/fin, April 2023
- Gartner customer service cost per contact — Gartner research
- AI customer support market $8.2B by 2028 — MarketsandMarkets
- Freshworks/Freshdesk AI features — freshworks.com

# Related Notes
- [[18-rag-explained]]
- [[20-chat-with-video-notebooklm]]
- [[13-customer-support-tool-demo]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

Chat with Website like SiteGPT business, and then customer support example, maybe we can remove it in the previous section not sure of it
