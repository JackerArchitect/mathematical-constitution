# DOCUMENT 002 — THE RELEASE MATH
## The √q Curve: Unlocking the Base Over 49 Seasons

> *The protocol chooses supply. The market chooses price.*
> *This document defines how the fixed base is unlocked. It does not — and cannot — define what the market will pay.*

### 1. UNLOCK, NOT MINT

Everything in this document draws from the fixed base of 100,000,000 *(see Document 001)*. The release track only **unlocks existing supply**; it never mints. The separate elastic mint that rewards stakers is a different source and never touches this base *(see Document 003)*.

### 2. THE CURVE

Cumulative release at quarter *q* is a single square-root function:

```
Cumulative Release(q) = 10,000,000 × √q
```

The marginal release in any quarter is therefore `10,000,000 × (√q − √(q−1))` — large early, decelerating forever.

### 3. WHY √q

* **Front-loaded, but not a cliff.** Early seasons release more to seed liquidity and discovery; the flow then thins into a long tail.
* **Predictable.** Anyone can compute any quarter's release with one line of math. No dynamic modifiers, no gameable parameters, no whale-tunable knobs.
* **Digestible.** The decelerating flow lets demand absorb supply without shocks.

### 4. THE SCHEDULE (70M UNLOCK POOL)

| Quarter | √q | Cumulative Release | Remaining Pool |
| :--- | :--- | :--- | :--- |
| Q1 | 1 | 10,000,000 | 60,000,000 |
| Q4 | 2 | 20,000,000 | 50,000,000 |
| Q9 | 3 | 30,000,000 | 40,000,000 |
| Q16 | 4 | 40,000,000 | 30,000,000 |
| Q25 | 5 | 50,000,000 | 20,000,000 |
| Q36 | 6 | 60,000,000 | 10,000,000 |
| Q49 | 7 | 70,000,000 | 0 |

*Q1's 10M is the Genesis LP deployed at launch; Q2–Q49 drip the remaining 60M. Exhausted exactly at Q49.*

### 5. DEMAND-DRIVEN DRIP & BUFFER VAULT

The curve sets a **ceiling**, not a guaranteed dump. Within a quarter, tokens are drip-fed by real demand; anything not absorbed routes to the Buffer Vault and stays locked until utility requires it *(see Document 001, §3)*. Supply therefore expands only as fast as the network is used.

### 6. WHAT THE CURVE DOES NOT DO

It does not set price. The release schedule shapes **supply**; price is discovered where demand meets that supply on the liquidity curve *(see Document 004)*. Anyone promising a per-season price target is selling fiction. We publish supply math and nothing else.

### 7. COVENANT

* The curve is immutable: one function, no knobs.
* Release is a ceiling, drip-fed by demand, buffered by the vault.
* The base is exhausted at Q49 and never re-inflated.

— **JackerArchitect.b5FH**

---

**JackerArchitect** — Independent System Architect
Web · jackerteo.com
X · @JackerArchitect

*The equations can be copied. The philosophy cannot. We build for equality. We build for eternity.*
