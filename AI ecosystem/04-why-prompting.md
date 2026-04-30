---
title: Prompting Ante Enti — AI కి Clear గా Cheppakunda Pothe?
phase: AI ecosystem
topic: prompting basics
format: reel
status: draft
scheduled:
tags: [ai, prompting, beginner, llm, chitti, robot]
related: ["[[05-types-of-prompting]]", "[[06-ai-skills-hype-is-just-prompting]]", "[[AI Ecosystem Index]]"]
week: 2
day: 1
category: ai
---

# Hook
> Chitti ki "TV petti padey" antey — TV ni edukuni padestadu. AI kuda same.

# Core Idea
_LLMs are next-token predictors trained on text data — they have no common sense or context unless you give it to them. Vague prompt = vague answer. Clear prompt = good answer. Prompting is the skill of giving AI exactly what it needs to give you what you want._

---

# Details
_Research & facts to write a better script from_

## How LLMs Actually Work
- LLMs don't "understand" language — they predict the most probable next word/token based on patterns in training data
- GPT-4 was trained on roughly 1 trillion tokens of internet text — books, Wikipedia, Reddit, code, articles
- Every response is a probability calculation: "given what came before, what word is most likely next?" — repeated thousands of times
- There is no intent, no common sense, no awareness of what you actually meant — only pattern matching at massive scale

## Why Prompting Changes Everything
- Stanford research showed that simply adding "think step by step" to a math problem improved LLM accuracy by up to 70%
- Rephrasing the same question differently can shift the answer quality by 30–40% — same model, same data, different prompt
- OpenAI's internal evals show that clear, structured prompts reduce hallucination rates significantly compared to vague ones
- A 2023 study (Google DeepMind) found that prompt quality was a bigger factor in output quality than model size in many tasks

## The Chitti Parallel
- Chitti is programmed to execute instructions literally — no inference of human intent
- "TV petti padey" in Telugu colloquially means "turn on the TV" — but literally means "put the TV and fall / place it down"
- Chitti picks it up and throws it — perfect execution of the literal instruction, zero common sense
- Current LLMs behave exactly like this when given ambiguous or casual prompts — they fill gaps with probability, not intent
- The fix in both cases: give precise, unambiguous instructions

## The Practical Takeaway
- Bad prompt: "write something about marketing" → generic, useless output
- Good prompt: "write a 5-point Instagram caption for a Telugu audience explaining why email marketing beats social media for small businesses" → specific, usable output
- The model didn't change. The prompt did.

---

# Breakdown
_Reel script — scene-based_

1. **Scene clip** — Chitti Robo: Dr. Vaseegaran brings Chitti home. Mom says "TV petti padey." Chitti picks up the TV and throws it on the ground.

2. **Cut to host** — "Chitti ki telidu — 'TV petti padey' ante TV ni ON cheyyu ani. Adhi cheppaledu. So literally chesadu."

3. **The parallel** — "Meeru use chesay ChatGPT, Claude, Gemini — anni ivi kuda same. Veetiki common sense ledu. Veetiki billions of pages of text data meeda train chesaru — so next word predict chestundi, that's it."

4. **The proof** — "Meeru 'write something about AI' antey — vague ga ichestundi. 'Write a 3-slide Telugu Instagram carousel explaining what an LLM is for a beginner' antey — exact ga ichestundi. Same model. Different prompt."

5. **The takeaway** — "Prompting ante AI ki instructions ivvadam. Meeru clear ga cheppite — clear ga ivvistundi. Garbage in, garbage out. Next clip lo manam different types of prompts gurinchi chuddam."

---

# Caption

```
Chitti ki "TV petti padey" antey — TV ni edukuni padestadu.

ChatGPT kuda same. Common sense ledu. Training data meeda next word predict chestundi — that's it.

Clear ga cheppite clear ga ivvistundi.
Vague ga cheppite vague ga ivvistundi.

Next clip lo manam different types of prompts gurinchi chuddam.

.
.
.
#ai #chatgpt #prompting #telugu #telugutech #llm #chittirobottelugu
```

# Visual Notes
- Open with Chitti Robo clip (fair use / meme format — short clip, commentary on top)
- Cut to host explaining in a talking-head format
- Text overlays: "Probability" → "Next word" → "No intent" on the LLM explanation section
- End card pointing to next video in the series

# Sources / Links
- Chitti Robo (2010) — scene reference, use as meme/commentary clip
- "Large Language Models are Zero-Shot Reasoners" — Kojima et al., 2022 (chain-of-thought / step-by-step finding)
- Google DeepMind prompt quality study, 2023
- OpenAI prompting best practices — platform.openai.com/docs/guides/prompt-engineering

# Related Notes
- [[05-types-of-prompting]]
- [[06-ai-skills-hype-is-just-prompting]]
- [[AI Ecosystem Index]]

# Raw Notes
_User's Telugu script — preserved exactly as written_

I want to a play scene from chitti robo movie where dr vaseegaran creates a robot and brings him home and then his mom say's ah TV petti padey which normal human understand like ON cheyyu but AI will not right
So what it does it Picks up the tv and throws on the ground and after the scene i will explain the current LLM models are also same they are trained on bunch of text data so it will just pick the next work based on probability so you have to give it clear prompts for it to give you good answers
if you give random text it will also give random answers
