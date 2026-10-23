# Quant Learning Resources

*Compiled by Andrew Faulds, October 2026*

A reference list of trading, quant and trading-infrastructure resources. It isn't a course: dip into whichever sections fit what you're working on. Each entry has a level (**Intro**, **Mid** or **Advanced**) so you can pick the right entry point.

> **Note on focus:** I put this together while preparing for a role building digital asset trading systems, with options as my main focus. The options and crypto sections are the most detailed. The other sections cover the essentials rather than everything.

## Contents

- [Where to look](#where-to-look)
- [Background reading](#background-reading)
- [Market structure and microstructure](#market-structure-and-microstructure)
- [Classic papers](#classic-papers)
- [Execution and algorithmic trading](#execution-and-algorithmic-trading)
- [Options and volatility](#options-and-volatility)
- [Digital assets](#digital-assets)
- [Maths, probability and statistics](#maths-probability-and-statistics)
- [Engineering and infrastructure](#engineering-and-infrastructure)
- [Hands-on project ideas](#hands-on-project-ideas)

## Where to look

| If you are... | Good places to start |
| --- | --- |
| New to trading and want the big picture | Background reading, then Harris |
| An engineer building market data, order or execution systems | Market structure, Execution, Engineering and infrastructure |
| Working on market making or quoting | Classic papers (Glosten-Milgrom, Kyle, Avellaneda-Stoikov), then Cartea |
| Working on options pricing or risk | Options and volatility, then Probability |
| Working with crypto venues or DeFi | Digital assets |
| Brushing up the maths | Maths, probability and statistics |

## Background reading

Narrative books, light on maths, that explain how modern markets and quant firms came to be.

| Book | Level | Why read it |
| --- | --- | --- |
| *Flash Boys* (2014), Michael Lewis | Intro | The story of the HFT latency race and the founding of IEX. One-sided, but the best way into debates about speed, order types and market fairness. |
| *Dark Pools* (2012), Scott Patterson | Intro | How electronic trading and alternative venues replaced the trading floor. Good companion to *Flash Boys*. |
| *The Man Who Solved the Market* (2019), Gregory Zuckerman | Intro | Jim Simons and Renaissance Technologies; how systematic trading became an industry. |
| *When Genius Failed* (2000), Roger Lowenstein | Intro | The collapse of LTCM. A classic lesson in leverage, liquidity and model risk. |
| *My Life as a Quant* (2004), Emanuel Derman | Intro | A physicist's path into Wall Street modelling. A good read on what quants actually do. |

## Market structure and microstructure

How exchanges work, who trades and why, and how prices form.

| Book | Level | What it gives you |
| --- | --- | --- |
| *Trading and Exchanges: Market Microstructure for Practitioners* (2003), Larry Harris | Intro | The best map of how markets actually work: order types, who trades and why, liquidity, dealers and market makers, and how exchange rules shape behaviour. Non-mathematical. |
| *Market Microstructure Theory* (1995), Maureen O'Hara | Mid | The standard academic treatment of the theoretical models (inventory and information-based) behind spreads and price formation. |
| *Empirical Market Microstructure* (2007), Joel Hasbrouck | Mid | How to measure liquidity, price impact and trading costs from real data. |
| *Trades, Quotes and Prices* (2018), Bouchaud, Bonart, Donier & Gould | Advanced | A modern, data-driven view of limit order books and price impact, written by physicists working in trading. |

## Classic papers

The papers most often cited in trading work. Most are short and readable even if you skip the proofs.

| Paper | Published in | Level | Key idea |
| --- | --- | --- | --- |
| Black & Scholes, "The Pricing of Options and Corporate Liabilities" (1973) | *Journal of Political Economy* | Mid | The option pricing formula: an option can be hedged with the underlying, so its price doesn't depend on expected returns. |
| Merton, "Theory of Rational Option Pricing" (1973) | *Bell Journal of Economics* | Advanced | Generalises and formalises Black-Scholes; the foundation of continuous-time finance. |
| Glosten & Milgrom, "Bid, ask and transaction prices in a specialist market with heterogeneously informed traders" (1985) | *Journal of Financial Economics* | Mid | The bid-ask spread exists because market makers lose to better-informed traders and must charge everyone else to compensate (adverse selection). |
| Kyle, "Continuous Auctions and Insider Trading" (1985) | *Econometrica* | Mid | An informed trader hides orders among noise traders, and prices absorb information gradually. Introduces market depth, often called "Kyle's lambda". |
| Almgren & Chriss, "Optimal Execution of Portfolio Transactions" (2000) | *Journal of Risk* | Mid | The trade-off between trading fast (market impact) and slow (price risk) when working a large order. The basis of most execution algorithms. |
| Avellaneda & Stoikov, "High-frequency trading in a limit order book" (2008) | *Quantitative Finance* | Mid | Where a market maker should place bids and asks, skewing quotes to manage inventory risk. The starting point for most market-making models. |
| Easley, L√≥pez de Prado & O'Hara, "Flow Toxicity and Liquidity in a High-frequency World" (2012) | *Review of Financial Studies* | Mid | Introduces VPIN, a measure of how much order flow comes from informed traders, linked to the 2010 Flash Crash. |
| Cont, Kukanov & Stoikov, "The Price Impact of Order Book Events" (2014) | *Journal of Financial Econometrics* | Mid | Short-term price moves are driven mainly by order flow imbalance at the best bid and ask. |
| Budish, Cramton & Shim, "The High-Frequency Trading Arms Race" (2015) | *Quarterly Journal of Economics* | Mid | Continuous order books reward tiny speed advantages. Proposes frequent batch auctions instead. The academic counterpart to *Flash Boys*. |
| Kirilenko, Kyle, Samadi & Tuzun, "The Flash Crash: High-Frequency Trading in an Electronic Market" (2017) | *Journal of Finance* | Mid | What HFTs actually did during the May 2010 Flash Crash, using regulator trade data. |

## Execution and algorithmic trading

| Book | Level | What it gives you |
| --- | --- | --- |
| *Algorithmic Trading and DMA* (2010), Barry Johnson | Intro‚ÄìMid | How orders move from strategy to exchange: order books, execution algorithms (VWAP, TWAP, implementation shortfall), transaction costs and direct market access infrastructure. |
| *Algorithmic and High-Frequency Trading* (2015), Cartea, Jaimungal & Penalva | Advanced | Rigorous models for optimal execution and market making using stochastic control. The natural next step after Avellaneda-Stoikov. |
| *Advances in Financial Machine Learning* (2018), Marcos L√≥pez de Prado | Advanced | How to apply ML to financial data without fooling yourself: labelling, backtest overfitting, feature importance. |

## Options and volatility

| Book | Level | What it gives you |
| --- | --- | --- |
| *Option Volatility and Pricing* (2nd ed., 2015), Sheldon Natenberg | Intro‚ÄìMid | The standard practitioner's introduction: pricing models, the Greeks, volatility, spreads and risk management. Widely used to train new option traders. |
| *Options, Futures and Other Derivatives*, John Hull | Intro‚ÄìMid | The standard textbook reference for derivatives. Broad and clear; better for looking things up than reading cover to cover. |
| *Paul Wilmott Introduces Quantitative Finance*, Paul Wilmott | Mid | A readable introduction to derivatives maths and the Black-Scholes framework. |
| *Volatility Trading* (2nd ed., 2013), Euan Sinclair | Mid | How to forecast volatility and trade it in practice, including position sizing. |
| *Dynamic Hedging* (1997), Nassim Nicholas Taleb | Mid‚ÄìAdvanced | A trader's view of managing options books: the Greeks in practice and where models break down. |
| *The Volatility Surface* (2006), Jim Gatheral | Advanced | How implied volatility varies by strike and expiry, and the models used to fit it. |

## Digital assets

| Source | Level | Key idea |
| --- | --- | --- |
| Nakamoto, "Bitcoin: A Peer-to-Peer Electronic Cash System" (2008) | Intro | The original whitepaper. Nine pages; worth reading once. |
| BitMEX perpetual swap documentation | Intro | Explains the perpetual future: a futures contract with no expiry, kept close to spot by periodic funding payments between longs and shorts. Now the most traded crypto derivative. |
| Uniswap v3 whitepaper (2021) | Mid | Automated market makers with concentrated liquidity, where liquidity providers choose a price range. Useful for seeing how on-chain liquidity differs from a limit order book. |
| Daian et al., "Flash Boys 2.0: Frontrunning, Transaction Reordering, and Consensus Instability in Decentralized Exchanges" (IEEE S&P 2020) | Mid | How bots front-run DeFi trades by bidding for transaction ordering. Introduced the term MEV (miner/maximal extractable value). |
| Deribit API documentation and testnet | Intro‚ÄìMid | The main crypto options venue. The testnet lets you practise placing options orders without real money. |

## Maths, probability and statistics

A range from refresher material to quant-level depth. Checking textbook problems with short Python Monte Carlo simulations is a good way to build intuition.

| Resource | Level | Why it's here |
| --- | --- | --- |
| 3Blue1Brown, *Essence of Linear Algebra* (YouTube) | Intro | Visual intuition for vectors, matrices and eigenvalues. A quick refresher. |
| StatQuest with Josh Starmer (YouTube) | Intro | Short, clear videos on core statistics: distributions, hypothesis tests, regression. Good for commute revision. |
| MIT 6.0002 (*Introduction to Computational Thinking and Data Science*), Monte Carlo lectures | Intro | Free lectures; a gentle, code-first introduction to simulation. |
| Harvard Stat 110 with Blitzstein & Hwang, *Introduction to Probability* | Intro‚ÄìMid | The best foundational probability course. Lectures and problem sets are free online. |
| Mosteller, *Fifty Challenging Problems in Probability* | Mid | Short puzzles for building speed and intuition. |
| Zhou, *A Practical Guide to Quantitative Finance Interviews* (the "green book") | Mid | Interview-style problems in probability, brain teasers and finance. |
| Capinski & Zastawniak, *Mathematics for Finance* | Mid | A compact introduction to the maths of pricing, from interest rates to options in discrete time. Small enough to read on a commute. |
| Ross, *Introduction to Probability Models* | Mid | Stochastic processes: Markov chains, Poisson processes, queueing. |
| Wasserman, *All of Statistics* | Mid‚ÄìAdvanced | A dense, fast tour of statistics and inference for people with some maths. |
| Owen, *Monte Carlo Theory, Methods and Examples* | Mid‚ÄìAdvanced | Error estimation and variance reduction. Pairs well with building a Monte Carlo option pricer. |
| Shreve, *Stochastic Calculus for Finance I* | Advanced | Discrete-time option pricing (binomial model); the bridge into continuous-time finance. |
| Glasserman, *Monte Carlo Methods in Financial Engineering* | Advanced | The reference text for simulation in derivatives pricing. |

## Engineering and infrastructure

| Resource | Level | Why it's here |
| --- | --- | --- |
| *Designing Data-Intensive Applications*, Martin Kleppmann | Mid | Not a finance book, but the best guide to the data systems (streams, replication, consistency) that trading platforms are built on. |
| *Terraform: Up & Running*, Yevgeniy Brikman, plus HashiCorp's own tutorials | Intro‚ÄìMid | Infrastructure as code: provisioning repeatable environments for trading and data systems. |
| Adrian Cantrill's AWS courses (learn.cantrill.io) | Intro‚ÄìAdvanced | Thorough, architecture-focused AWS training. The AWS Organizations and multi-account material is useful for setting up regulated, segregated environments. |

## Hands-on project ideas

Small builds that turn the reading into something concrete. Each can be provisioned with Terraform and deployed through a CI/CD pipeline.

1. **Market data pipeline:** stream trades and order book updates from a crypto exchange's WebSocket feed into Kinesis, then land them in S3 for analysis.
2. **Options pricer as a service:** a Black-Scholes pricer with Greeks on Lambda behind API Gateway. Extend it with a Monte Carlo pricer and compare the two.
3. **Order management system:** a minimal OMS that places, amends and cancels orders on a crypto exchange's test environment and tracks positions.
4. **Options lab:** place small options trades on the Deribit testnet and watch how the Greeks and P&L move as the underlying changes.

