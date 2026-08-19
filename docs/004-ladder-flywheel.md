# DOCUMENT 004 — LP LADDER & FLYWHEEL
## Execution on Meteora DLMM · Distribution on Real Yield

> *Real yield is the only chip for perpetual operation.*
> *This document defines how liquidity is deployed (the ladder) and how profit is divided (the flywheel).*

### 1. THE EXECUTION ENGINE

Liquidity is deployed on **Meteora DLMM** — discrete, fixed-price bins with zero slippage inside each bin. The sell-side depth uses a single-sided strategy: pure-token liquidity laid bin by bin above the current price. Price therefore climbs one bin at a time — a staircase, not a wick.

### 2. THE TWO POOLS (GENESIS LP)

The Genesis LP *(see Document 001)* splits into two engines:

* **Pricing Pool** — a dual-sided pool (token + seed USDC) that anchors the initial price P0.
* **Ladder Pool** — pure-token sell-side depth distributed from P0 upward to a defined upper boundary.

### 3. THE LADDER IS DEPTH, NOT A PRICE PROMISE

The ladder's upper boundary is a **design parameter for depth**, endogenous to the release curve — not a price target. The market, not the protocol, decides the price trajectory *(see Document 002, §6)*.

### 4. BUY-THROUGH PRESSURE MATH

The calculable quantity is the USDC required to consume the ladder depth:

> `USDC to consume = Ladder Tokens × P0 × √M`  (M = upper boundary ÷ P0)

Conversely, given buying pressure X, the multiplier reached is a function of that pressure against the locked token supply. 

*√M is the geometric mean — the average price at which the ladder sells.*

This is a stress-test tool for liquidity engineering, not a forecast.

### 5. THE APPRECIATION ENVELOPE (49 QUARTERS)

A suggested per-quarter appreciation multiplier, applied cumulatively to P0. It is a **liquidity-engineering parameter for bin placement** — a suggested ceiling, not a floor, not a target, and never a promise. The protocol never defends a price. **The market chooses price.**

| Q | ×Q | Cum ×P0 |
| :--- | :--- | :--- |
| 1 | 5.00 | 5.00 |
| 2 | 2.00 | 10.00 |
| 3 | 1.80 | 18.00 |
| 4 | 1.70 | 30.60 |
| 5 | 1.60 | 48.96 |
| 6 | 1.50 | 73.44 |
| 7 | 1.40 | 102.82 |
| 8 | 1.30 | 133.66 |
| 9 | 1.20 | 160.39 |
| 10 | 1.10 | 176.43 |
| 11 | 1.09 | 192.31 |
| 12 | 1.08 | 207.70 |
| 13 | 1.07 | 222.22 |
| 14 | 1.06 | 235.56 |
| 15 | 1.05 | 247.34 |
| 16 | 1.04 | 257.23 |
| 17 | 1.03 | 264.95 |
| 18 | 1.02 | 270.25 |
| 19 | 1.02 | 275.65 |
| 20 | 1.02 | 281.16 |
| 21 | 1.02 | 286.79 |
| 22 | 1.02 | 292.52 |
| 23 | 1.02 | 298.37 |
| 24 | 1.02 | 304.34 |
| 25 | 1.02 | 310.43 |
| 26 | 1.02 | 316.64 |
| 27 | 1.02 | 322.97 |
| 28 | 1.02 | 329.43 |
| 29 | 1.02 | 336.02 |
| 30 | 1.02 | 342.74 |
| 31 | 1.02 | 349.59 |
| 32 | 1.02 | 356.58 |
| 33 | 1.02 | 363.71 |
| 34 | 1.02 | 370.99 |
| 35 | 1.02 | 378.41 |
| 36 | 1.02 | 385.98 |
| 37 | 1.02 | 393.70 |
| 38 | 1.02 | 401.57 |
| 39 | 1.02 | 409.60 |
| 40 | 1.02 | 417.79 |
| 41 | 1.02 | 426.15 |
| 42 | 1.02 | 434.67 |
| 43 | 1.02 | 443.37 |
| 44 | 1.02 | 452.23 |
| 45 | 1.02 | 461.28 |
| 46 | 1.02 | 470.50 |
| 47 | 1.02 | 479.91 |
| 48 | 1.02 | 489.51 |
| 49 | 1.02 | 499.30 |

**Phases:** I. Genesis Surge (Q1–Q2) · II. Glide Decay (Q3–Q10) · III. Fine Decay (Q11–Q17) · IV. Maturity (Q18–Q49, 1.02 ≡ ~8.24% annualized).

**Internal checkpoints** map the geometric decay of the multiplier. If the market exceeds the envelope, the protocol does not chase; if it lags, the protocol does not defend. The envelope structures depth — nothing more.

### 6. THE PROFIT FLYWHEEL (70/10/10/10)

Official LP profit is never extracted; it is generated and divided, in the open:

| Flow | Share | Destination |
| :--- | :--- | :--- |
| Compounding | 70% | Auto-deepens liquidity (the flywheel) |
| Vision Rail | 10% | Founder |
| Builders Rail | 10% | Team (code & audits) |
| Project Fund | 10% | Future development & real-world deployment |

Every rail is a claim on profit flow only — never on the base.

### 7. THE RAILS ARE FLOW-CLAIMS ONLY

Every rail is a claim on **profit flow**, never on the fixed base. No rail mints, no rail sells the base, no rail vests insider tokens. If the pool does not earn, no rail pays. *No work, no fish.*

### 8. COVENANT

* The ladder is depth, not a price promise.
* The flywheel compounds first, divides second.
* Rails are paid only from real yield, in the open, on-chain.

— **JackerArchitect.b5FH**

---

**JackerArchitect** — Independent System Architect
Web · jackerteo.com
X · @JackerArchitect

*The equations can be copied. The philosophy cannot. We build for equality. We build for eternity.*
