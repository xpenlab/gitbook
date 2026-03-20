# Frequently Asked Questions

>This section compiles the most frequently asked questions from users. If you can’t find the answer you’re looking for here, please refer to the full documentation or reach out through official support channels.

---

## Platform Basics

### What is Taolend?

Taolend is a peer-to-peer (P2P) lending platform built on the Bittensor EVM chain, designed specifically for lending between TAO and ALPHA tokens:

- **Lenders**: Deposit TAO and create loan Offers to earn interest
- **Borrowers**: Collateralize ALPHA to borrow TAO and access liquidity
- **Leverage Traders**: Use TAO to open leveraged long positions on Alpha tokens
- **P2P Matching**: Lenders and borrowers are directly matched through the Offer mechanism

### How does Taolend work?

Taolend operates through a P2P Offer-based matching model:

1. **Lenders Create Offers**
   - Define lending terms such as Amount, Daily APR, and collateral requirements
   - Offers are signed offline
   - Signed Offers are listed publicly in the Market

2. **Borrowers Accept Offers**
   - Browse available Offers in the Market
   - The system automatically matches the Best Daily APR
   - Borrow with one click, and TAO is transferred immediately

3. **P2P Loan Relationships**
   - Each loan has a clearly defined lender and borrower
   - Interest is paid directly to the lender (after a 30% protocol fee)
   - Loans are repaid and managed independently

### Why use Taolend?

**For Lenders**:
- ✅ Earn predictable interest income (Daily APR: 0.01%–1%)
- ✅ Loans are protected by ALPHA collateral (90% safety margin)
- ✅ Create multiple Offers with different terms to diversify risk

**For Borrowers**:
- ✅ Retain long-term exposure to ALPHA
- ✅ Access TAO liquidity for other activities
- ✅ Repay or refinance at any time

**For Leverage Traders**:
- ✅ Boost your ALPHA position using borrowed TAO
- ✅ Control risk with adjustable leverage and slippage settings
- ✅ Close position at any time to lock in profits

### Is Taolend safe to use?

Taolend applies multiple layers of security:

**Security Features**:
- ✅ Funds are managed by audited smart contracts
- ✅ ALPHA collateral protects lenders
- ✅ Transparent and traceable P2P loan structure
- ✅ EIP-712 compliant signature verification

**Risk Warnings**:
- ⚠️ ALPHA price volatility
- ⚠️ Borrower default risk (mitigated by collateral)

**Fees Applied**:
- ✅ **Protocol Fee**: 30% of interest (lenders receive 70%)

---

## Account and Bridging

### Do I need to register an account?

Yes. Registration is required before using Taolend:

1. **Connect Wallet** (EVM-compatible, e.g. MetaMask)
2. **Sign a message**
3. **Confirm registration transaction**

📖 See: [Account Registration](account/registration.md)

### Which wallets are supported?

All EVM-compatible wallets are supported:
- MetaMask (recommended)
- WalletConnect
- Coinbase Wallet
- Other EVM wallets

### How do I bridge assets?

Taolend runs on the Bittensor EVM chain, so assets must be bridged first:

**Lenders**:
1. Bridge TAO for lending
2. Bridge an additional ~0.1 TAO for Gas

**Borrowers**:
1. Bridge ALPHA as collateral
2. Bridge ~0.05–0.1 TAO for Gas

**Estimated Time**: 10–30 seconds

📖 See: [Bridge Assets](account/bridge-assets.md)

### Can I use multiple wallets?

Yes. Each wallet address is treated as a separate account:
- Assets and history are isolated
- Easy switching between accounts
- No linking required

### What if I forget my password?

Taolend does not store passwords. Your wallet controls your account.

**Important**:
- Back up your mnemonic phrase securely
- Never share your private key
- Accounts cannot be recovered by the platform

---

## Deposits and Withdrawals

### Is there a minimum deposit?

There is **no minimum**, but due to Gas costs:
- Lenders are advised to deposit at least 10 TAO
- Borrowers should deposit sufficient ALPHA for their loan needs

### When are deposits available?

Deposits are available immediately after confirmation (usually **10–30 seconds**):
- Lenders can create Offers right away
- Borrowers can borrow immediately

### Can I withdraw at any time?

Yes, with the following constraints:

**Lenders**:
- Withdrawable Balance = Balance − Amount currently lent

**Borrowers**:
- Withdrawable Balance = Balance − Collateral Amount

### How long do withdrawals take?

Withdrawals are processed immediately after confirmation (around **10–30 seconds**).

### Why can’t I withdraw my full Balance?

**Lenders**:
- Some TAO is actively lent out

**Borrowers**:
- ALPHA is locked as collateral

📖 See: [Deposits and Withdrawals](account/deposit-withdraw.md)

---

## Lend (Lender)

### How do I become a lender?

1. Bridge TAO
2. Register an account
3. Deposit TAO
4. Create a Loan Offer

📖 See: [Lend](core-features/lend.md)

### What is a Loan Offer?

A Loan Offer defines the lending terms set by a lender:
- **Amount**: Maximum TAO to lend
- **Daily APR**
- **Subnet**: Accepted ALPHA Subnet
- **Maximum Acceptable Price**: ALPHA price cap
- **Expire in**: Offer validity period

