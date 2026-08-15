# DOCUMENT 004 — LP LADDER & FLYWHEEL
## Execution on Meteora DLMM · Distribution on Real Yield

> *Real yield is the only chip for perpetual operation.*
> *This document defines how liquidity is deployed (the ladder) and how profit is divided (the flywheel).*

### 1. THE EXECUTION ENGINE

Liquidity is deployed on **Meteora DLMM** — discrete, fixed-price bins with zero slippage inside each bin. The 99% ladder uses the **Bid-Ask single-sided strategy**: pure-token sell-side depth laid bin by bin above the current price. Price therefore climbs one bin at a time — a staircase, not a wick.

### 2. THE TWO POOLS (10M GENESIS LP)

The 10M Genesis LP *(see Document 001, §4)* splits into two engines:

* **1% Pricing Pool (100,000)** — a dual-sided pool (token + seed USDC) that anchors the initial price P0.
* **99% Ladder Pool (9,900,000)** — pure-token sell-side depth distributed from P0 to 10×P0.

### 3. THE 10x IS A LADDER WIDTH, NOT A PROMISE

The ladder's top is the mathematical reciprocal of Q1's emission rate: `100% ÷ 10% = 10x`. This is a **design parameter for depth**, endogenous to the release curve — not a price target. The market, not the protocol, decides whether it is reached *(see Document 002, §6)*.

### 4. BUY-THROUGH PRESSURE MATH

The calculable quantity is the USDC required to consume the ladder:

```
USDC to consume = Ladder Tokens × P0 × √M        (M = ladder top ÷ P0)
```

Conversely, given buying pressure X, the multiplier reached is:

```
M = ( X ÷ (Ladder Tokens × P0) )²
```

*√M is the geometric mean of 1 and M — the average price at which the ladder sells.*

**Illustrative:** 9,900,000 tokens at P0 = $0.005, M = 10 → USDC ≈ 9.9M × 0.005 × 3.162 ≈ **$156,500** of real demand to push the ladder to 10x. This is a stress-test tool, not a forecast.

### 5. THE PROFIT FLYWHEEL (70/10/10/10)

Official LP profit is never extracted; it is generated and divided, in the open:

| Flow | Share | Destination |
| :--- | :--- | :--- |
| Compounding | 70% | Auto-deepens liquidity (the flywheel) |
| Vision Rail | 10% | Architect royalty (permanent) |
| Labor Rail | 10% | Builders & auditors (per milestone) |
| Angel Rail | 10% | Early patrons (genesis NFT holders) |

### 6. THE RAILS ARE FLOW-CLAIMS ONLY

Every rail is a claim on **profit flow**, never on the fixed base. No rail mints, no rail sells the base, no rail vests insider tokens. If the pool does not earn, no rail pays. *No work, no fish.*

### 7. COVENANT

* The ladder is depth, not a price promise.
* The flywheel compounds first, divides second.
* Rails are paid only from real yield, in the open, on-chain.

— **JackerArchitect.b5FH**

---

**JackerArchitect** — Independent System Architect
Web · jackerteo.com
X · @JackerArchitect

*The equations can be copied. The philosophy cannot. We build for equality. We build for eternity.*
