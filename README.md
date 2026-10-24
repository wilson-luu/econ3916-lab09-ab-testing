# A/B Testing — Designing the Data-Generating Process

**Objective:** This project demonstrates how randomized assignment eliminates selection bias, and applies non-parametric statistical methods (permutation tests and bootstrapping) to evaluate causal Average Treatment Effects (ATE) in both experimental and observational contexts.

**Methodology:**
* Loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls) and computed the experimental ATE
* Simulated an observational comparison group to show selection bias, and split the gap: Observational ATE = True ATE + Selection Bias
* Ran a permutation test (9,999 shuffles) and a bootstrap BCa 95% confidence interval for the ATE
* Ran a power analysis: the power of this study, and the sample size needed for three dollar effects
* Applied the same tests to the Cookie Cats mobile game A/B test (90,189 players, gate at level 30 or 40, Day-1 retention)
* Wrote a sample-size function, n_needed(), checked it against the power analysis, and used it to size a rerun of Cookie Cats

**Key Findings:**
Trainees earned $1,794.34 more (permutation p = 0.0046, 95% CI $575.18 to $3,262.37); the simulated comparison group gave an ATE of -$14,784.45. Cookie Cats: a retention difference of 0.59 pp (p = 0.0752); a rerun would need 111,366 players per group.
