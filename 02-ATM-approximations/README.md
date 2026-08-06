# ATM Option Approximations

Desk-level mental pricing of options and Greeks. This note derives the fast
approximations a trader uses to price and risk-manage options in their head,
and (more importantly) shows that they all descend from a **single number**:
the height of the standard normal density at zero, $\varphi(0) \approx 0.4$.

The emphasis throughout is on *why* each shortcut works, the exact identities
that connect the Greeks, and the precise conditions under which each
approximation holds and breaks.

---

## What's inside

| # | Topic | Key result |
|---|-------|-----------|
| 1 | **Brenner–Subrahmanyam** | ATM option price $\approx 0.4\,S\,\sigma\sqrt{T}$ |
| 2 | **ATM delta** | $\Delta_{\text{ATM}} \approx 0.5 + 0.2\,\sigma\sqrt{T}$ — the ATM call is *not* the 50-delta option |
| 3 | **ATM vega** | $\text{Vega}_{\text{ATM}} \approx 0.4\,S\sqrt{T}$, with the exact identity $S\,\varphi(d_1) = K\,\varphi(d_2)$ |
| 4 | **Vega put–call symmetry** | Same-strike call vega equals put vega, exactly; and the 25Δ symmetric-delta case, where the smile breaks it |
| 5 | **Vega–gamma identity** | $\text{Vega} = S^2\,\sigma\,T\,\Gamma$ — the exchange rate between implied and realized vol exposure |
| 6 | **Theta–gamma identity** | $\theta = -\tfrac12\,\sigma^2 S^2\,\Gamma$ — theta is the rent paid for gamma |
| 7 | **The daily breakeven move** | $\sigma\sqrt{dt} \approx \sigma/16$ — the "rule of 16" derived, not recited |
| 8 | **Theta / premium rule** | $|\theta| \approx C/(2T)$ at the money, with the ITM/OTM deviations |

**Appendix — $\sqrt{T}$ at a glance.** A lookup table of $\sqrt{T}$ and the
ATM premium as a percentage of spot for the standard horizons (1 day through
1 year), plus the three mental anchors: *three months is one half*, *one
trading day is one sixteenth*, and *doubling maturity multiplies by 1.4*.

---

## The organizing idea

Every approximation in the note traces back to the first-order expansion of
the normal CDF around zero, $N(x) \approx \tfrac12 + \varphi(0)\,x$, evaluated
at the ATM point $d_1 = \sigma\sqrt{T}/2$. The premium, the delta correction,
and the vega all fall out of the same step. The Greeks are then tied together
by two exact identities: **vega–gamma** and **theta–gamma**, so that the entire
desk toolkit is one geometric truth (the value $0.4$) plus two lines of
algebra.

The note is deliberately explicit about the boundary between what is *exact*
(the vega–gamma and theta–gamma identities, put–call vega symmetry at a common
strike) and what is *approximate* (everything carrying a $\approx$, valid at
the money and degrading with moneyness). Knowing which is which is the point.

---

## Scope and assumptions

- **European options**, zero rates ($r = 0$) unless stated otherwise. The
  zero-rate assumption keeps the algebra clean and is a good approximation in
  the low-rate regimes where these mental shortcuts are used; the structure
  survives non-zero rates with forward-based (Black-76) versions.
- **At the money** is the working regime. Each result states how it deviates
  as the option moves in- or out-of-the-money.
- Volatility is quoted **annualized**; time in **years**; the daily breakeven
  uses trading time ($dt = 1/252$).

---

## Who this is for

Anyone who prices or risk-manages options and wants the mental arithmetic to
be fast *and* correct (where $0.4\,S\sigma\sqrt{T}$ and
the rule of 16 come up constantly), desk work, or building intuition behind
the exact Black–Scholes Greeks.

Prerequisites: comfort with the Black–Scholes formula and the standard Greeks.
No stochastic calculus required — the note works entirely at the level of the
BS formula and its derivatives.

---

## Files

- `ATM_option_approximations.pdf` — the compiled note (corrected edition).

---

## References

- Brenner, M. & Subrahmanyam, M. G. (1988). *A Simple Formula to Compute the
  Implied Standard Deviation.* Financial Analysts Journal, 44(5), 80–83.
- Natenberg, S. (2014). *Option Volatility and Pricing*, 2nd ed. McGraw-Hill.
- Sinclair, E. (2013). *Volatility Trading*, 2nd ed. Wiley.

---

*Part of a series of study notes on options and volatility trading.*
