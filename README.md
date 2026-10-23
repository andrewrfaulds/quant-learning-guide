# Quant Learning Resources

*Compiled by Andrew Faulds ¬∑ October 2026*

Start with the three core books: they cover how markets work, how options are priced and how orders get executed. The papers and whitepapers then explain the mechanics behind market making and crypto derivatives. Everything after that is optional depth, ordered roughly by how often it comes up for engineers building trading systems.

## Contents

- [Core books](#core-books)
- [Key papers](#key-papers)
- [Crypto market structure](#crypto-market-structure)
- [Probability and statistics](#probability-and-statistics)
- [Going deeper](#going-deeper)

## Core books

Read these first, in this order. Together they give a working vocabulary for trading, options and execution.

| Book | Author | What it gives you |
| --- | --- | --- |
| *Trading and Exchanges: Market Microstructure for Practitioners* (2003) | Larry Harris | The best map of how markets actually work: order types, who trades and why, liquidity, dealers and market makers, and how exchange rules shape behaviour. Non-mathematical. |
| *Option Volatility and Pricing* (2nd ed., 2015) | Sheldon Natenberg | The standard practitioner's introduction to options: pricing models, the Greeks, volatility, spreads and risk management. Widely used to train new option traders. |
| *Algorithmic Trading and DMA* (2010) | Barry Johnson | How orders move from strategy to exchange: order books, execution algorithms (VWAP, TWAP, implementation shortfall), transaction costs and direct market access infrastructure. |

## Key papers

Three short classics explain why spreads exist and how market makers set quotes. Avellaneda-Stoikov is the most directly useful for anyone building quoting systems.

| Paper | Published in | Key idea |
| --- | --- | --- |
| Glosten & Milgrom, "Bid, ask and transaction prices in a specialist market with heterogeneously informed traders" (1985) | *Journal of Financial Economics* | The bid-ask spread exists because market makers lose to better-informed traders and must charge everyone else to compensate (adverse selection). |
| Kyle, "Continuous Auctions and Insider Trading" (1985) | *Econometrica* | An informed trader hides orders among noise traders; prices absorb information gradually. Introduces market depth, often called "Kyle's lambda". |
| Avellaneda & Stoikov, "High-frequency trading in a limit order book" (2008) | *Quantitative Finance* | A practical model for where a market maker should place bids and asks, skewing quotes to manage inventory risk. The starting point for most market-making strategies. |

## Crypto market structure

Two primary sources cover the instruments that make digital asset markets different from traditional ones.

| Source | Key idea |
| --- | --- |
| BitMEX perpetual swap documentation | Explains the perpetual future: a futures contract with no expiry, kept close to spot by periodic funding payments between longs and shorts. Now the most traded crypto derivative. |
| Uniswap v3 whitepaper (2021) | Explains automated market makers with concentrated liquidity, where liquidity providers choose a price range. Useful for understanding on-chain liquidity and how it differs from a limit order book. |

## Probability and statistics

A path from beginner to quant-level fluency. Checking textbook problems with short Python Monte Carlo simulations is a good way to build intuition alongside the maths.

| Resource | Why it's here |
| --- | --- |
| MIT 6.0002 (*Introduction to Computational Thinking and Data Science*), Monte Carlo lectures | Free lectures; a gentle, code-first introduction to simulation. |
| Harvard Stat 110 with Blitzstein & Hwang, *Introduction to Probability* | The best foundational probability course; lectures and problem sets are free online. |
| Owen, *Monte Carlo Theory, Methods and Examples* | Error estimation and variance reduction; pairs well with building a Monte Carlo option pricer and checking it against Black-Scholes. |
| Mosteller, *Fifty Challenging Problems in Probability* | Short puzzles for building speed and intuition. |
| Zhou, *A Practical Guide to Quantitative Finance Interviews* (the "green book") | Interview-style problems in probability, brain teasers and finance. |
| Ross, *Introduction to Probability Models* | Stochastic processes: Markov chains, Poisson processes, queueing. |
| Wasserman, *All of Statistics* | A dense, fast tour of statistics and inference for people with some maths. |
| Shreve, *Stochastic Calculus for Finance I* | Discrete-time option pricing (binomial model); the bridge into continuous-time finance. |
| Glasserman, *Monte Carlo Methods in Financial Engineering* | The reference text for simulation in derivatives pricing. |

## Going deeper

Optional, for those who want more after the core material. Cartea is the natural next step after Avellaneda-Stoikov but assumes stochastic calculus.

| Book | Author | What it gives you |
| --- | --- | --- |
| *Algorithmic and High-Frequency Trading* (2015) | Cartea, Jaimungal & Penalva | Rigorous models for optimal execution and market making using stochastic control. |
| *Paul Wilmott Introduces Quantitative Finance* | Paul Wilmott | A readable introduction to derivatives maths and the Black-Scholes framework. |
| *Mathematics for Finance* | Capinski & Zastawniak | A compact intro to the maths of pricing, from interest rates to options in discrete time. Small enough to read on a commute. |
| *Advances in Financial Machine Learning* (2018) | Marcos L√≥pez de Prado | How to apply ML to financial data without fooling yourself: labelling, backtest overfitting, feature importance. |
| *Designing Data-Intensive Applications* | Martin Kleppmann | Not a finance book, but the best guide to the data systems (streams, replication, consistency) that trading platforms are built on. |

