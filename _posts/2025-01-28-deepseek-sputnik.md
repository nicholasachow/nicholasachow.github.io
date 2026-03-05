---
layout: post
title: "The DeepSeek r1 model: AI's Sputnik moment?"
subtitle: "How a low-cost, high-performance model from China sparked panic, and what it means for AI"
---

I woke up today to Nvidia's stock price down something like 20%.

But it wasn't just Nvidia, but the tech market writ large.

It didn't take me long before I found out it was because of DeepSeek, a Chinese AI research arm spin-off from a quantitative hedge fund.

Last December, the DeepSeek team released their newest AI reasoning model, **DeepSeek r1**; for some reason, Mr. Market decided to go ballistic over the news today.

It reminds me of the old Ben Graham/Warren Buffett adage:

> "In the short run, the market is a voting machine, but over the long run, it's a weighing machine."

Right now, the *voting machine* side is in full force: we've seen markets react violently (mostly in the negative).

I have some assorted thoughts (obviously none of this is investment advice).

---

## tl;dr

The DeepSeek team has pulled off a remarkable engineering feat in building their r1 model. They've combined a variety of hard-won AI research insights — from low rank approximations to multi-token prediction — and delivered a highly cost-efficient approach to training and inference.

* The oft-cited **$6M in training costs** is just the incremental *final run* cost. Under the hood, there's a massive R&D expense of prior experiments, infrastructure, and the "art" of knowledge-distillation.
  * Their 10x cheaper performance benchmark (v. a similar Facebook model) *is* impressive.
* Distillation is a key piece of their puzzle. It's a reminder that **you can't replicate or "distill" a strong model without access to other powerful models**.
* There are so many ways to improve AI inference, and they are all multiplicative: **DeepSeek's r1 model shows the way to improve a bunch of different levers at once, and you have an enormous system level improvement**.
* The markets took a whole month (since DeepSeek's December 26 announcement of their V3 model, which the r1 model was based off of) before reacting, which is striking in itself.
* American AI research dominance has its rude awakening — will this be its Sputnik moment?

Yes, DeepSeek's r1 model is a big deal.

No, it's not going to make every existing AI model obsolete tomorrow.

But it *does* underscore that engineering creativity in AI is alive, well, and more international than many realize.

---

## Ideas

1. **Capital-efficient frontier AI:** DeepSeek demonstrates that building near state-of-the-art models doesn't *have* to require gargantuan training bills. They used many known techniques (FP8 vs. FP32, low rank approximations for KV caching, multi-token prediction) — but the magic is in how those techniques are combined to drastically lower the cost of training their model.

2. **Distillation as an art:** this model underscores an important fact: you can compress knowledge from bigger models if you do it *well*. DeepSeek (probably) leveraged multiple powerful teacher models, and the refined result shows up in r1's performance.

3. **Many levers of AI improvement:** As I've often noted, improvements in AI aren't *always* about one big architecture change. A bunch of smaller, orthogonal enhancements can yield a multiplicative effect. DeepSeek's r1 is a real-world case study of that principle.

---

## Deeper dive

### The $6M "training cost" nuance

When people point to DeepSeek's r1 and exclaim "It only cost $6M to train this model — US AI production is screwed!", they're glossing over some key nuance:

* **Incremental vs. total cost:** that $6M is just the incremental cost for the final, public-facing run. It doesn't include the countless hours of testing, ablation studies, and experiments leading up to that final push.

* **A 10x cost reduction:** even so, achieving a 10x cost improvement over a similarly capable Meta model is impressive. That said, it's not a magical free lunch — it's the culmination of strategic application of known research insights plus a few novel twists from the DeepSeek team.

### Distillation done right

Distillation is the process of taking a large model's outputs and teaching a smaller model to mimic them. In practice, it can get tricky fast:

1. **You need a powerful teacher (model):** if you don't already have access to highly capable models, your distillation can only go so far. DeepSeek likely leveraged multiple large-scale models to teach its own models (e.g., ChatGPT, Baidu's models, etc.).

2. **It's part science, part art:** tuning distillation objectives and data pipelines requires a deep blend of theoretical understanding and empirical tinkering. When done *really* well, you can get a smaller (and cheaper) model that still performs near the level of its bigger teachers.

Early glimpses of DeepSeek r1 responses sometimes revealed interesting footprints of other models — a little revelation into the training process.

---

## Other relevant reads

* [DeepSeek-V3 Technical Report](https://arxiv.org/pdf/2412.19437): the original technical paper released by the company

* [How has DeepSeek improved the Transformer architecture?](https://epoch.ai/gradient-updates/how-has-deepseek-improved-the-transformer-architecture): great read on many of the implementation details

* [DeepSeek V3 and the actual cost of training frontier AI models](https://www.interconnects.ai/p/deepseek-v3-and-the-actual-cost-of)

* [*Fire-Flyer AI-HPC: A Cost-Effective Software-Hardware Co-Design for Deep Learning*](https://arxiv.org/pdf/2408.14158v1): An older paper that DeepSeek published on its AI training and inference infrastructure
