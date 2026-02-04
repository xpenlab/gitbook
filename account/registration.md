# Account Registration

> Before using Taolend for any lending or borrowing activities, you must complete account registration. The process is simple and usually takes only a few minutes.

## Why Registration Is Required

Taolend manages all lending and borrowing operations through smart contracts. Registering an account allows Taolend to:

- **Create an On-Chain Identity**: Register your EVM address with the smart contract
- **Establish Address Mapping**: Link your EVM address to a Bittensor SS58 address
- **Enable Full Functionality**: Unlock all features such as Deposit, Borrow, Lend, and creating Offers
- **Ensure Security**: Verify ownership through EIP-712 signature authentication

## Preparation

Before registering, make sure that:

- ✅ You have completed [Asset Bridging](bridge-assets.md)
- ✅ Your EVM wallet (e.g. MetaMask) has enough TAO to pay Gas fees (recommended: at least 0.1 TAO)
- ✅ You are aware of your Bittensor SS58 address
- ✅ You are using the official Taolend website

---

## Registration Process

### Step 1: Access the Platform

1. **Open the Official Taolend Website**
   - Visit: [Taolend.io](https://Taolend.io)
   - Double-check the URL to avoid phishing sites

2. **Check Network Connection**
   - Make sure your wallet is connected to the correct network
   - Taolend operates on the Bittensor EVM chain

### Step 2: Connect EVM Wallet

1. **Click Connect Wallet**
   - Locate the **Connect Wallet** button in the top-right corner

2. **Select Wallet Type**
   - Choose MetaMask (recommended)
   - Or any other supported EVM wallet

3. **Confirm Connection**
   - A connection request will pop up in your wallet
   - Review the requested permissions
   - Click **Connect**
   - Confirm that your wallet address is displayed on the page

### Step 3: Complete Registration

![Registration Interface](../images/register.png)

1. **Locate the Register Button**
   - Navigate to the **Profile** page
   - After connecting your wallet, if the address is not registered, a **Register** button will appear
   - After clicking it, your current EVM address and the derived SS58 address will be shown
   - Confirm the EVM address is correct, then click **Register** to proceed

2. **Signature Verification**
   - A signature request will appear in your wallet
   - Carefully review the message
   - Click **Sign** in your wallet

3. **Confirm Registration Transaction**
   - After signing, a transaction confirmation window will appear
   - This transaction calls the smart contract’s `register()` function
   - Click **Confirm** to submit

4. **Wait for Transaction Confirmation**
   - The transaction will be confirmed on-chain
   - Usually takes **10–30 seconds**
   - You can track the status in a block explorer
   - Once confirmed, the page will show a registration success message

### Step 4: Verify Registration Status

1. **View Account Information**
   - After successful registration, your account information will be displayed
   - Including your EVM address
   - And the corresponding SS58 address

2. **Test Features**
   - Try accessing the **Deposit** feature
   - Confirm that platform functions are available

---

## Address Mapping Relationship

### EVM Address vs SS58 Address

Taolend works with two address formats:

**EVM Address** (0x...)
- Used for all Taolend platform interactions
- Address format used by MetaMask
- Primary address recognized by smart contracts

**SS58 Address** (Bittensor format)
- Native address format of the Bittensor chain
- Used for bridging and staking operations
- Automatically derived by the system

### Address Derivation

During registration, Taolend will:

1. Record your EVM address
2. Automatically derive the corresponding SS58 address
3. Create a permanent mapping between the two
4. Allow you to manage Bittensor assets using your EVM address
