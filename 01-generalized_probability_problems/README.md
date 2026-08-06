# Volume I: Generalized Probability Problems

Sixteen problem-driven chapters, roughly 110 pages, on the probability
machinery that recurs in quantitative trading.

Each chapter follows the same arc:
1. Open with a concrete question.
2. Develop exactly the tools its solution requires.
3. Generalize the problem as far as it goes.
4. Return to trading applications where the mathematics is genuinely
   relevant.

📄 **[Read the compiled PDF](generalized-probability-problems.pdf)** • sources in this folder

## Contents at a glance

| Theme                                  | Central problem                     |
|----------------------------------------|-------------------------------------|
| Exchangeability                        | Records, secretary, uniform sum     |
| Order statistics                       | Max–min identity, `E|X-Y|`          |
| Reinforcement processes                | Pólya urn                           |
| Optimal stopping                       | Secretary variants, red–black cards |
| Pattern hitting times                  | Guibas–Odlyzko theorem              |
| Random walks and gambler's ruin        | Hitting probabilities and times     |
| Ballot problem and arcsine law         | The U-shape of time-positive        |
| Extreme values on discrete sequences   | Longest run of heads                |
| Growth-optimal betting                 | Kelly criterion                     |
| Size-biasing and renewal theory        | Bus paradox                         |

Detailed descriptions below.

## What is covered

### Exchangeability and the counting of orderings

Three of the most-cited constants in probability — *e*, 1/*e*, and
*π*/4 — all emerge from one mechanism: uniformly distributed orderings
of i.i.d. observations. Chapters:

- Records and their logarithmic scarcity
- The secretary problem and the 37% rule
- The uniform-sum problem and its appearance of *e*
- Catalan first-passage times and *π*/4

### Order statistics and the max–min toolkit

Expected maxima and minima under uniform and general laws, plus the
max–min identity that reduces `E|X-Y|` to two order-statistic
computations. Consequences developed in the chapter:

- Empirical quantiles and historical Value-at-Risk
- The Parkinson volatility estimator as a range functional
- Vickrey–Myerson revenue equivalence as a statement about
  `E[U_{(n-1)}]`

### Reinforcement processes and Bayesian updating

The Pólya urn as a martingale, with its limit identified as a Beta
distribution via moment matching. The reinforcement parameter reads
as a dial:

- Small reinforcement → deterministic limit (sampling with replacement)
- Large reinforcement → coin-flip limit (aggressive reinforcement)
- Negative reinforcement → self-correcting limit (sampling without
  replacement, converging to a Brownian bridge)

Closes with the derivation of the urn as a physical realization of
Beta–Binomial conjugacy.

### Optimal stopping under partial information

The two flavors of stopping problem, sharpened by their differences:

- **Rank-based:** secretary problem and its variants (expected rank,
  top-k, sample buying with paid observation).
- **Value-based:** the red–black card problem via Bellman recursion.

Includes the boundary case that distinguishes problems where dynamic
programming is necessary from those where a martingale shortcut kills
the game.

### Pattern hitting times

The Guibas–Odlyzko theorem for the expected time to see a fixed
pattern in i.i.d. tosses, developed through two independent proofs:

- Probability generating functions and the autocorrelation polynomial
- Optional stopping on a population of gamblers (the "infinite casino")

Includes Conway's leading-number algorithm for pattern-vs-pattern
races.

### Random walks and gambler's ruin

Simple symmetric and asymmetric walks, hitting probabilities and
expected times via first-step analysis, and the reflection principle.
Read as discrete Poisson equations, harmonic functions produce linear
ruin probabilities, constant sources produce parabolic hitting times,
and the framework generalizes verbatim to Brownian motion.

### Ballot problem and the arcsine law

Sparre Andersen uniformity, the last-zero decomposition, and the
derivation via bivariate generating functions of the counterintuitive
U-shape: the fraction of time a random walk spends positive is
maximized at 0 and 1, not at 1/2. The same central-binomial kernel
that produces *π*/4 in the majority-crossing problem produces the
arcsine density here.

Trading applications: reading P&L paths, time above high-water mark
as an edge signal, the timing of maximum drawdowns.

### Extreme values on discrete sequences

The longest run of heads: a tour of four approximation methods,
priced against each other in accuracy and speed:

1. Poisson bound → self-deriving, biased by roughly +1 unit
2. Pooling principle → reduces multi-sequence problems to one
3. Schilling's asymptotic → closed form, accurate to a tenth of a unit
4. Exact Markov chain → the benchmark

Includes the Chen–Stein reading of Poisson clumping, the biased-coin
generalization, and applications to stop-loss calibration and
multiple-testing inflation in backtests.

### Growth-optimal betting and information theory

The Kelly criterion under discrete and continuous returns, the
volatility-drag formula `g ≈ μ − σ²/2` and its vertex form, and the
identity `g* = Sharpe²/2`.

The chapter closes with the identification of the growth rate as a
Kullback–Leibler divergence, (*your growth rate is the distance
between your beliefs and the price*) and the mutual-information
theorem for side information.

### Size-biasing and renewal theory

The bus paradox and the inspection paradox as manifestations of one
mechanism (length-biased sampling), plus the renewal theorem used
across the volume to distinguish diffusive from linear regimes in
record frequencies and run lengths.

### Appendix

Nine background entries used across the chapters: Stirling and the
harmonic numbers, Gumbel and extreme value theory, the Beta family as
a unifier of order statistics and the arcsine law, martingales and
optional stopping, generating functions as an analytic toolbox, and
de Finetti's representation theorem.

## Suggested reading path

Every chapter is self-contained. For someone approaching the material
cold: start with **records and the constant *e*** — it introduces
exchangeability, the mechanism that recurs across the volume — then
jump to whichever problem sounds most interesting. Cross-references
are explicit where one chapter's tools are used by another.
