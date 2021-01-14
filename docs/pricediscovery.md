---
id: pricediscovery
title: Price Discovery
sidebar_label: Price Discovery
slug: /whitepaper/pricediscovery
---

The term, "price discovery", is a very broad term. When used in the realm of traditional financial markets, the term is generally used to refer to the passive act of observing prices trades occur at. There are three assumptions behind this:

1. There is enough trade liquidity for an accurate price to be generated.
2. The price is observed in realtime. For example, 15-minute delated prices are probably no longer accurate in a volatile market.
3. Participants in the observed markets act in realtime to correct short-term trade imbalances.

### Order Books

In traditional financial markets the term price discovery means passively observing prices that result from trading activity. The conventional order book can be viewed as a centralized price consensus mechanism that depends on the concentration of order flow into a single matching engine, to ensure trades execute at the best bid or ask. The accuracy of prices generated from an order book is dependent on the volume of trading activity and as such is highly sensitive to short term imbalances in supply and demand. As an example, during a price runup or selloff **the best bid or ask on an order book does not necessarily reflect an accurate consensus price**, hence the tendency for order books to mean revert after the short-term supply / demand imbalance corrects.

### Decentralized Exchanges (DEX)

Order books have been adapted to decentralized blockchain technology by moving the matching engine into an on-chain smart contract but it doesn't always work as intended, with issues like front running still being possible at the miner or validator level and price spreads staying large due to uncertainty from block times and price discrepancies, information latency and order flow imbalances from different geographic areas.

### Automated Market Makers (AMM)

Automated market makers improve on the order book as a decentralized trading mechanism by adding market maker functionality into the on-chain logic, substituting a bonding curve to approximate a natural supply / demand pricing curve. The result is a **trading engine** well adapted to blockchain technology but as a **price consensus mechanism** it is still highly sensitive to short term imbalances in supply and demand, just like the order book is. In fact, the AMM relies almost entirely on short-term price volatility for its price discovery since there are no fixed bids or asks like on an order book.

### Schelling Point Consensus

The Microtick project creates a stable mechanism for price discovery that does not rely on order flow or short-term price volatility to reach consensus. It does this using a Schelling point mechanism similar in spirit to blockchain oracle pools but with a consensus price that dynamically adjusts block by block in realtime, and one that **can be hedged financially**. Because the resulting consensus price is an average, it will tend to be more stable than an order book or automated market maker. In addition, it will tend to create an accurate, convergent consensus price even on assets that are not actively traded.
