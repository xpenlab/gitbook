# Platform Roles

> The Taolend platform has two primary roles: **Lender** and **Borrower**. Users can act as both roles at the same time.

---

## Lender

### Role Definition

A Lender is a user who holds TAO and provides liquidity to Borrowers by creating Offers (lending orders) in order to earn interest.

### How It Works

1. **Deposit TAO**: Deposit TAO into the Taolend contract
2. **Create Offer**: Define lending terms (signed offline, no Gas required)
3. **Wait for Borrowers**: Borrowers browse and Accept Loan Offers
4. **Earn Interest**: Interest is calculated daily and credited after repayment

### Income Source

A Lender’s income comes from interest paid by Borrowers:

```
Interest paid by borrower = Loan amount × Daily interest rate × Days
Lender actual earnings = Total interest × 70%
Protocol fee = Total interest × 30%
```

**Example**:
- Borrow Amount: 100 TAO
- Daily APR: 0.1%
- Loan duration: 30 days
- Total interest: 3 TAO
- Lender earnings: 2.1 TAO (70%)
- Protocol fee: 0.9 TAO (30%)

### Risks and Benefits

**Benefits**:
- ✅ Passive income with minimal management
- ✅ Stable returns, calculated daily
- ✅ ALPHA collateral protection with a 90% safety margin
- ✅ Ability to create multiple Offers to diversify risk
- ✅ Unused TAO can be Withdrawn at any time

**Risks**:
- ⚠️ **Liquidity risk**: TAO is locked until the loan is repaid
- ⚠️ **ALPHA price volatility**: Collateral value may decline
- ⚠️ **Borrower default**: Late or missed repayment (mitigated by collateral)

### Suitable For

- Users holding idle TAO who want to earn yield
- Users familiar with Bittensor Subnets and ALPHA valuation
- Users able to periodically review and manage Offers

📖 **Detailed Guide**: [Lend](lend.md)

---

## Borrower

### Role Definition

A Borrower is a user who holds ALPHA (Bittensor Subnet tokens) and borrows TAO from Lenders by providing ALPHA as collateral.

### How It Works

1. **Deposit ALPHA**: Deposit ALPHA as Collateral Amount
2. **Initiate Borrow**: The system automatically matches the Best Daily APR Offer
3. **Receive TAO**: Borrow TAO with one click; funds arrive instantly
4. **Repay or Refinance**: Repay Loan at any time or switch to a better Offer

### Costs and Fees

Borrowers incur the following costs:

1. **Loan Interest**
   - Daily APR ranges from 0.01% to 1% (set by Lenders)
   - Calculated daily based on the Borrow Amount

2. **Gas Fees**
   - Required for borrowing, repayment, and refinancing
   - Recommended balance: 0.05–0.1 TAO

**Example**:
- Borrow Amount: 50 TAO
- Daily APR: 0.15%
- Loan duration: 15 days
- Total interest: 1.125 TAO
- Total repayment: 51.125 TAO

### Risks and Benefits

**Benefits**:
- ✅ Retain ALPHA exposure and long-term upside
- ✅ Access TAO liquidity for other opportunities
- ✅ Flexible repayment at any time
- ✅ Ability to lower interest via refinancing
- ✅ Minimum Borrow Amount of just 1 TAO

**Risks**:
- ⚠️ **Overdue risk**: Failure to repay results in loss of all ALPHA collateral
- ⚠️ **Interest cost**: Accumulates daily over time
- ⚠️ **ALPHA price risk**: Price drops may reduce borrowing capacity
- ⚠️ **Liquidity lock-up**: Collateral cannot be used elsewhere

### Loan Cycle

**Phase 1: Active (0–3 days)**
- ✅ Normal usage
- ✅ Daily interest accrual
- ✅ Repay Loan at any time

**Phase 2: Minimum Period Reached (after 3 days)**
- ⚠️ Lender may initiate collection
- ⚠️ Repayment is recommended

**Phase 3: Collection Period (within 3 days)**
- ⚠️ Immediate repayment required
- ⚠️ Failure to repay leads to overdue status

**Phase 4: Overdue**
- ❌ **All ALPHA collateral is forfeited**

### Suitable For

- Users holding ALPHA with long-term conviction
- Users needing short-term TAO liquidity
- Users confident in timely repayment
- Users who understand and accept liquidation risk

📖 **Detailed Guide**: [Borrow](borrow.md)

---

## Next Steps

- Learn how to [lend TAO](lend.md)
- Learn how to [borrow TAO](borrow.md)
- Explore detailed explanations of [core features](README.md)