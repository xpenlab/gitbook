# Platform Overview

## What is Taolend?

> Taolend is a peer-to-peer (P2P) lending platform built on the Bittensor EVM chain, focused on facilitating lending between TAO and ALPHA tokens.

## Core Features

### P2P Offer Matching Mechanism

Taolend uses a distinctive P2P offer-based matching model:

- **Lenders Create Offers**: Freely define interest rates, amounts, collateral requirements, and other terms
- **Borrowers Select Offers**: Browse the market and choose offers with the best conditions
- **Peer-to-Peer Lending**: Every loan establishes a direct, transparent relationship between a lender and a borrower

### Lending Assets

- **Lent Asset**: TAO (Bittensor native token)
- **Collateral**: ALPHA (Bittensor subnet token)

### Key Parameters

| Parameter | Description |
|-----------|-------------|
| Minimum Loan Amount | 1 TAO |
| Collection Protection Period | 3 days (21,600 blocks) |
| Collection Grace Period | 3 days (21,600 blocks) after entering collection |
| Daily Interest Rate Range | 0.01% – 1% * |
| Protocol Fee | 30% of interest (70% to lenders) |
| Safety Margin | 90% of ALPHA price |

> Loans cannot be collected or liquidated within the first 3 days. 
> After this period, lenders are allowed (but not forced) to initiate collection.

\* Interest is calculated per block. 1 day = 7,200 blocks.

## How It Works

### Lenders

1. Deposit TAO into the contract
2. Create offers using offline signatures (no on-chain transaction required)
3. Wait for borrowers to accept the offer
4. Earn interest automatically while the loan is active
5. Withdraw principal and interest after repayment

### Borrowers

1. Deposit ALPHA as collateral
2. Browse available offers in the marketplace
3. Select the best offer and initiate the loan
4. Receive TAO liquidity instantly
5. Repay at any time or refinance to optimize costs

## Get Started

- 📖 [Quick Start](quick-start.md) – Get up to speed in 5 minutes
- 💡 [Core Functions](core-features/README.md) – Explore the platform mechanics in depth
- ❓ [FAQ](faq.md) – Answers to frequently asked questions  