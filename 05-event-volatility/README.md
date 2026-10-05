# Event Volatility
### Pricing the jump from the term structure, and trading it with a bounded tail

Part of [*Notes on Volatility Trading*](../../).

An option whose life spans an information event (an earnings release, a central-bank
decision, a binary ruling) carries an implied variance that splits into a diffusion part
and an event part:

$$\sigma_{\text{IV}}^2\,T = \sigma_{\text{diff}}^2\,T + \sigma_{\text{event}}^2$$

These notes build everything on that one identity.

## The question

Implied volatility rises into an earnings release and collapses after it. Can that
pattern be traded? Under fair pricing, no: the path is arithmetic, a fixed event variance
spread over fewer and fewer days, and every hedged position through the event has zero
expected P&L. What can be traded is the level of the event's volatility against what the
stock has actually done in past events. The notes work out how to measure that gap and
how to trade it.

## What it covers

**Part I: Pricing the volatility of an event**

1. **The variance decomposition.** Diffusion variance plus event variance, and why
   variance adds while volatility does not.
2. **The term-structure cliff.** Extracting the event variance from expiries that bracket
   the event, and from two expiries that both contain it when no pre-event expiry exists.
3. **The mechanical path of implied volatility.** Why it rises into the event and
   collapses after it.
4. **Why the path is not a tradable signal.** The vega gained on the way up is already
   paid for by time decay and by the gamma of the jump.
5. **Calibration in practice.** Diffusion volatility, implied and realized event
   volatility, the signal, and the limits of a small history that may describe a
   different company.

**Part II: Trading the event**

6. **The naked short straddle.** A high win rate over an unbounded left tail.
7. **The post-event calendar.** Why its loss through the event is bounded by the debit
   paid, and why it keeps only part of the edge.
8. **A worked example.** Outcomes by size of move, expected P&L and risk, transaction
   costs, and the tenor of the long leg as the dial between edge and tail.
9. **Practical considerations.** Strikes, expiries, Greeks, exit, and when the trade fails.

In the worked example, the calendar keeps about a tenth of the naked straddle's edge, and
breaks even at a transaction cost of about 1% per side, against 19% for the naked
straddle.

## Reading it

Self-contained, around 20 pages, with derivations shown rather than asserted. Every
number in the worked example comes from exact Black–Scholes repricing and Monte-Carlo
simulation, and the scripts that produce them are in this folder.

## Corrections

If you find an error, I want to know. That is the standard the notes are built on.
