# ZNT — The Zenith Token

> *The first deflationary token whose supply reduction is triggered by verified algorithmic trading performance.*

**Total supply:** 21,000,000 ZNT — fixed forever. No mint. Only burn.
**Live trading since:** April 22, 2026
**Protocol:** [Proof of Alpha](https://github.com/1Alecc/Proof-Of-Alpha-ZNT)
**Status:** Pre-launch — track record accumulation phase

---

## What Is ZNT?

ZNT is the canonical implementation of the **Proof of Alpha Protocol** — a new tokenomics primitive where a token's deflation is mathematically bound to externally-verified trading performance.

Every time **Zenith** — a proprietary multi-brain algorithmic trading system — generates verified profit on a funded account, 30% of that profit is used to buy ZNT on the open market and send it permanently to the dead address.

No promises. No roadmap speculation. Just math on top of verified results.

```
Zenith generates alpha
        |
Prop firm independently verifies and pays out
        |
30% of payout -> buy ZNT on DEX
        |
100% of purchased ZNT -> 0x000...dead
        |
Supply decreases permanently
        |
BurnExecuted event on-chain with hash of original trade record
```

---

## Why ZNT Is Different

Most tokens are backed by:
- Promises ("we will build X")
- Protocol usage (collapses when usage drops)
- Inflation disguised as yield

ZNT is backed by:
- A trading system operating live since **April 22, 2026**
- Independent verification by regulated prop firms (The 5%ers)
- Institutional-grade oracle: FIX Protocol — the messaging standard of institutional finance since 1992
- An on-chain audit trail linking every burn to its original trade record

**The backing is not a promise. It is a track record.**

---

## The Numbers

| Property | Value |
|---|---|
| Total supply | 21,000,000 ZNT |
| Burn per payout | 30% of verified profit |
| Reinvestment | 40% -> new funded accounts |
| Founder allocation | 20% (1yr cliff + 3yr vesting) |
| Public sale | 25% |
| Planned launch | 2027 (after 12+ months of live track record) |

Every new funded account Zenith connects to is an additional burn engine.
The deflation rate compounds with scale.

---

## How to Verify a Burn

Every burn event emits `BurnExecuted` on Ethereum mainnet:

```solidity
event BurnExecuted(
    uint256 pnlUSD,           // Verified P&L that triggered this burn
    uint256 zntBurned,        // ZNT permanently destroyed
    uint256 supplyAfter,      // Supply remaining after this burn
    bytes32 tradeRecordHash,  // SHA-256 of the original FIX ExecutionReport
    uint256 sequenceId,       // FIX sequence number (anti-replay)
    address indexed oracle
);
```

To verify any burn:
1. Find the `BurnExecuted` event on Etherscan
2. Copy the `tradeRecordHash`
3. Compare against the trade record on The 5%ers dashboard
4. The SHA-256 of the original FIX message must match

The chain of evidence is unbreakable. See [BURNS.md](BURNS.md) for the live registry.

---

## The Engine — Zenith Corp

Zenith is a 10-brain consensus trading system (Decagon V12.7) built entirely by Samuel Imbrecht, 16, from Valledupar, Colombia.

It operates continuously on MetaTrader 5, analyzing XAUUSD, XAGUSD, BTCUSD, ETHUSD, NAS100, XTIUSD, and DAX40 through ten independent analytical engines that vote on every trade:

- **TitanAI** — LightGBM ML, 49 engineered features
- **DeepNet** — BiLSTM + Attention, GPU-accelerated
- **Lazarus** — Institutional order flow and VSA
- **DXY Guard** — Dollar strength via ICE formula
- **VolProfile** — Volume Profile: POC/VAH/VAL/HVN/LVN
- **Ares AI** — Dynamic trade manager (break-even, trailing, zombie exit)
- **Entropy AI** — Black swan veto and circuit breaker
- *...and four more*

The algorithm is private. The results are public.

---

## Current Status

| Component | Status |
|---|---|
| Zenith trading system | Live since April 22, 2026 |
| The 5%ers Bootcamp $25k | Active |
| Proof of Alpha Protocol | Published April 27, 2026 |
| ZNT smart contract | In development — deploy planned 2027 |
| FIX Oracle Bridge | Planned 2027-2028 |
| First burn event | Pending mainnet deploy |

---

## Roadmap

See [ROADMAP.md](ROADMAP.md) for the full timeline.

---

## Protocol Specification

ZNT implements the Proof of Alpha Protocol.
Full technical specification, smart contracts, and oracle interface:
**https://github.com/1Alecc/Proof-Of-Alpha-ZNT**

---

## Legal

ZNT is a deflationary utility token. It does not represent equity, profit sharing, dividends, or investment returns of any kind. This repository is for informational purposes only and does not constitute a securities offering or financial advice. Acquiring ZNT involves substantial risk including total loss of capital. Consult a qualified legal and financial advisor before any decision.

---

*ZNT — The Zenith Token*
*First defined: April 27, 2026*
*Canonical Proof of Alpha implementation*
*Samuel Esteban Imbrecht Bermudez — Zenith Corp*
