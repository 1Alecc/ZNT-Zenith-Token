# ZNT Burn Registry

> Public record of every ZNT burn event.
> Each entry links the on-chain transaction to the original trade record.
> Updated after every verified payout from a funded account.

---

## Summary

| Metric | Value |
|---|---|
| Total burns executed | 0 |
| Total ZNT burned | 0 |
| Total supply burned (%) | 0% |
| Current supply | 21,000,000 ZNT (pre-launch) |
| First burn | Pending mainnet deploy (2027) |

---

## Burn Log

*No burns recorded yet. ZNT mainnet deploy is planned for 2027.*

*Once live, every burn will appear here with:*
- *Etherscan transaction link*
- *ZNT amount burned*
- *USD P&L that triggered the burn*
- *SHA-256 hash of the original FIX ExecutionReport*
- *The 5%ers trade record link for independent verification*

---

## How Burns Work

```
1. Zenith executes a profitable trade on a funded account
2. Prop firm independently verifies and issues payout
3. FIX Oracle Bridge detects the ExecutionReport (Tag 35=8)
4. Bridge generates signed attestation with SHA-256 of the FIX message
5. BuybackBurn.sol receives attestation, validates ECDSA signature
6. Contract swaps USDC -> ZNT on DEX (Uniswap)
7. All purchased ZNT sent to 0x000000000000000000000000000000000000dEaD
8. BurnExecuted event emitted on-chain
9. This registry is updated
```

---

## Verification Guide

To independently verify any burn:

**Step 1:** Find the transaction on Etherscan
```
https://etherscan.io/address/[ZNT_CONTRACT_ADDRESS]
-> Events -> BurnExecuted
```

**Step 2:** Note the `tradeRecordHash` field (bytes32)

**Step 3:** Go to The 5%ers dashboard and locate the trade by date and amount

**Step 4:** Download the trade confirmation or payout PDF

**Step 5:** Compute SHA-256 of the original document and compare
```bash
sha256sum trade_confirmation.pdf
# Must match tradeRecordHash from the on-chain event
```

If the hashes match: the burn is verified. The profit was real.

---

## Live Tracking (Available After Mainnet Deploy)

- Etherscan: `[contract address — pending deploy]`
- ZNT Dashboard: `[pending]`
- Dune Analytics: `[pending]`

---

*ZNT Burn Registry — updated after every verified payout*
*ZNT — The Zenith Token | Proof of Alpha Protocol*