**Key Characteristics**:
- ✅ Offline signature
- ✅ Immediately visible in the Market
- ✅ Can be cancelled on-chain

### Does creating an Offer cost Gas?

No. Creating a Loan Offer uses an offline signature and is Gas-free.

### Is there a limit on Offers?

No limit. You can create as many Offers as you like.

### How do I cancel an Offer?

1. Go to **Lend → Offers / Active**
2. Click **Cancel**
3. Confirm the transaction

### How do lenders earn interest?

```
Total Interest = Borrow Amount × Daily APR × Days
Lender Earnings = Interest × 70%
Protocol Fee = Interest × 30%
```

>💡 Interest is calculated per block (1 day = 7,200 blocks). Daily APR is shown for clarity.

### When can I collect collateral?

After the **3-day minimum loan period**:
- 0–3 days: Collection not allowed
- After 3 days: Collection can be initiated
- Collection window: 3 days
- After that: Collateral may be claimed

### What happens if a borrower defaults?

If repayment is not made after the collection window:
1. Click **Claim Interest / Withdraw Collateral**
2. ALPHA collateral is transferred to you

### When is interest credited?

Interest is credited immediately after repayment and added to your Balance.

---

## Borrow (Borrower)

### How do I borrow?

1. Bridge ALPHA and some TAO for Gas
2. Register
3. Deposit ALPHA
4. Go to **Borrow → Assets**
5. Accept a matched Offer

📖 See: [Borrow](core-features/borrow.md)

### What is the minimum Borrow Amount?

The minimum is **1 TAO**.

### How much TAO can I borrow?

```
Borrowable TAO = ALPHA amount × ALPHA price × 60% (depends on Offer)
```

A 90% price safety margin is applied.

### Is there a fixed loan term?

No fixed maturity, but:
- Minimum loan period: 3 days
- Collection period: 3 days
- Failure to repay results in full collateral loss

### Is collection automatic after 3 days?

No. After the 3-day minimum period, lenders are allowed to initiate collection, but it is never automatic.

### Can I repay early?

Yes:
- Interest accrues only for actual usage time
- No early repayment penalties
- Collateral unlocks immediately

### What if I don’t have enough TAO to repay?

1. Go to **Profile**
2. Click **Deposit**
3. Ensure sufficient Balance before clicking **Repay Loan**

### What is refinancing?

Refinancing replaces an active loan with a better Offer:
- Automatically closes the old loan
- Opens a new one in a single transaction
- Saves Gas and reduces interest

### How do I avoid liquidation?

- Repay within 3 days
- Monitor loan status
- Maintain sufficient TAO Balance
- Refinance if rates drop

### What happens if I’m overdue?

After collection ends:
- ❌ All ALPHA collateral is lost
- ❌ Collateral is transferred to the lender

---

## Leverage-Long

### What is Leverage-Long?

Borrow TAO against your ALPHA for leverage.

- You deposit TAO as collateral
- The platform borrows additional TAO on your behalf
- Combined TAO is used to buy Alpha tokens
- Purchased Alpha is held as collateral to secure the loan

📖 See: [Leverage-Long](core-features/leverage.md)

### What if a lender initiates collection on my position?

> ❗️ If you don't close your position in time, ALL ALPHA collateral will be forfeited to the lender. Act IMMEDIATELY if you see IN_COLLECTION!

Steps to close:
1. Go to **Trade → Active**
2. Click **Close** on your position
3. Confirm the transaction

Do not wait — monitor your positions closely at all times.

### Can I close my position at any time?

Yes. You can close your Leverage-Long position at any time:
- If the ALPHA price increases, closing your position returns your full collateral plus any accrued profits after the loan is repaid.
- If the ALPHA price drops, you can still recover your remaining collateral after the loan is repaid.

Closing early at a small loss is always better than waiting for liquidation.

### How do I get started with Leverage-Long?

1. Bridge TAO to your EVM account
2. Register and deposit TAO
3. Go to **Trade → Leverage-Long**
4. Set Collateral Amount, Leverage, and Slippage
5. Click **Open Long**

📖 See: [Leverage-Long Quick Start](quick-start-leverage.md)

---

## Risks and Security

### What are the main risks?

**Lenders**:
- Liquidity lock-up
- ALPHA price drops
- Borrower default

**Borrowers**:
- Full collateral loss on default
- Interest costs
- ALPHA price volatility

**Leverage Traders**:
- Full principal loss if position is not closed before grace period expires
- Alpha price volatility amplified by leverage
- Interest costs on borrowed TAO

### How do I stay safe?

- Verify the official site: https://Taolend.io
- Never share private keys
- Avoid phishing links

### Will Taolend ever ask for my private key?

**Never.** Any request for private keys is a scam.

---

## Technical

### Supported network?

Bittensor EVM chain only.

### Why did my transaction fail?

- Insufficient Gas
- Insufficient Balance
- Network congestion
- Action not yet allowed

Failed transactions still consume Gas.

### How fast are confirmations?

Most actions confirm within **10–30 seconds**.

---

## Disclaimer

This documentation is for informational purposes only and does not constitute financial advice. Using Taolend involves risks, including market volatility, borrower default, and ALPHA price fluctuations. Always assess your risk tolerance before participating.