---
layout: page
title:
---

# Project Federer

In the summer of 2015, I played a series of tennis matches against my friend Sanjay Kaliyur at Princeton. I lost every single one. The closest I came was a match on September 9th, which Sanjay won 5-7, 6-0, 6-0 -- I took my first-ever set off him, then completely fell apart. Afterward, I had a flood of questions about what went wrong and no way to answer them. Luckily, we had recorded the entire match. Project Federer was born from the simple frustration of losing and wanting to understand why.

The project's goal was to evaluate three different methods of measuring tennis performance and determine which is most useful for informing strategy and training: the eye test (qualitative observation), traditional statistics (aces, first serve percentage, break points, etc.), and a new shot-level analytical framework I designed from scratch.

The eye test -- watching the match and assessing each player's strokes, movement, footwork, and mentality -- yielded broad conclusions. Sanjay was superior in forehand, serve, volleys, footwork, and experience; I had the edge in backhand and movement. The resulting strategy was straightforward: get my serves in, extend rallies, hit to Sanjay's backhand, avoid his forehand. Useful, but not specific enough to build a training plan around.

Traditional statistics gave more precision but still left critical questions unanswered. I had a 7:29 winner-to-unforced-error ratio, made only 50% of my first serves, and served 14 double faults. But the stats couldn't tell me *which* types of serves I was missing, whether my errors came from poor movement or unfamiliarity with pace, or whether my break points lost were due to serving or groundstroke breakdowns.

To go deeper, I invented a shorthand notation system that captured every shot across five attributes: the player who hit it, the stroke type (forehand, backhand, serve, volley, overhead, etc.), the spin (topspin, flat, slice, kick), the direction (crosscourt, down-the-line, inside-out, middle, etc.), and the result (winner, unforced error, forced error, ace, double fault). A single shot like "C_F_t_CC_W" translates to "Chow hits a topspin forehand crosscourt winner." With this system, there were 1,326 possible shot types spanning forehands, backhands, first serves, second serves, volleys, overheads, and specialty shots.

I then manually transcribed every shot from the match video into this code -- over 600 shots across three sets -- and entered them into an Excel spreadsheet. To avoid counting occurrences by hand, I built a Python tennis client that could ingest the shot data from a text file and let me search and filter by any combination of attributes. Want to find every flat forehand I hit down the line? Every kick serve Sanjay hit wide on the ad side? The client would return every match and the total count instantly.

With the data structured, I developed the Benefit Index -- a metric for ranking each shot's contribution to winning. For a given shot, the index squares the number of times that shot appeared in points I won (to weight sample size), divides by the total times the shot was attempted across all points, and scales by the ratio of that stroke type to all groundstrokes. This produced ordinal rankings of my 84 unique shots from most to least beneficial. My top groundstrokes were topspin forehands and backhands to the middle; my worst were slice and flat shots to unconventional directions. For first serves, flat serves down the middle on the deuce side ranked highest; for second serves, topspin wide on the deuce side was most effective.

The project had real limitations -- the sample size from a single match was too small for rigorous statistical conclusions, and shot correlation with winning a point is not the same as causation. Some rankings contradicted the eye test, and it was impossible to tell whether that reflected genuine insight or noise. But the framework proved the concept: granular shot-level data surfaces patterns that neither watching the match nor reading the box score can reveal, like which specific spin-direction combinations on serve correlate with holding serve, or which groundstroke patterns precede unforced errors.

I concluded that the success of this kind of tennis analytics hinges on the ease of data collection. Manually transcribing every shot from video is painful and time-consuming, and at the time of writing, computers weren't sophisticated enough to automate it. I predicted that once technology made shot-level data collection automatic, this kind of analysis would become standard. A decade later, that prediction has largely come true with companies like Hawk-Eye and SwingVision doing exactly this.

[Read the full paper (PDF)](https://www.dropbox.com/scl/fi/7trsshe5d07wa5eyts5hh/projectfederer.pdf?rlkey=grpvxfzqnhpdq0f1o8emkjt9s&e=3&st=rasvp8hg&dl=0)
