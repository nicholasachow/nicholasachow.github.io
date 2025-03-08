---
layout: post
title: "The three key levers of AI: product, operations, and you"
subtitle: Can AI turbocharge your entire business, not just your product?
comments: true
mathjax: true
---

I've written about [how to build AI products]({% post_url 2024-03-21-ai-lever %}) and the core part argument is that **AI is the lever, not a product**. In this way, I’ve implicitly argued that AI is a product lever — its unique capabilities allow for the existing product to be a better version of itself.

It turns out that there are multiple areas of an organization where AI can provide leverage, not just on top of the existing product. They are:

1) Product leverage
2) Operational leverage
3) Individual leverage

---

## Product leverage

> Your existing product is the fulcrum that the AI lever sits on. AI can augment valuable product features or dramatically improve the product's cost structure.
> 
> — [How to build great AI products]({% post_url 2024-03-21-ai-lever %})

There's far too many specific generative AI design patterns and features to cover comprehensively, but here are a few:

### Semantic search

While it has existed for a while, semantic search has been turbocharged by these new LLMs. Semantic search is an advanced search technique that understands user intent and contextual meaning to deliver more accurate and relevant results — said another way, it allows search algorithms to understand plain English. It's a tremendously effective way to improve the user experience because it allows for more precise answers to their queries. Furthermore, semantic search is often one of the quickest drop-in implementations to a new product because there are so many libraries that allow for swift semantic search deployment.

As an aside, it's also quite interesting to see the potential shift back in search queries. Remember when older generations used to ask Google in full sentences, "What is the weather in San Francisco, California today?" until they were cajoled into simply typing "SF weather"? Semantic search and LLM search puts us back into the situation where a more descriptive natural language formulation will give us better answers.

For example, "Tell me more about the movie that has the scene where the Joker creepily claps in the prison cell?"

<iframe width="560" height="315" src="https://www.youtube.com/embed/Alk2ixHGLto?si=A1qsnzoRSYeBpIuP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Malleable content
I think that LLMs are propelling us towards the tipping point of content customization and interactivity, something I call "malleable content." With LLMs, we can dynamically reformat content to match individual preferences and needs, creating personalized experiences like never before.

When a user requests information, LLMs tailor the content in real-time, adjusting the format, tone, and complexity based on the user's context and preferences. For instance, a single piece of content can be condensed into a concise summary for quick reading, expanded into an in-depth analysis for thorough understanding, or converted into a conversational format for interactive engagement. This level of customization not only enhances user experience but also increases the accessibility and relevance of information, effectively meeting diverse user demands.

Think of summarization as content compression and the command "explain this" as content expansion. With LLMs, content becomes instantly malleable and customizable, reflecting a profound shift in how we interact with information.

And of course, content malleability isn't just constrained to the domains of text and LLMs, but also audio, video, and text with multimodal models.

### Multimodality

Multimodality, which combines text, voice, and image inputs, represents another frontier in AI product leverage. By allowing a product to accept and process various forms of input, AI can create a more seamless and intuitive user experience.

Imagine a scenario where an artist can describe their vision using voice, sketch it with a stylus, and supplement it with reference images, all within the same platform. What about a language learner who practices pronunciation via voice input, reads along with text, and receives visual aids to reinforce vocabulary? Multimodality not only broadens the scope of interactions but also paves the way for innovative applications, from immersive educational tools to sophisticated creative platforms.

They say a picture is worth a thousand words (so then videos are worth a million words?), so here are some of the OpenAI GPT-4o release videos to get a better sense of multimodality:

<iframe width="560" height="315" src="https://www.youtube.com/embed/rKp36MmRlXA?si=SXcQBLOLG77Ks1YJ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/WzUnEfiIqP4?si=Q9E_zojLQzicgXoV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/MirzFk_DSiI?si=hoo10yz221uxnTVV" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### The future of AI product design
One of the most intriguing aspects of leveraging AI in product design is the nascent stage of many design principles. As AI technology continues to evolve, many best practices remain to be discovered. For example, generative AI often encounters the "blank slate" problem, where users are overwhelmed by too many choices, leading to decision paralysis.

Crafting AI systems that offer helpful guidance without overwhelming users is an ongoing challenge. The non-deterministic nature of AI is both a strength and a limitation. It enables dynamic and adaptable interactions but also means that the system may not always produce consistent results, which can be problematic in certain applications.

---

## Operational leverage

