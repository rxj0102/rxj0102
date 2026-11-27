## Rajvardhan Jadhav

MS in Quantitative Finance and Risk Management at Temple University (Fox), May 2027. B.Tech in Computer Science, NIT Warangal.

I test ideas on free data and report what holds up, including when nothing does. Every number in these READMEs is written by code in the repo, and CI fails if the page and the results disagree.

**Start here.** [behavioral-pricing-kernel](https://github.com/rxj0102/behavioral-pricing-kernel) for research: four hypotheses written down before any estimation, a log of every specification run, and all four reported as not supported. [Portfolio-VaR](https://github.com/rxj0102/Portfolio-VaR) for risk: ten models re-estimated on past data only and scored on 25 years they had not seen, next to the in-sample shortcut that makes them look better than they are.

### Research

| Repo | Question | Answer |
|---|---|---|
| [behavioral-pricing-kernel](https://github.com/rxj0102/behavioral-pricing-kernel) | Is the option-implied pricing kernel behavioral? | Pre-registered on 815 densities: none of four hypotheses supported |
| [Portfolio-VaR](https://github.com/rxj0102/Portfolio-VaR) | Which VaR models survive a walk-forward backtest? | GJR-GARCH-t at lag one; none under the Dynamic Quantile test, over 6,474 days |
| [var-confidence-audit](https://github.com/rxj0102/var-confidence-audit) | Do banks' trading VaR models hold their stated confidence? | 106 bank-years of 10-K backtests: far too cautious on average, about 2.5 times too many 99% exceptions in 2007, 2008 and 2020 |
| [13f-timestamp-alpha](https://github.com/rxj0102/13f-timestamp-alpha) | Do hedge funds hide their best ideas in confidential 13F filings? | No: hidden and shown positions earn the same (t 0.10) |
| [congressional-trading-alpha](https://github.com/rxj0102/congressional-trading-alpha) | Can outsiders profit by copying Congress members' disclosed trades? | No: 37,096 House trades from official filings earn nothing after disclosure (t -0.8) and late filings point the wrong way; 7,850 Senate trades show nothing that survives a multiple-testing correction |
| [options-vol-surface](https://github.com/rxj0102/options-vol-surface) | Does VIX overstate the volatility that follows? | Yes: above realized volatility in 84% of 21 day periods since 1995, by 4.1 vol points on average, yet no worse a forecast than GARCH |
| [factor-research](https://github.com/rxj0102/factor-research) | How much does survivorship bias inflate factor returns? | Rebuilding S&P 500 membership cuts the size spread from 12.5% to 5.7% a year |

### Systems

| Repo | What it is | Evidence |
|---|---|---|
| [hft](https://github.com/rxj0102/hft) | C++20 tick-to-trade engine | Back-to-back replay understates latency: a quiet tick takes 94 ns back to back and 531 ns at 1 ms spacing. On a real Nasdaq ITCH day its book matches a separate Python rebuild from the raw feed at every update |
| [limit-order-book-matching-engine](https://github.com/rxj0102/limit-order-book-matching-engine) | C++20 order book and replay | A full real Nasdaq ITCH day: top of book identical to a separate Python rebuild from the raw feed at 2.6 million updates |
| [sentinel](https://github.com/rxj0102/sentinel) | Signal platform with a locked holdout | None of four locked signals confirmed out of sample |

### Libraries

Pricing and volatility libraries (stochastic, rough and local volatility, rates, exotic Monte Carlo), checked against closed forms and published benchmarks such as Hull's tables.

### How I use AI

Most of this code was written with Claude Code, and the commits say so. I set the question, the data and the pass or fail rule before results exist, and every README number is written by code that CI checks. Checking the output against closed forms, benchmarks and second implementations found and fixed over 20 real bugs, each in its own pull request with before and after numbers.

GitHub: [rxj0102](https://github.com/rxj0102) · Site: [rxj0102.github.io](https://rxj0102.github.io)
