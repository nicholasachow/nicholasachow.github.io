---
layout: post
title: "How to solve the game of life"
tags: [life]
---

*I'm revisiting a concept that I introduced originally as part of my musings: formulating life as a multi-armed bandit problem.*

*I think it's even more relevant in the volatile macroeconomic climate today, so I've been thinking more about this.*

---

The first time I visited Las Vegas, I was shell-shocked. My ten-year-old brain didn't understand how to process the cacophony of noise and drunken revelry on the Las Vegas Strip, where it was intermixed with all sorts of extraordinary sights and smells.

What was more shocking, though, were the hotel casinos. One night, as my parents quickly shuttled my brother and me from our hotel room to the restaurant, we walked through the hotel's casino. I remember the dizzying array of flashing lights and the noxious miasma of cigarette smoke. Still, for some reason, I was captivated by the circles of people sitting around the poker table and the throngs of people sitting in front of the slot machines.

Since then, I've been fascinated by casino games. Each game has incredible knowledge and insight you can learn, but only if you pay attention. Poker is an excellent lesson in human psychology and disciplined risk-taking. Blackjack is an exercise of patience and good decision-making. But the most important life lessons can be learned from slot machines.

Slot machines are an apt analogy for life.

Slot machines are often called "multi-armed bandits" because they effectively steal money from people. But, we can use the idea of slot machine games to learn something profound about life.

Life can be cast as a multi-armed bandit problem: you have a wealth of slot machines (different disciplines, activities, and experiences) to try and a limited budget (time, money, energy, etc.) Every decision you make can be construed as pulling a lever on a slot machine, and the result is the payoff.

This is a remarkably beautiful model for life, as it allows you to decompose life into a sequential decision-making process.

There's an exceedingly rich mathematical literature focused on these multi-armed bandit problems, and researchers have formulated numerous strategies to approach these problems. A straightforward example is the epsilon-greedy policy.

In the epsilon-greedy policy, you explore with probability epsilon and exploit with probability (1-epsilon); in other words, occasionally randomly sample a slot machine, and at all other times, keep going to the slot machine that you think has the highest payout probability. For simple multi-armed bandit problems, this epsilon-greedy strategy and its variants work quite well, and we arrive at optimal (or near optimal) strategies.

However, the reality is that life is a bit more wicked and complicated than the vanilla multi-armed bandit problem. In life, there are often pre-requirements, like completing medical school before being allowed to be a practicing doctor. This is equivalent to the unavailability of certain machines until other machines have been sampled, which is not a restriction in the original multi-armed bandit problem.

Furthermore, the payoff distributions in life are non-stationary; that is, payoff probabilities are not fixed and change throughout time. Payoffs from pursuing the same discipline will morph drastically as the world evolves.

For example, if you were a computer programmer in the mid-20th century, your payoff distribution looks markedly different than that of a computer programmer today. If we want to be extremely precise, we don't care about maximizing the next payoff but the total payoff throughout the game. A job might have very low payoff probabilities initially, but after spending a few years in it, it could evolve to be highly lucrative. If you were extraordinarily myopic and only tried to maximize the next possible payoff, your shortsightedness could cost you considerably.

The good news is that life also has some nice attributes that make this optimization problem a bit easier: each pull in life is not independent. In the original multi-armed bandit formulation, each trial on a machine was independent — when you pulled a lever, it only gave you information about the payoff of that specific machine and nothing else.

In life, when you try something, it gives you a wealth of information not only about that item but also about many other tangentially related items. Once you find out that you enjoy solving quantitative problems, the appeal of various other disciplines — mathematics, engineering, physics, etc. — increases. Or, if you realize that you experience palpable anxiety whenever you are forced to perform in front of large audiences, that also conveys valuable information about your possible inclinations toward public speaking, musical performance, stand-up comedy, and the like.

Therefore, since exploration in real life has this unique non-independence property, there is extreme value in optimizing for learning and growth early in your career. If I were to describe my strategy, it is remarkably like the epsilon-greedy strategy, except that I dynamically adjust the epsilon exploration parameter through different phases of learning.

In the broadest view of my progression of knowledge and development, my epsilon will decrease on average over time as I delve deeper. Yet, when I encounter a new idea that upends my current frameworks or perspectives (which will inevitably happen), I will dramatically increase my exploration rate to adjust and learn more. Most importantly, this strategy should ideally keep intellectual calcification and complacency at bay.

And if it doesn't, I'll just have to adjust my strategy.
