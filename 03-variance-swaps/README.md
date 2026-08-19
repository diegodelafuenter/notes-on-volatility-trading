# Hedged Straddles, Hedging Error, and the Variance Swap

Part of *Notes on Volatility Trading*.

A self-contained note on why a continuously delta-hedged straddle is *not* a
variance swap, and what the single difference between them — dollar-gamma
weighting — implies for replication, hedging error, and the way the clean
picture breaks on a real book.

## The question

If a continuously delta-hedged straddle earns P&L tied to realized variance,
why isn't it simply a variance swap? The answer is one word: **weighting**.
The notes develop the full chain behind it, from a single option to the
variance swap and its variants.

## What it covers

- The P&L of any delta-hedged option as the dollar-gamma-weighted integral of
  realized minus implied variance — not special to the straddle.
- The vega / vanna / volga block that constant-implied marking hides: it
  vanishes at expiry (a pure variance trade held to expiry) and is realized in
  full if the position is closed early (a vega trade). The bridge to surface
  dynamics.
- Discrete-hedging error: the 1/√n scaling, and why halving the error costs
  four times the hedges — a rate robust to path-varying gamma.
- The variance swap: how the 1/K² strip makes dollar gamma constant in spot and
  removes the weighting, and why this is the construction underneath the VIX.
- Where the clean picture breaks on a real book: jumps (the O(J³) residual that
  gives variance swaps their crash risk) and the gamma swap that tames it.
- Pricing in practice: why the swap never leaves the strip — the strike *is* the
  replication, trading OTC relocates it rather than escaping it, and the cost
  stack (the un-buyable wing, the jump residual) explains why single-name swaps
  live OTC and why the cap sits on the left tail.

## Reading it

Self-contained, with worked examples and derivations shown rather than
asserted. The LaTeX source is in this folder; compile with any standard TeX
distribution.

## Corrections

If you find an error, I want to know — that is the standard the notes are built on.
