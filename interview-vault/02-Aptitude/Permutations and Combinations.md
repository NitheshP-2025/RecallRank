# Permutations and Combinations

**Key points / formula:** Permutation (order matters): nPr = n!/(n-r)!. Combination (order doesn't matter): nCr = n!/(r!(n-r)!). Use permutations for arrangements, combinations for selections/groups.

**When it's asked (pattern cue):** "In how many ways can you arrange" (permutation) vs "in how many ways can you choose/select a group" (combination) — the key tell is whether order/position matters in the answer.

**Worked micro-example:** Choose 3 people from a group of 5 for a committee (order doesn't matter).
```
5C3 = 5! / (3! x 2!) = (5x4x3x2x1) / (3x2x1 x 2x1) = 10
```

**Common gotcha / trick:** Using nPr when the problem actually describes an unordered selection (or vice versa) — always ask "does swapping two chosen items create a different valid answer?" If yes, use permutation; if no, use combination.
