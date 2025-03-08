---
layout: post
title: Decoding Silicon Valley's newest religion
subtitle: The essentials of AI, explained for All
comments: true
mathjax: true
---

Silicon Valley treats AI like a sacred, untouchable force that will change everything.

Yet, for a technology that’s supposed to touch every aspect of society, there’s surprisingly little effort to demystify it for the average person. AI remains a strangely guarded technology, its ascendancy proclaimed by buzzwords, yet its inner workers wrapped in obscurity and its understanding remaining a privilege reserved for the technocrati. 

But for AI to be useful to us all, we need to break through that mystique. Here’s the truth: you don’t need a technical background to grasp the essentials of AI.[^1]

In fact, with just a few intuitive comparisons and everyday examples, you can grasp the fundamentals of AI:

Dr. Seuss and *The Cat in the Hat* helps us understand how the mechanics of how modern large language models work

If you’ve ever looked for a book at a library, you can understand the difference between training a model, finetuning a model, and doing *retrieval augmented generation (RAG)*

You can treat the newest wave of generative AI as *an army of semi-competent interns*

As AI tools become woven into the fabric of our daily lives, understanding how they work is no longer optional. With the right foundation, you won’t be at the technology’s mercy; instead, you’ll be empowered to make smart, intentional use of AI in whatever way serves you best.

---

## Language models versus Google search

*Why is it when I search for something with ChatGPT, it will give me an obviously wrong answer? Google doesn't give me the wrong answer!*

When I first talk about generative AI with many people, the first thing they bring up is the language model's propensity to return incorrect information. Or more accurately, they point to the model's problem with *hallucinating* — the tendency for language models to "make up" information.

And this is because language models don't work in the same way that Google search does.

Google search works by crawling the web, indexing billions of pages, and ranking them based on relevance and authority. When you type in a query, it matches your keywords against this giant index. It’s a process of retrieving *existing information*: finding what’s already out there and giving it back to you, filtered through algorithms trained on relevance signals like backlinks, keywords, and freshness. Slap on a giant advertising engine, and this is the foundation of Google's $2 trillion (and counting) business.

In contrast, language models work by *next-token prediction* — given a word, predict the next word that comes after it. "Next-token prediction" is basically just a fancier way of saying “next-word prediction”.

Try filling in the next word:

*"The cat in the [blank]".*

Most (American/western) audiences will respond with *“hat”*.

And if we kept going?

*"The cat in the hat, by [blank]".*

Most people will fill this in with *"Dr. Seuss"*.

Congratulations, you now understand how modern language models work. 

At its most basic and simplified level, researchers create language models by shoving a huge amount of text data through these models (say, the Internet). These language models will learn statistical correlations between different words, phrases, sentence structures, and more.[^2] The more context (i.e., words) you pass in, the more information and "understanding" the language model will have.

But that's it. Modern large language models are just trained on huge text repositories and predicting the next word that comes along. It just turns out that by doing this, they can mimic human reasoning, answer questions, write code, and demonstrate human-like creativity.

A practical implication of this difference in construction manifests itself in search. 

Some of you may not be old enough to remember this, but when Google (and other search engines) first came out, there was this funny phenomenon where the older generation would search with full sentences.

For example, the youth would type in "weather in palo alto" and others would type in "Google, could you please tell me what the weather is in Palo Alto, California, today? Thank you". Each of these search queries leads to basically the same result, because Google is doing keyword search. In fact, in the early days, the more verbose search would have given you subpar results, because Google hadn't yet implemented catches to process keyword search with complete sentences.

However, in the current age of LLMs, it's actually beneficial to have longer search queries with more context: "facts about LeBron James, focusing on the timeline of how he built his outside-NBA business empire, so that I can learn how to build a business as a professional athlete" trumps "facts about LeBron James" every time. But, the last twenty years of using Google has trained us away from this laden LLM search.

