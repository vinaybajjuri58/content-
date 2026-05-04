---
title: Knowledge Graph Use Case — E-commerce Recommendations
phase: AI ecosystem
topic: knowledge graph, e-commerce, recommendations, Amazon, Flipkart, Meesho
format: reel
status: draft
scheduled:
tags: [ai, knowledge-graph, ecommerce, recommendations, amazon, flipkart, graph-database]
related: ["[[21-knowledge-graph-intro]]", "[[22-knowledge-graph-legal-docs]]", "[[24-knowledge-graph-personality-analysis]]", "[[AI Ecosystem Index]]"]
week: 5
day: 3
category: ai
---

# Hook
> Oka shirt buy chesaav Amazon lo. "Customers who bought this also bought: pants, belt, matching shoes." Idi accident kaadu — idi knowledge graph. Oka shirt ki pant connection undi — millions of transactions lo find chesaaru. Mee next purchase predict chesindi.

# Core Idea
_E-commerce recommendation engines are knowledge graphs. Every product, customer, category, and brand is a node. Every purchase, view, wishlist add, and "bought together" event is an edge. When you buy a shirt, the graph traverses: shirt → bought with → pant → bought with → belt → same category → other belts → bought by → customers like you → also bought → shoes. That's why the recommendations feel eerily accurate. Amazon attributes 35% of its revenue to this graph._

---

# Details
_Research & facts to write a better script from_

## The Simple Version — "Bought Together"

Most people think Amazon's "customers also bought" is a simple correlation: "people who buy X also buy Y." That's the starting point — but the knowledge graph goes much deeper.

**Basic relationship:**
- Customer A bought: shirt, pant, belt
- Customer B bought: shirt, shoes, watch
- Customer C bought: pant, belt, shoes

Graph edges created:
- shirt → bought_with → pant (by A)
- shirt → bought_with → belt (by A)
- shirt → bought_with → shoes (by B)
- pant → bought_with → belt (by A and C)
- belt → bought_with → shoes (by C)

New customer buys a shirt:
- Graph: shirt → bought_with → pant, belt, shoes
- Pant + belt have the strongest connection (2 customers, not 1)
- Recommendation: "Frequently bought together: pant, belt"

## The Full Knowledge Graph — E-commerce

**Nodes in a real e-commerce graph:**
- Products (each SKU)
- Customers
- Categories (shirts, pants, formal wear)
- Brands (Zara, H&M, Raymond)
- Occasions (office wear, wedding, casual)
- Attributes (blue color, cotton fabric, size M)
- Price ranges

**Edges:**
- Customer → bought → Product
- Customer → viewed → Product
- Customer → added_to_wishlist → Product
- Product → belongs_to → Category
- Product → made_by → Brand
- Product → suitable_for → Occasion
- Product → has_attribute → Color / Fabric / Size
- Product → frequently_bought_with → Product
- Product → similar_to → Product (same category, overlapping attributes)
- Customer → similar_to → Customer (overlapping purchase history)

**Query: "New customer bought a blue formal shirt. What to recommend?"**

Graph traversal:
1. Blue formal shirt → belongs_to → Formal Wear category
2. Formal Wear → frequently_bought_with → Formal Pants, Formal Belt, Formal Shoes
3. Blue formal shirt → has_attribute → Blue → frequently_paired_with → Navy pants, Grey pants
4. Customers who bought this shirt → also_bought → Black Oxford shoes (strong edge, many customers)
5. Customer profile: first purchase, unknown preferences → recommend top 3 by edge weight

Result: "Navy formal pants, black Oxford shoes, formal belt" — specific, grounded, personalized.

## Amazon — The Numbers

- Amazon's recommendation engine drives **35% of total revenue** (McKinsey, frequently cited)
- Amazon's 2023 revenue: $574 billion → 35% = ~$200 billion influenced by recommendations
- Amazon uses a combination of collaborative filtering (knowledge graph) + deep learning for ranking
- Their system processes billions of interactions per day to update edge weights in real time

**"People who viewed this also viewed"** — graph traversal across view events
**"Inspired by your browsing history"** — graph from your session
**"Buy again"** — time-series edges: when did you last buy this, when do you typically repurchase?

## Indian E-commerce — Flipkart, Meesho, Myntra

**Flipkart (Walmart-owned):**
- India's largest e-commerce platform by some metrics
- Uses knowledge graph for fashion recommendations — "complete the look" feature
- Fashion graph: outfit → shirt node + pant node + shoe node all connected under an "outfit" ensemble node
- "Complete the look" = traverse the outfit node → find missing items for this customer

**Meesho:**
- Primarily serves Tier 2-3 India
- Knowledge graph includes regional preferences — products popular in specific cities, festivals, seasons
- "Customers in Vizag who bought X also bought Y" — geographic edges on the graph

