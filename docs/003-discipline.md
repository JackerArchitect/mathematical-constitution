# DOCUMENT 003 — CAPITAL DISCIPLINE
## The Two 49s: Macro Decay, Micro Fractal

> *Mercenaries pay the tax. Believers reap the reward.*
> *This document defines the discipline layer: how yield decays over 49 seasons, and how capital is locked, slashed, and rewarded over 49 days.*

### 1. THE STAKING SOURCE (TRACK B)

Staking rewards are **newly minted** — an elastic supply that exists entirely outside the fixed 100M base *(see Documents 001–002)*. They never dilute the base and never draw from it.

A staker's yield is one line of math:

```
Reward = Staked Amount × Current-Season APY
```

### 2. THE MACRO: 49-SEASON APY STAIRCASE

Yield decays linearly from 98% to 5% across 49 quarters (12.25 years):

```
APY_q = 5% + 93% × (49 − q) ÷ 48
```

| Quarter | APY |
| :--- | :--- |
| Q1 | 98.00% |
| Q4 | 92.19% |
| Q9 | 82.50% |
| Q16 | 68.94% |
| Q25 | 51.50% |
| Q36 | 30.19% |
| Q49 | 5.00% |

Early seasons pay for conviction; late seasons pay for utility. The staircase is fixed — no dynamic modifiers, no gameable knobs.

### 3. THE MICRO: 49-DAY MATURATION & TIERED SLASHING

Every staked position enters a **49-day maturation**. Exiting early triggers a penalty applied to **both the principal and the accrued rewards**:

| Window | Slash |
| :--- | :--- |
| Day 1–7 (Mercenary) | 30% |
| Day 8–14 (Speculator) | 14% |
| Day 15–30 (Transition) | 7% |
| Day 31–48 (Symbolic) | 3% |
| Day 49 (Full Maturity) | 0% |

The penalty decays as commitment deepens. At Day 49, the position is fully free.

### 4. POST-MATURITY AUTO-COMPOUNDING

Reaching Day 49 removes the penalty **permanently**. An untouched position keeps earning and auto-compounds. Before maturity: decaying friction. After maturity: accelerating compounding.

### 5. LOYALTY BONUS REDISTRIBUTION

Slashed tokens are **never burned and never sent to the treasury**. They are pooled and redistributed pro-rata, as a bonus, to every staker who remains. Every mercenary exit directly funds the loyal.

### 6. THE FRACTAL PRINCIPLE

The micro mirrors the macro: **49 days of discipline inside 49 seasons of decay**. Long-term capital is rewarded at every structural layer; short-term capital is taxed at every structural layer.

### 7. COVENANT

* Yield is minted, never taken from the base.
* Slashing hits principal and rewards alike; it decays to zero at maturity.
* Slashed value goes to believers, not to the void.
* Both staircases are immutable.

— **JackerArchitect.b5FH**

---

**JackerArchitect** — Independent System Architect
Web · jackerteo.com
X · @JackerArchitect

*The equations can be copied. The philosophy cannot. We build for equality. We build for eternity.*
