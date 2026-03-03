---
layout: page
title:
---

# Project Insight

Project Insight was the mathematical companion to [Project Federer](/projects/project-federer). Where Project Federer asked "which shots are most effective?", Project Insight asked a more fundamental question: given that a player wins each point with some probability *p*, what is the probability of winning the entire match? The answer turns out to be far from obvious, because tennis has one of the strangest scoring systems in sports -- and that structure has profound consequences for competition.

A tennis match is built from a hierarchy of points, games, and sets. A game requires winning at least four points by a margin of two. A set requires winning at least six games by a margin of two (with a tiebreak at 6-6). A match requires winning two out of three sets. At every level, there are potential infinite extensions -- deuce games, tiebreaks -- that make the math interesting.

The game-level model was the foundation. I defined *g(p)* as the probability of winning a game given point-win probability *p*, then decomposed it into two parts: the "prior deuce probability" (winning in four, five, or six points before reaching deuce) and the "infinite sum probability" (reaching deuce at 3-3, then eventually winning two consecutive points). The key insight is that after deuce, the game resets -- each pair of points is independent. This means the infinite sequence of possible deuce outcomes forms a geometric series that converges to a clean closed-form expression.

The set-level model was considerably more complex. There are exactly three disjoint ways to win a set: win 6-0 through 6-4 (be the first to six games while the opponent has at most four), win 7-5 (both players reach five games, then win two straight), or win 7-6 via tiebreak (both players reach six games, then win a tiebreak to seven points). I first computed a "naive" version assuming one player serves every game, then built a "robust" version that properly accounts for service alternation -- introducing separate probabilities for winning a service game and a return game. This required enumerating every possible combination of service and return games won at each score, producing pages of combinatorial expressions.

The tiebreak calculation mirrored the game model but with a deuce threshold at 6-6 instead of 3-3, and in the robust version, alternating service and return point probabilities throughout. The match probability was the simplest piece: the probability of winning two out of three independent sets.

The full model was implemented as a Python script with functions for each layer -- `game_prob`, `tiebreak_prob`, `set_prob`, and `match_prob` -- that could be composed into a single function taking just two inputs: probability of winning a service point and probability of winning a return point.

I validated the model against real data from the same match that drove Project Federer -- my 5-7, 6-0, 6-0 loss to Sanjay. The results were striking. Using Set 1 data alone (where I won 53% of service points and 56% of return points), the model predicted an 87.9% chance of victory -- consistent with me actually winning that set. Using Set 2 data (41% service, 14% return) and Set 3 data (41% service, 25% return), the predicted win probabilities collapsed to essentially zero. Across the full match, I won 45% of service points and 41% of return points -- numbers that sound competitive. But the model predicted just a 3.03% chance of winning.

This was the paper's most important finding: tennis's hierarchical scoring structure acts as a massive amplifier of small point-level advantages. If a player wins 50% of service points and 50% of return points, their match-win probability is exactly 50%. But winning just 51% of service points (with return held at 50%) jumps the match-win probability to 55.35%. The structure of the sport means that small, consistent edges at the point level compound dramatically through games, sets, and the match.

The model's main assumption -- that all points are independent and identically distributed -- doesn't perfectly hold in reality, since players are affected by momentum, fatigue, and pressure. But I cited research by Klaassen and Magnus (2001) showing that while tennis points aren't perfectly i.i.d., their divergence from independence is extremely small, especially at higher levels of play. For the purpose of modeling match outcomes, the assumption is reasonable.

Together, Project Federer and Project Insight represent two complementary approaches to understanding tennis through mathematics: one empirical and data-driven, the other theoretical and probabilistic. Project Federer tells you *which shots to hit*; Project Insight tells you *how much each point matters*.

[Read the full paper (PDF)](https://www.dropbox.com/scl/fi/ifq726qyvpychjxztuol9/Project-Insight.pdf?rlkey=xff8h7qya7xwn0dut2v8atvqx&e=3&dl=0)
