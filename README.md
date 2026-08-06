# Notes on Volatility Trading

*Personal notes on options, volatility, and quantitative trading.*

## About

These notes document my ongoing study of options and volatility. Rather than
being encyclopedic, each is a self-contained treatment of a topic I found
interesting or insufficiently explained in standard references.

They are not a replacement for textbooks. The aim is to answer the questions
those textbooks tend to leave open: why a result holds, when it breaks, and
what it means for someone actually trading volatility. Every document is
written independently from first principles unless stated otherwise.

The probability and ATM-approximation notes come first and serve as the
mathematical foundation; the later notes build toward concrete
volatility-trading ideas.

## Philosophy

Most references explain *what* a model or strategy is. These notes focus on:

- **Why** it works
- **When** it works and when it fails
- **What assumptions** are hidden behind it
- **Why a volatility trader should care**

Wherever possible, derivations are paired with intuition, practical
implications, and limitations. The emphasis is on understanding, not
memorization.

## Project scope

The repository is open-ended and grows as new notes reach publication quality. 

## Roadmap

| Note | Status |
|:-----|:------:|
| Probability problems, generalized | ✅ Complete |
| ATM approximations | ✅ Complete |

## Contents

**Volume I — Probability** *(complete, ~110 pp)*
- 📘 [`generalized_probability_problems/`](01-generalized_probability_problems/): sixteen problem-driven chapters
  on exchangeability, order statistics, reinforcement processes,
  optimal stopping, pattern hitting times, random walks, the arcsine
  law, extreme values on discrete sequences, growth-optimal betting,
  and information theory.

**Volume II — ATM approximations** *(complete)*
- 📗 [`options/ATM-approximations/`](options/02-ATM-approximations/):
  closed-form expressions and error bounds for at-the-money options,
  useful as trader-grade intuition for short-dated Black–Scholes
  prices.

## Repository structure

```
Notes-on-Volatility-Trading/
├── README.md
├── LICENSE
├── pdf/
│   ├── 01_Probability_Problems.pdf
│   ├── 02_ATM_Approximations.pdf
│   └── ...
└── images/
```

## References

Where possible, derivations are supported by standard textbooks, papers, or
publicly available literature. Where an explanation reflects my own
interpretation, it should be read as my personal understanding rather than an
established result.

## Feedback

This is an ongoing personal project. If you spot a mathematical error, an
unclear explanation, or have a suggestion, I'd genuinely appreciate it through
GitHub Issues.

## Disclaimer

These notes are for educational purposes only. Nothing here constitutes
financial advice or a recommendation to trade any instrument.

## Author

Diego de la Fuente: [LinkedIn](https://www.linkedin.com/in/diego-de-la-fuente-ba9041211)

## License

Released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/):
free to share and adapt with attribution.

---

*"The goal is not to accumulate formulas, but to develop the intuition
required to think about volatility."*