**Myntra:**
- Fashion-only — deeper fashion knowledge graph
- Occasion nodes: Diwali → recommended outfits → connects to festive product nodes
- Stylist recommendations feature = curated graph traversal paths

## Beyond "Bought Together" — Advanced Graph Use Cases

**Inventory-aware recommendations:**
- Node: Product → has_edge → Stock Level (low stock)
- Graph can de-prioritize low-stock items or suggest alternatives when out of stock
- Flipkart uses this to avoid recommending items that can't be delivered to your pin code

**Return prediction:**
- Customer → returned → Products (historical edge)
- Product → high_return_rate → True (edge to attribute)
- If customer profile overlaps with high-return customers and product has high return rate: lower recommendation priority or add "note: check size guide"

**Price sensitivity graph:**
- Customer → typically_buys_in → Price Range (₹500-₹1500)
- Product → priced_at → ₹2000
- Graph knows this product is outside this customer's typical range → recommend it only if it's on sale or similar items exist in their range

---

# Breakdown
_Reel script_

1. **Hook** — "Shirt buy chesaav. 'Customers also bought: pants, belt, shoes.' Idi accident kaadu. Idi knowledge graph. Every purchase, every view, every combination — edges ga store ayyindi. Graph traverse chesaaka mee next purchase predict avutundi."

2. **The basic graph** — "Nodes: products, customers, categories, brands, occasions. Edges: 'bought with,' 'viewed,' 'belongs to,' 'similar to.' Shirt buy chesthe → graph: shirt → bought_with → pant (strong edge, thousands of customers), → belt, → shoes. Top 3 recommend avutundi."

3. **Amazon numbers** — "Amazon recommendation engine: 35% of total revenue. 2023: $574 billion revenue. 35% = $200 billion recommendations influence chesaay. Billions of interactions daily update chestaay edge weights. Real time."

4. **Indian context** — "Flipkart: 'complete the look' — outfit node lo shirt + pant + shoes connected. Missing item suggest avutundi. Meesho: geographic edges — Vizag customers emi buy chestunnaru. Myntra: Diwali occasion node → festive outfits → product nodes. Same graph, different data."

5. **Advanced uses** — "Return prediction: high-return customer + high-return product → lower recommendation priority. Price sensitivity: customer ₹500-₹1500 range lo buy chestadu → ₹2000 product recommend cheyyadu unless sale lo undi. Graph inventory aware kuda avutundi — out of stock products de-prioritize chestundi."

6. **Bridge** — "Products and customers nodes ga. Next: people and relationships nodes ga. Concall, movie script, management — knowledge graph tho personality analysis. D4 lo."

---

# Caption

```
Shirt buy chesaav. "Customers also bought: pant, belt, shoes."

Idi accident kaadu — idi knowledge graph.

Nodes: products, customers, categories, occasions, brands
Edges: "bought with," "viewed," "similar to," "belongs to"

Graph traverse: shirt → bought_with → pant (strong edge) → belt → shoes → recommend.

Amazon: recommendation engine drives 35% of revenue.
2023 revenue $574B → $200B+ recommendations influence chesaay.

Flipkart: "complete the look" — outfit graph. Missing item suggest avutundi.
Meesho: geographic edges — city-specific preferences.
Myntra: Diwali occasion node → festive outfit recommendations.

Advanced: return prediction, price sensitivity, inventory-aware — anni graph edges.

.
.
.
#ai #knowledgegraph #ecommerce #recommendations #amazon #flipkart #telugu #telugutech
```

# Visual Notes
- Open with Amazon/Flipkart "frequently bought together" section — familiar to everyone
- Graph visualization: shirt node → edges → pant, belt, shoes (weight shown by line thickness)
- Customer node + product nodes + "bought with" edges — growing network as purchases happen
- Amazon stat: "$200B+ influenced by recommendations" — large visual impact
- India grid: Flipkart, Meesho, Myntra logos with their specific graph use case
- Advanced graph: return prediction flow — customer history node → product return rate node → decision
- Tone: relatable. Everyone has experienced this recommendation. Now they know why.

# Sources / Links
- McKinsey "35% of Amazon's revenue from recommendations" — widely cited, McKinsey & Company
- Amazon recommendation system — Amazon Science blog (various papers on collaborative filtering)
- Flipkart "Complete the Look" feature — Flipkart engineering blog
- Meesho tech blog — engineering.meesho.com
- Myntra AI/ML blog — medium.com/myntra-engineering
- Neo4j e-commerce knowledge graph — neo4j.com/use-cases/retail

# Related Notes
- [[21-knowledge-graph-intro]]
- [[22-knowledge-graph-legal-docs]]
- [[24-knowledge-graph-personality-analysis]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

using in Ecommerce if a shirt and pant are bought together we can create entities and add that relation so we can use that data next time someone buys that shirt or pant
