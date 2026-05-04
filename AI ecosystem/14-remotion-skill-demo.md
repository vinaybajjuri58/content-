---
title: Remotion Skill Demo — AI Generates Motion Graphics Using a Skill
phase: AI ecosystem
topic: tool calling, skills, remotion, motion graphics, automation
format: reel
status: draft
scheduled:
tags: [ai, tool-calling, skills, remotion, motion-graphics, automation, workflows]
related: ["[[13-customer-support-tool-demo]]", "[[15-tools-gone-wrong]]", "[[AI Ecosystem Index]]"]
week: 3
day: 5
category: ai
---

# Hook
> AI ki "IPL standings animation create cheyyi" antey — 30 second motion graphic output vachindi. Tool call chesinda? Kaadu. Skill call chesinda.

# Core Idea
_A Skill is a pre-packaged chain of tools that AI can call as a single unit. Where a tool does one thing (search web, create file), a skill orchestrates multiple tools together to produce a complex output. Remotion is a JavaScript library for generating videos programmatically — when exposed as a skill, AI can generate motion graphics without a human touching a design tool._

---

# Details
_Research & facts to write a better script from_

## Tool vs Skill — The Distinction

**Tool:** A single callable function. One input, one output.
- `search_web("IPL standings 2024")` → returns search results
- `create_file("animation.tsx")` → creates a file
- `run_terminal("npx remotion render")` → runs a command

**Skill:** A bundled chain of tools, exposed as one callable unit. Takes a high-level intent, executes multiple steps internally.
- `create_motion_graphic(topic="IPL standings", duration=30, style="modern")` → returns a video file
- Internally: writes React/Remotion code → fetches live data → configures animation → renders video → exports file
- From the AI's perspective: one call. Internally: 5-6 tool calls orchestrated.

This distinction matters: tools = primitive actions. Skills = composed workflows. Week 7 (Workflows) will go deeper on this.

## What Remotion Is
- Remotion is an open-source JavaScript/React library for creating videos programmatically
- Instead of dragging elements in Premiere Pro, you write code: position, timing, animation are all code
- This makes video creation automatable — an AI can write Remotion code to produce a video
- Founded by Jonny Burger (2021), used by companies for programmatic video generation (personalized ads, data visualizations, automated explainers)
- Key advantage: if you change the data (e.g., new cricket scores), re-running the same code produces an updated video automatically

## How AI + Remotion Skill Works

Step by step when AI receives "create a 30-second animation about compound interest":

1. `parse_intent` — AI understands: topic = compound interest, duration = 30s, format = explainer animation
2. `fetch_data("compound interest formula, growth table")` — web search or database tool for numbers to animate
3. `write_remotion_code(topic, data, duration)` — AI writes the React/Remotion component (code tool)
4. `validate_code(file)` — check for syntax errors (read tool + linter tool)
5. `run_renderer("npx remotion render Animation --output output.mp4")` — terminal tool executes the renderer
6. `return_file("output.mp4")` — delivers the final video file to the user

Total: 6 tool calls, packaged as one "create_motion_graphic" skill.

## Why This Matters for Content Creators
- A Telugu creator making daily content can instruct an AI to produce animated explainers without knowing design or code
- Data-driven animations: AI fetches live data (market stats, cricket scores, election numbers) and animates them automatically
- Template once, regenerate endlessly — same animation structure, different data
- This is the beginning of AI-first content production pipelines

## The Skills Ecosystem
- Claude supports "tools" via MCP — skills can be built on top as higher-order MCP servers
- GitHub Copilot Workspace uses a similar skill architecture for multi-step coding tasks
- OpenAI's "Actions" in GPTs are effectively skills — a packaged sequence of API calls behind one button
- The trend: from individual tools → skills → fully automated workflows (Week 7) → autonomous agents (Week 8)

---

# Breakdown
_Reel script_

1. **Hook** — "AI ki 'IPL standings ka 30-second animation banao' antey — output: motion graphic video. Oka tool call chesinda? Kaadu — skill call chesinda. Difference teluskuntama."

2. **Tool vs Skill** — "Tool: oka function. Search web. Create file. Run command. Single action. Skill: multiple tools oka package lo. High-level intent ivvandi — internally anni steps run avutayi, final output vostundi."

3. **Remotion explain** — "Remotion ante JavaScript library — videos code tho create cheyyadam. Premiere Pro lo drag drop kaadu — code rasthe video avutundi. Idi AI ki perfect — AI code rayyagaladu, code run chesthe video ready."

4. **What happens step by step** — "AI 'compound interest animation' ani vinnappudu: data fetch chesindi, Remotion code rasindi, renderer run chesindi, video output chesindi. Meeru chusedi: oka prompt → oka video. Actually jarigindi: 6 tool calls."

5. **Why it matters** — "Content creators ki idi game changer. Live data fetch → animate → publish. Cricket scores, stock prices, election results — oka template, data change avvanga automatic ga new video. Design knowledge lekundane."

6. **The bigger picture** — "Tool → Skill → Workflow → Agent. Idi progression. Oka skill oka workflow lo part avutundi. Week 7 lo manam full automation workflows chudatamu. D6 lo — idi wrong ga configure chesthe emi avutundo."

---

# Caption

```
AI ki "IPL standings animation create cheyyi" antey — 30 second motion graphic vachindi.

Tool call kaadu — Skill call.

Tool: oka function. Skill: tool chain — fetch data → write code → render → export video.

Remotion: videos code tho create cheyyadam. AI code rayyagaladu. So AI + Remotion = motion graphics on demand.

Content creators ki: oka template, live data, auto-generate. Design knowledge lekundane.

Tool → Skill → Workflow → Agent. Idi progression. Week 7 lo full automation.

.
.
.
#ai #remotion #toolcalling #skills #contentcreation #telugu #telugutech #automation
```

# Visual Notes
- Open with the finished animation playing (IPL standings or similar — something visually impressive)
- Show the "one prompt → video" moment
- Then pull back: show the tool chain that ran underneath
- Tool vs Skill diagram: tool = single box, skill = multiple boxes chained together → one output
- Remotion code snippet briefly visible — then video output from the same code
- End: tool → skill → workflow → agent progression diagram (teaser for upcoming weeks)

# Sources / Links
- Remotion — remotion.dev — programmatic video with React
- Jonny Burger — Remotion founder
- Claude MCP tool use — Anthropic documentation
- OpenAI GPT Actions — packaged API call sequences

# Related Notes
- [[13-customer-support-tool-demo]]
- [[15-tools-gone-wrong]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_
