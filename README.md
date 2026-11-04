# econ5200-lab11-did

# Difference-in-Differences: Parallel Trends, Staggered Adoption and the Forbidden Comparison

## Objective
I worked through where difference-in-differences breaks down: when groups follow different trends, when treatment is adopted at different times, and when errors are correlated within states.

## Methodology
- Reproduced the Card and Krueger (1994) minimum-wage difference-in-differences from David Card's original data files and compared my estimate with their published +2.76.
- Built a panel where the true treatment effect was zero but the treated and control groups were on different trends, then ran a pre-trend test to diagnose the false positive.
- Simulated a staggered-adoption panel with a true mean effect of 6.71 and estimated it with two-way fixed effects.
- Decomposed the two-way fixed effects estimate into its two-by-two comparisons and measured how much weight fell on the comparison that uses already-treated units as controls.
- Simulated a panel with state shocks that persist from period to period and compared iid standard errors with the correct ones.
- Had an AI write a Goodman-Bacon decomposition, checked it against my own numbers, and revised my prompt once. I then tested it on a panel with missing outcomes.

## Key Findings
- My reproduction of Card and Krueger gave 2.75 full-time-equivalent employees, against their published +2.76.
- A significant difference-in-differences estimate appeared on a panel where the true effect was zero. Different trends between the groups caused it, and the pre-trend test caught it.
- Two-way fixed effects returned -0.94 on the staggered-adoption panel, where the true mean effect was 6.71. 0.667 of the weight sat on the comparison that uses already-treated units as controls.
- With persistent state shocks, iid standard errors were 8.6 times too small.
- The AI-written Goodman-Bacon decomposition needed one prompt revision. After that, its weighted sum on the panel with missing outcomes was 2.6735.
