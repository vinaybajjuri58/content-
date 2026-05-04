---
title: Customer Support AI Demo — Real Data Via Tool Call
phase: AI ecosystem
topic: tool calling, customer support, CRM, human-in-the-loop
format: reel
status: draft
scheduled:
tags: [ai, tool-calling, customer-support, crm, human-in-the-loop, demo]
related: ["[[12-cursor-tool-demo]]", "[[14-remotion-skill-demo]]", "[[15-tools-gone-wrong]]", "[[AI Ecosystem Index]]"]
week: 3
day: 4
category: ai
---

# Hook
> Zomato support ki "my order hasn't arrived" antey — mee order ID cheppakkarledu. AI ne fetch chesindi. Order ID, delivery partner status, estimated time — anni. Ela? Tool call.

# Core Idea
_A traditional chatbot only knows what it was scripted to say. An AI with tool access can query your actual account, check live order status, process a refund — all in real time. The difference between a chatbot that says "sorry for the inconvenience" and one that actually solves your problem is tool calling._

---

# Details
_Research & facts to write a better script from_

## Traditional Chatbot vs AI with Tools

**Traditional chatbot (scripted):**
- Decision tree based — "if user says X, respond with Y"
- Can only answer what was pre-programmed
- Can't access your actual account, order, or data
- The "sorry for the inconvenience, please call our helpline" machine
- Customers hate these — they solve nothing

**AI with tool access:**
- LLM understands natural language — no rigid decision tree
- Given tools: `get_customer_account(customer_id)`, `get_order_status(order_id)`, `initiate_refund(order_id, amount)`, `update_ticket(ticket_id, resolution)`
- Can look up your actual data, reason over it, and take action
- The difference: real answers, not scripted deflection

## The Tool Call Chain for Customer Support

When a customer says "my order #12345 hasn't arrived, I want a refund":

1. `authenticate_customer(session_token)` — verify who is asking
2. `get_order_details(order_id: "12345")` — fetch order from database: item, value, delivery partner, estimated time
3. `check_delivery_status(tracking_id)` — call delivery partner API: current location, delay reason
4. `check_refund_eligibility(order_id)` — verify policy: is this order refund-eligible?
5. If eligible and within threshold: `initiate_refund(order_id, amount)` — process it
6. `create_support_ticket(customer_id, resolution)` — log the resolution
7. Reply to customer with full context and confirmation

- Entire sequence: seconds. No human agent involved.
- Companies using this: Intercom Fin, Zendesk AI, Ada, Freshworks Freddy

## Human-in-the-Loop vs Auto-Execute

This is one of the most important concepts in AI agent design:

**Human-in-the-loop:**
- AI surfaces a recommendation: "This order qualifies for a ₹350 refund. Shall I process it?"
- Human (agent or customer) confirms before action is taken
- Slower, but reversible — the AI's mistake can be caught before execution
- Required for high-stakes actions: large refunds, account changes, cancellations

**Auto-execute:**
- AI processes the refund directly, notifies customer of completion
- Faster, no friction
- But: if the AI made a wrong judgment — wrong order refunded, wrong amount — the action is already done
- Required guardrail: tight rules on what can be auto-executed and what requires confirmation

**The design question every product team answers:**
- Refund under ₹200: auto-execute
- Refund over ₹5,000: human confirmation required
- Account deletion: always human review
- Wrong answer here → D6 examples

## Real-World Scale
- Intercom reports their AI agent (Fin) resolves 51% of customer queries without human involvement
- Klarna (buy-now-pay-later company) reported their AI assistant handled 2.3 million conversations in its first month — equivalent to 700 full-time human agents
- Estimated annual savings from customer support AI: $8 billion by 2025 (Juniper Research)
- The risk: when the AI agent has refund/credit/account-action permissions and makes a wrong call at scale

---

# Breakdown
_Reel script_

1. **Hook** — "Zomato support ki 'my order hasn't arrived' antey — meeru order ID type cheyyakkarledu. AI ne teesukondi. Order details, delivery partner status, estimated time — anni AI daggare vachindhi. Ela? Tool call."

2. **Old chatbot vs AI with tools** — "Paata chatbot: decision tree. 'Order issue?' → 'Sorry for the inconvenience, call our helpline.' Useless. Tool access unna AI: mee account query chesindi, order database nundi status fetch chesindi, delivery API call chesindi. Real answer."

3. **The tool chain** — "Meeru 'refund kavali' antey AI emi chestundi: authenticate chestundi → order details fetch chestundi → refund eligibility check chestundi → refund process chestundi → ticket create chestundi. 5 tool calls. Seconds lo. Human agent involve avvadu."

4. **Human-in-the-loop** — "Ikkade important design decision. AI refund automatic ga process cheyyali? Leda meeru confirm cheskonate? Small amounts: auto. Large amounts: confirm cheskoni. Idi wrong ga decide chesthe — D6 lo chudatamu ela damage avutundo."

5. **Real scale** — "Klarna — buy now pay later company — AI assistant oka month lo 2.3 million conversations handle chesindi. 700 full-time human agents equivalent. Tools lekapothe idi possible kaadu."

6. **The pattern** — "Tool calling ante idi: AI model + real world data access + action permission. Support kaadu — bank lo, hospital lo, government services lo — anni places lo idi jarugutondi. Permissions design correct ga cheyyakapothe — D6."

---

# Caption

```
Zomato support ki "order hasn't arrived" antey — meeru emi type cheyyakkarledu.

AI ne fetch chesindi. Tool call chesindi.

Order database → delivery API → refund eligibility → process → ticket log. 5 tool calls. Seconds.

Paata chatbot: "sorry for inconvenience." Tool access unna AI: solved.

Klarna: oka month lo 2.3 million conversations. 700 human agents equivalent.

Ikkade catch: AI ki refund permission istey — wrong ga chesthe damage at scale. D6 lo chudatamu.

.
.
.
#ai #toolcalling #customersupport #aiagent #telugu #telugutech #automation
```

# Visual Notes
- Show the contrast: old chatbot "sorry for inconvenience" response vs AI with tools actually solving
- Animate the tool call chain step by step: each database/API call as a visual node
- Human-in-the-loop visual: AI surfacing a recommendation → human approves → action taken
- Auto-execute visual: AI → direct action → confirmation sent
- End with Klarna stat as a data visual

# Sources / Links
- Intercom Fin AI agent — resolution rate statistics
- Klarna AI assistant — 2.3M conversations report (February 2024)
- Juniper Research — customer support AI savings forecast
- Ada, Zendesk AI, Freshworks Freddy — enterprise AI support tools

# Related Notes
- [[12-cursor-tool-demo]]
- [[14-remotion-skill-demo]]
- [[15-tools-gone-wrong]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_