The operational lever of AI focuses on streamlining processes and workflows outside the core product value proposition, making them cheaper and faster. By automating routine tasks and optimizing operations, AI can significantly enhance an organization’s overall efficiency. This includes streamlining customer service interactions, automating HR resume screening, generating customer leads, and managing finance and accounting tasks. With AI handling these processes at greater speed and accuracy than humans, organizations can achieve substantial cost savings and productivity improvements.

In customer service, for example, AI chatbots can manage a large volume of inquiries simultaneously, providing instant responses and resolutions to common issues. Personally, if it means that I don't have to navigate through a labyrinth of phone redirects, be placed on hold for two and a half hours, and then curse the airline gods when their system unceremoniously boots me off the line, then [I, for one, welcome our AI (customer support) overlords](https://observer.com/2016/08/i-for-one-welcome-our-ai-overlords/).

Similarly, in HR, AI can expedite resume screening by swiftly identifying candidates who meet the required qualifications, thereby accelerating the hiring process and ensuring the best candidates are considered. I used to think that the "human touch" was essential for selecting resume screen candidates, and then I learned that recruiters spend an average of negative three minutes on each resume. I'm sure that AI will be better that this (and then allow recruiters to work on more interesting downstream tasks).

There's a bunch more examples — financial reporting, expense tracking, invoice processing, customer lead generation, analytics, etc. — but I think you get the idea.

While these applications of AI might seem straightforward, their impact is significant. The most common recent example is [Klarna’s AI-driven chatbot reportedly generated $40 million in business value by automating customer service functions](https://www.klarna.com/international/press/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month/). Even though the skeptic in me thinks the company generated a disproportionate amount of hype around this one AI feature in preparation for their IPO (to get that sweet, sweet AI valuation premium), I find it difficult to argue with $40M in cost savings.

Of course, the lines between product leverage and operational leverage can sometimes blur. For instance, if an AI tool improves a core data pipeline and halves product latency, it could be seen as a hybrid product lever and operational lever. It's not always a perfect categorization, but distinguishing between the two is generally useful for understanding and strategizing AI implementations.

Finally, companies need to weigh the "buy versus build" tradeoff when integrating AI. Everyone in Silicon Valley is building some specialized AI module for some function, which means there's an incredible amount of noise. However, it is still crucial to assess whether it’s more cost-effective and efficient to build an in-house solution or buy an existing one. This decision can significantly impact the speed and success of AI adoption within the organization; unfortunately, it's still an open problem yet to be solved.

---

## Individual leverage

In knowledge work, there's an oft-repeated adage: "All the assets leave the building at the end of the day and come back in the morning."

In many of our industries today, human capital is the primary asset. Therefore, these people can gain substantial leverage from AI technologies that enhance their productivity and capabilities. The final form of AI leverage, individual leverage, focuses on the tools and workflows tailored for individual contributors, enabling them to perform their tasks more effectively and efficiently.

One of the most obvious individual AI levers is enterprise search, which allows employees to retrieve information from their data quickly and accurately (using semantic search, remember that?). AI-driven search engines like Perplexity provide more nuanced and contextually relevant results compared to traditional search engines like Google. In addition to AI-first search engines like Perplexity, there are also more and more vertical-specific search engines popping up: they tailor their algorithms to meet the unique needs of different industries, providing specialized and actionable insights. This is particularly valuable in fields such as medicine, law, or finance, where access to precise and reliable information is crucial.

However, it's still incredibly early in this individual leverage space. There are a ton of very interesting projects popping up, and it's unclear which ones will be useful enough to merit a lot of work. If I spent a dollar on every interesting AI software tool that I saw, I would be filing for bankruptcy by the end of the week.

One general heuristic that I urge people to use: if you see a new piece of cool AI software show up, there's a 99% chance you can replicate 80% of its functionality using ChatGPT and prompt engineering. It doesn't take that long to verify that, and it's important to keep experimenting with different tools and technologies.

If it's interesting enough and your prompt engineering can't get you to where you want, then think about buying the tool.

Otherwise, don't. Your wallet will thank you.

---

As we navigate this AI-driven transformation, it's crucial to maintain a balance between automation and the human touch. AI can handle repetitive, data-driven tasks with remarkable efficiency, but the creative, strategic, and empathetic aspects of work still thrive under human stewardship.

[This balance ensures that while AI optimizes processes, human ingenuity continues to lead the way in innovation and complex problem-solving](% post_url 2024-03-21-ai-lever %).

[The journey to fully leverage AI is akin to a multi-armed bandit problem. We must experiment, learn from each pull, and iteratively refine our approach to discover the most rewarding strategies](https://nicholasachow.substack.com/p/how-to-solve-the-game-of-life).

Success lies not in a single pull, but in the cumulative wisdom gained from continuous exploration and adaptation.