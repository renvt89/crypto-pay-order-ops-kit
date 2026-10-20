# Crypto-Pay Order Ops Kit (teaser)

This kit is an order ledger CLI and a set of customer message templates for sellers of digital goods or services who accept stablecoin payments, such as USDT on BEP-20.

## The problem
Every stablecoin order raises the same questions:
- Did the buyer pay the exact amount?
- Was the payment sent on the right network?
- Was the order delivered?
- What do you tell a buyer who underpaid?

## What the full kit contains
- **order-ops.mjs**: a Node 18+ CLI with zero dependencies and no network calls. Its commands are `new`, `mark-paid`, `mark-underpaid`, `refund`, `deliver`, `expire` and `report`. It keeps a plain `orders.csv` ledger and refuses to deliver any order that is not marked paid.
- **5 customer message templates**:
  - payment instructions, with warnings about the wrong network and about address swaps
  - payment received
  - underpaid
  - expired
  - refund policy
- **CHECKLIST.md**: a 5-minute daily routine for checking payments on a public block explorer. For each payment you check:
  - the token contract (to catch fake USDT)
  - the exact amount
  - the network
  - the confirmations
  - the tx hash

## Honest limits
- The CLI does **not** verify payments on-chain. You check each transaction yourself on a public block explorer and then mark it paid.
- The kit covers order operations only. It is not trading software and not a wallet. It is not financial, legal or tax advice.
- It never asks for private keys or seed phrases.

## Status
The full kit goes on sale as a fixed $19 download on Gumroad, and this README will link to the listing once it is live.

Built by Rene Vergara.
