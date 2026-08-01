# Probability Basics

**Key points / formula:** P(event) = favorable outcomes / total outcomes. P(A and B independent) = P(A) x P(B). P(A or B) = P(A) + P(B) - P(A and B) (to avoid double-counting overlap).

**When it's asked (pattern cue):** Dice, cards, coin-flip problems, or "what's the chance that at least one of..." (often easier via 1 - P(none)).

**Worked micro-example:** Probability of rolling at least one 6 in two dice rolls.
```
P(no 6 on one roll) = 5/6
P(no 6 on both rolls) = 5/6 x 5/6 = 25/36
P(at least one 6) = 1 - 25/36 = 11/36
```

**Common gotcha / trick:** Forgetting to subtract the overlap term in P(A or B) when events aren't mutually exclusive; not recognizing "at least one" problems are usually solved faster via the complement (1 - P(none)) than by direct casework.