Now, the younger, AI-native generation will point their fingers and laugh at the Google-native generation for their lack of technology skill. History truly comes full circle.

So, the reason that Google and ChatGPT require different modes of interaction and return such different types of answers is because they represent two different technical approaches. It's two fundamentally different paradigms: retrieval/search (Google) v. next-token generation (LLMs). And once you understand that, you can begin to see why language models might have some of the strengths and weaknesses that they have.

---

## Larry Linguistic Maximus — Training v. finetuning v. retrieval-augmented generation (RAG) v. prompt engineering

One of the most common applied tasks for LLMs (and AI models in general) is figuring out how to improve their performance. To answer this, researchers and technical folks will throw around terms like prompt engineering, training the model, finetuning the model, or performing RAG. But what does any of this all mean? 

I know that AI safety researchers would caution me from anthropomorphizing these language models, but it's often the easiest way to build intuition for how they work.

Imagine we have an eager college intern, Larry Linguistic Maximus (L.L.M. for short). Like most studious students, Larry loves learning at the library.

<figure>
  <img src="/assets/img/princeton_library.jpg" width="100%">
  <figcaption>A gorgeous library at the Institute for Advanced Studies in Princeton, NJ.</figcaption>
</figure>

If we wanted Larry to be a generalist and "get good at business", we could **train** him by forcing him to read every single business textbook, business biography, and Harvard Business School case study that exists. It would probably be prohibitively time-consuming and expensive to do this, but it would be possible.

Perhaps we want Larry to answer questions about a particular product to assist our sales team. Then we might give Larry a set of relevant product documentation; when the sales team asks him a relevant question, Larry would search the documents for the right information, and then answer based on the synthesis of the documents. This is **retrieval-augmented generation (RAG)**.

Maybe we want Larry to specialize in reading legal documents and finding particular types of contract clauses. We would spend some time finding legal documents, identifying the relevant contract clauses for these documents, and have Larry figure out the patterns himself. From our initial selection, Larry is **finetuning** his ability to identify these contract clauses.

And if we want Larry to do anything better, he would certainly benefit from clearer instructions and more context about the task at hand. We would then take it upon ourselves to give him better, higher quality instructions that result in better work — that's **prompt engineering**.

If you take these intuitive analogies, you can actually roughly figure out the relative cost and difficulty between each of these approaches:

- **Prompt engineering** (give Larry better instructions) is *very easy*, takes *hours* to implement, and is basically *free*.
- **Retrieval augmented generation** (give Larry a reference guide) is *easy*, takes *days* to implement, and is relatively *cheap*.
- **Finetuning** (have Larry memorize a library section) is *harder*, takes *days to weeks* implement, and is *expensive*.
- **Training** (force Larry to memorize the entire library) is the *hardest*, takes *weeks to months* to implement, and is *extremely expensive*.

Furthermore, our Larry Linguistic Maximus analogies allow us to realize that these model improvement techniques aren't mutually exclusive, and we can imagine combinations of the techniques.

When Larry specializes in identifying relevant contract clauses, we could give him better instructions after he learns how to extract the clauses from the legal documents, combining *finetuning* with *prompt engineering*. 

We could re-train Larry entirely (*training*) and give him different documents to reference (*RAG*) while he does another task.

Having these human-like analogies allows you to think about the strengths and weaknesses of these approaches — time, cost, architecture decisions. Most importantly, it allows some semblance of an intuition for non-technical stakeholders.

---

## Find the correct job for the AI

*But Nick, when I give a person a book to look up particular facts, they won't forget that information nearly as quickly as an LLM. My five year old doesn't even have this problem. Why is that?*

Now here's one area where we get in trouble for anthropomorphizing AI and LLMs. 

AI is really, really good at doing many things that people are bad at — and that's often magical. AI is also really, really bad at doing certain things that people are good at — and that's often infuriating.

