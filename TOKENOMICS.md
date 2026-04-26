# ZNT Tokenomics

> Supply, distribution, burn mechanism, and deflation model.

---

## Supply

| Property | Value |
|---|---|
| Total supply | 21,000,000 ZNT |
| Additional issuance | Impossible — no mint function |
| Supply direction | Only downward |

The 21M cap is a direct reference to Bitcoin's fixed supply as a founding principle.
Once deployed, no force in the world can increase the supply of ZNT.

---

## Distribution

| Allocation | % | ZNT | Notes |
|---|---|---|---|
| ZPF Treasury | 40% | 8,400,000 | Buybacks, operations, reserve |
| Founder | 20% | 4,200,000 | 1yr cliff + 3yr linear vesting |
| Public Sale | 25% | 5,250,000 | Initial liquidity |
| Ecosystem / Partners | 10% | 2,100,000 | Prop firms, brokers, integrations |
| Legal Reserve | 5% | 1,050,000 | Audits, compliance, legal structure |

**Founder vesting:** no token can be sold before the project demonstrates real utility.
The contract enforces this mathematically — it is not a promise.

---

## Burn Mechanism

Every payout from a Zenith-operated funded account is split:

```
30% -> Buy-Back & Burn ZNT (permanent supply reduction)
40% -> ZPF Treasury (fund new funded accounts)
20% -> Operational Reserve (infrastructure, legal, development)
10% -> Founder (personal income — no token sales required)
```

The burn is not managed — it is mechanical.
It does not require any action from the team after the oracle is live.

### Self-correcting deflation

When ZNT price falls:
- The same USD amount purchases more ZNT
- More ZNT burned per event
- Deflation accelerates when price is low
- This mechanically supports the price floor

There is no death spiral. Burn rate depends on Zenith's P&L —
completely independent of the crypto market.

---

## Burn Projections

*Assuming ZNT launch price of $0.10:*

| Scenario | Monthly Payout | Monthly Burn (USD) | ZNT Burned/Month |
|---|---|---|---|
| Conservative (1 account) | $1,200 | $360 | ~3,600 |
| Moderate (3 accounts) | $3,500 | $1,050 | ~10,500 |
| Optimal (10 accounts) | $15,000 | $4,500 | ~45,000 |

### Compounding effect

Each new funded account Zenith connects to is an additional burn engine.
The Treasury (40%) accumulates specifically to purchase new accounts.
At 3+ active accounts, the Treasury accumulates faster than the cost of a new account —
the number of active accounts grows exponentially, not linearly.

| Month | Active Accounts | Monthly Payout | ZNT Burned/Month |
|---|---|---|---|
| 1 | 1 ($25k) | ~$1,200 | ~3,600 |
| 6 | 2 ($50k) | ~$2,800 | ~8,400 |
| 12 | 4 ($100k) | ~$6,000 | ~18,000 |
| 24 | 8 ($200k) | ~$13,000 | ~39,000 |
| 36 | 16 ($400k) | ~$28,000 | ~84,000 |

At 36 months: approximately **500,000 ZNT burned** (-2.4% of total supply).

---

## Launch Price

| Metric | Value |
|---|---|
| Suggested launch price | $0.05 - $0.10 per ZNT |
| Market cap at launch (public sale) | ~$262,500 - $525,000 |
| Fully diluted valuation | ~$1,050,000 - $2,100,000 |

The FDV is intentionally conservative. ZNT does not launch on speculation —
it launches with 12+ months of verified trading track record behind it.

---

*ZNT Tokenomics V1.0 — April 27, 2026*
*ZNT — The Zenith Token | Proof of Alpha Protocol*
