# The Skew Risk Premium
### Implied versus Realized Asymmetry, and Where the Moment Ladder Breaks

Part of *Notes on Volatility Trading*.

A complete, in-depth look at skew, from how it is measured to how it is traded.

## The question

Investors overpay for volatility, but do they also overpay for asymmetry? They do.
Implied skew is systematically steeper than the skew that returns actually realize,
and that gap is a second premium, one you can trade.

## What it covers

**Part I: The Skew Risk Premium**

1. **Two meanings of skew.** The slope of the volatility surface and the third moment
   of returns, and how the two connect.
2. **The skew risk premium.** Its definition, and the three forces that sustain it:
   structural put demand, jump risk that realized returns under-count, and
   correlation in index products.
3. **Model-free extraction with BKM.** Risk-neutral skewness from option prices alone,
   built as the variance-swap replication run at higher order.
4. **Noise in the realized leg.** Why the standard error of sample skewness is at best
   √(6/n), and the robust estimators that trade tail sensitivity for stability.
5. **Trading the premium.** The risk reversal as a vanna trade, its Greek profile, and
   the situations that motivate a trade.

**Part II: Where the Moment Ladder Breaks**

6. **Why variance and not volatility.** Variance is additive, it replicates cleanly,
   and the square root carries a Jensen wedge.
7. **Where the moment ladder breaks.** Estimation noise worsens at every higher
   moment, truncating the strike grid can flip the sign of extracted kurtosis, and the
   premia of successive moments stop being distinct.

The notes close with the questions the framework should answer, including how to tell
a mispricing from a regime shift, and whether a 25-delta skew is enough or BKM is
necessary.

## Reading it

Self-contained, with derivations shown rather than asserted and the key results
checked by simulation. The LaTeX source is in this folder; compile it with any standard
TeX distribution.

## Related notes

- *Hedged Straddles, Hedging Error and the Variance Swap*: the variance premium this
  note extends one moment up, and the static replication that BKM builds on.

## Corrections

If you find an error, I want to know. That is the standard the notes are built on.