AI tools exhibit what Ethan Mollick coins the ["jagged frontier"](https://www.oneusefulthing.org/p/centaurs-and-cyborgs-on-the-jagged?open=false#%C2%A7inside-the-jagged-frontier):

> Imagine a fortress wall, with some towers and battlements jutting out into the countryside, while others fold back towards the center of the castle. That wall is the capability of AI, and the further from the center, the harder the task. Everything inside the wall can be done by the AI, everything outside is hard for the AI to do. The problem is that the wall is invisible, so some tasks that might logically seem to be the same distance away from the center, and therefore equally difficult — say, writing a sonnet and an exactly 50 word poem — are actually on different sides of the wall. The AI is great at the sonnet, but, because of how it conceptualizes the world in tokens, rather than words, it consistently produces poems of more or less than 50 words.  Similarly, some unexpected tasks (like idea generation) are easy for AIs while other tasks that seem to be easy for machines to do (like basic math) are challenges for LLMs.

This concept of a jagged frontier highlights the unpredictable nature of AI capabilities. It's not a smooth progression from easy to difficult tasks, but rather a complex landscape of strengths and weaknesses. Recognizing this pattern can help us approach AI more effectively, much like how we approach **human** talent.

When we interview a person for a job, we don't fixate on their inability to perform tasks outside their expertise or experience. We don't disqualify a software engineer because they can't recite Shakespeare, or dismiss a graphic designer for their lack of knowledge in quantum physics. Instead, we focus on their strengths, their potential, and how their skills align with the job requirements.

**We evaluate people based on what they can do, not on what they can't**. There are always trivial questions that can make someone look bad or highlight their weaknesses, but that's not the point of an interview. The goal is to find the right fit – a person whose strengths and abilities match the needs of the role.

As Nicholas Carlini [points out](https://nicholas.carlini.com/writing/2024/how-i-use-ai.html#fix):

> In the same way I wouldn't write off humans as being utterly useless because we can't divide 64 bit integers in our head — a task completely trivial for a computer — I don't think it makes sense to write off LLMs because you can construct a task they can't solve. Obviously that's easy — the question is can you find tasks where they provide value?

AI is that brilliant, yet hilariously incompetent intern — we need to spend time figuring out what is the right task to maximize its abilities.

When working with these tools, figure out what AI tools can do, and focus on that.

Can you find tasks where AI tools provide value? I bet you can.

---

## Riding the exponential wave

People are really bad at intuitively understanding exponential growth. [I’ve written about this time and time again](https://nicholasachow.substack.com/p/musings?open=false#%C2%A7focus-on-what-you-can-control-less-is-more), but humans are really bad at non-linear growth.

Technology is a story of exponential growth, and AI is no different.

We don’t exactly have a Moore’s law equivalent in AI (yet), but I’m sure there are a few candidates for exponential curves in AI: 
- training costs
- model size
- benchmark performance
- cost of inference (i.e., running these models)

And just like for other technological trends, if you decompose the overall exponential growth curve, you might find that it’s because of a bunch of simultaneous improvements.

Let’s think about the cost of inference, and how much conceivably it could improve a lot. Let’s just talk about some of the model-specific optimizations:

- *model architecture*: designing smarter models that require less computation, speeding up inference without sacrificing accuracy
- *model distillation*: compressing a large model’s knowledge into a smaller one, keeping the intelligence while shedding the excess weight
- *model pruning*: trimming unnecessary parameters from a model to make it leaner and faster
- *model parallelism*: sometimes, running smaller models in parallel will outperform a singular, more powerful model
- *quantization*: reducing the memory footprint of a model allows it to run faster

Astute readers will realize that I haven't even talked about all the hardware improvements (e.g., Nvidia's GPU factory). You could break this down to even more elements: inference optimizations, deployment optimization, data-level optimizations, etc. And each of these topics has numerous subtopics, each subtopic of which has dedicated armies of PhD researchers.

Then there’s other exogenous factors, like how many VCs are shoveling money into this space and subsidizing all the spend on GPUs and other hardware. 

But multiply all of these small improvements together, and you get something that looks closer to exponential improvement of inference writ large.

This holds for all the different performance curves: the sum is greater than its parts. AI improvement is exponential because improvements are multiplicative.

It's less crucial to understand exactly how model distillation or tensor calculation optimization works, but more crucial to understand how they fit together.

---

## AI is a lever, not the product

This is basically a combination of two earlier pieces I wrote ([here](%post_url 2024-03-21-ai-lever) and [here](%post_url 2024-06-05-three-levers)), but I think the ideas are extremely important.

In a rapidly evolving landscape, it’s critical to understand whether your company is **AI-native** or **AI-augmented**. AI-native companies — like OpenAI or Anthropic — sell AI as their core product. In contrast, AI-augmented companies integrate AI to make their existing products more effective and efficient.

The distinction matters: AI-native companies are built to deliver AI technology, while AI-augmented companies use AI as a **lever** — a force multiplier — not the end goal. Unfortunately, many AI-augmented companies fall into the trap of pretending they’re AI-native.

A cautionary tale: Alfred, the CEO of a startup, tells his team to “add AI” into their product after seeing flashy AI demos on social media. His company hires top researchers, shifts resources, and pours millions into new AI features. But a year later, there’s little to show—because Alfred misunderstood AI’s role. **Throwing AI at a product won’t work without intentional strategy.** As Archimedes said, “Give me a place to stand, and I shall move the world.” AI can be powerful — but only if it’s rooted on top of a strong fulcrum, like your product or operational workflow.

AI creates value by acting as a lever across three areas:

1. **Product Leverage**: AI enhances existing features or dramatically improves cost structures. Examples include semantic search, which understands user intent to deliver relevant results, and malleable content, where LLMs dynamically adjust the tone, complexity, or format to meet user needs in real-time. Similarly, multimodal inputs allow seamless interaction across text, voice, and images, opening new frontiers for creative and educational applications. In all these cases, AI augments the core product to deliver a more personalized, intuitive experience.

2. **Operational Leverage**: AI can streamline workflows, automate routine tasks, and reduce operational costs. LLM-based chatbots, for example, efficiently handle customer inquiries. AI also speeds up processes like HR resume screening, financial reporting, and lead generation. These applications free employees to focus on higher-value work, ensuring the organization runs faster and leaner.

3. **Individual Leverage**: For knowledge workers, AI tools act as powerful allies. AI-driven enterprise search engines provide faster, more relevant answers than traditional tools, while prompt engineering lets individuals extract immense value from general-purpose LLMs like ChatGPT. However, not every AI tool is worth adopting — if ChatGPT (plus prompt engineering) can replicate 80% of a new tool’s features with the right prompts, there’s no need to waste time or money. The key is experimentation: keep testing tools, and adopt only the ones that provide real, meaningful leverage.

Contrary to what countless Twitter demos would suggest, AI’s power lies not in flashy features but in thoughtful, well-integrated solutions. Successful AI-augmented companies focus on how AI improves the customer’s experience rather than chasing trends. Teams that succeed with AI make opinionated design choices rooted in customer needs, understanding where AI fits into the product or process.

As mentioned earlier, Jeff Bezos often says that the better question is not, "What will change in ten years?" but, "What will stay the same?" No matter how advanced AI becomes, the fundamentals remain: **People have problems, and products exist to solve them.** AI only adds value when it aligns with that purpose.

So, don’t think of AI as the product — it is the lever. Focus on building great products, identify where AI can enhance or streamline, and implement deliberately. The companies that thrive will be those that treat AI as a tool, not the entire solution.

---

[^1]: AI in its broadest sense has been around since the 20th century.  When I say “AI” I mostly mean generative AI (generating data from a distribution, starting from GANs) — if you know what I’m talking about here, I know you’ll likely have your own definition of what’s AI v. ML v. generative AI.
[^2]: For a technical introduction, look at [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/).