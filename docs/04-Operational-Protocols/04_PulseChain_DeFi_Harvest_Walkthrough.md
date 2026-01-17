# PulseChain DeFi Harvest Walkthrough (LP → USDC → Wise)

**Date:** January 17, 2026  
**For:** Bryan (Old Glory Foundation)  
**Purpose:** Step-by-step guide to harvest DeFi yields from PulseChain and convert to fiat via Wise

---

## Overview

This walkthrough shows you how to:
1. **Harvest yields** from PulseChain liquidity pools (LPs)
2. **Convert** LP tokens → PulseChain native tokens → USDC
3. **Bridge** USDC from PulseChain to Ethereum mainnet
4. **Off-ramp** USDC to USD via centralized exchange or Wise integration

**Goal:** Get $3,000-$6,000 USD per month from DeFi yields into your Wise account for salary payments and living expenses.

---

## Prerequisites

Before starting, ensure you have:

- [ ] **MetaMask wallet** with PulseChain network added
- [ ] **PulseChain RPC endpoint:** `https://rpc.pulsechain.com`
- [ ] **Active LP positions** on PulseChain (e.g., pDAI/pWBTC, Atropa pairs)
- [ ] **Small amount of PLS** for gas fees (~10-20 PLS, about $0.50-$1.00)
- [ ] **Centralized exchange account** (Coinbase, Kraken, or Binance) for USDC off-ramp
- [ ] **Wise Business account** (for final USD deposit)

---

## Step 1: Connect to PulseChain Network

### Add PulseChain to MetaMask

If you haven't added PulseChain to MetaMask yet:

1. Open **MetaMask**
2. Click **network dropdown** (top center)
3. Click **"Add Network"** → **"Add a network manually"**
4. Enter PulseChain details:

| Field | Value |
|-------|-------|
| **Network Name** | PulseChain |
| **RPC URL** | https://rpc.pulsechain.com |
| **Chain ID** | 369 |
| **Currency Symbol** | PLS |
| **Block Explorer** | https://scan.pulsechain.com |

5. Click **"Save"**
6. Switch to **PulseChain network**

### Verify Connection

- Open https://scan.pulsechain.com
- Enter your wallet address
- Confirm you can see your LP positions and token balances

---

## Step 2: Harvest LP Yields

### Option A: PulseX (Most Common)

**PulseX** is the primary DEX on PulseChain.

1. Go to **https://app.pulsex.com**
2. Click **"Connect Wallet"** → Select **MetaMask**
3. Navigate to **"Liquidity"** or **"Farms"**
4. Find your LP positions (e.g., pDAI/pWBTC, Atropa/PLS)
5. Click **"Harvest"** or **"Claim Rewards"**
6. Confirm transaction in MetaMask
7. Wait for confirmation (usually 10-30 seconds)

**Gas Cost:** ~0.5-2 PLS per transaction

### Option B: 9inch (Aggregator)

**9inch** is a DEX aggregator that may offer better rates.

1. Go to **https://9inch.io**
2. Connect MetaMask
3. Navigate to your LP positions
4. Harvest rewards
5. Confirm transaction

### What You'll Receive

After harvesting, you'll have:
- **LP tokens** (e.g., pDAI/pWBTC LP tokens)
- **Reward tokens** (e.g., PLSX, INC, or other farm rewards)

---

## Step 3: Remove Liquidity from LP Positions

To convert LP tokens back to individual tokens:

1. Go to **https://app.pulsex.com/liquidity**
2. Find your LP position
3. Click **"Remove"**
4. Select **percentage to remove** (25%, 50%, 75%, 100%)
5. Click **"Remove Liquidity"**
6. Confirm transaction in MetaMask

**Result:** You'll receive the two tokens that made up the LP pair (e.g., pDAI + pWBTC)

**Gas Cost:** ~1-3 PLS per transaction

---

## Step 4: Swap Tokens to USDC

Now you need to convert all tokens to USDC for bridging.

### Step 4a: Swap pDAI, pWBTC, and other tokens to PLS

1. Go to **https://app.pulsex.com/swap**
2. **From:** Select token to swap (e.g., pDAI)
3. **To:** Select **PLS**
4. Enter amount to swap
5. Click **"Swap"**
6. Confirm transaction in MetaMask
7. Repeat for all tokens you want to convert

**Gas Cost:** ~1-2 PLS per swap

### Step 4b: Swap PLS to USDC

1. Go to **https://app.pulsex.com/swap**
2. **From:** PLS
3. **To:** USDC (search for "USDC" in token list)
4. Enter amount to swap
5. Click **"Swap"**
6. Confirm transaction in MetaMask

**Important:** Make sure you're swapping to **bridged USDC** (USDC.e or similar), not a wrapped version.

---

## Step 5: Bridge USDC from PulseChain to Ethereum

To off-ramp USDC, you need to bridge it to Ethereum mainnet (most exchanges don't support PulseChain directly).

### Option A: PulseChain Bridge (Official)

1. Go to **https://bridge.pulsechain.com**
2. Connect MetaMask (ensure you're on PulseChain network)
3. **From:** PulseChain
4. **To:** Ethereum
5. **Token:** USDC
6. Enter amount to bridge
7. Click **"Bridge"**
8. Confirm transaction in MetaMask
9. Wait for bridge confirmation (5-30 minutes)

**Bridge Fee:** ~$5-20 USD (varies by network congestion)

### Option B: Third-Party Bridges

If official bridge is congested or expensive:

- **Multichain:** https://multichain.org
- **Synapse:** https://synapseprotocol.com
- **Hop Protocol:** https://hop.exchange

**Note:** Always verify bridge contract addresses before using third-party bridges.

---

## Step 6: Off-Ramp USDC to USD

Once USDC is on Ethereum mainnet, you have several off-ramp options.

### Option A: Coinbase (Recommended for US)

**Why Coinbase:**
- Direct USDC support (no conversion needed)
- Free USDC deposits
- Fast ACH withdrawals to US bank account (1-3 business days)
- Low fees (0.5% for ACH withdrawal)

**Steps:**

1. **Create Coinbase account** (if you don't have one)
   - Go to https://www.coinbase.com
   - Complete KYC verification

2. **Get your Coinbase USDC deposit address:**
   - Log in to Coinbase
   - Click **"Receive"**
   - Select **"USDC"**
   - Select **"Ethereum network"** (ERC-20)
   - Copy deposit address

3. **Send USDC from MetaMask to Coinbase:**
   - Open MetaMask (ensure you're on Ethereum mainnet)
   - Click **"Send"**
   - Paste Coinbase USDC deposit address
   - Enter amount to send
   - Confirm transaction
   - Wait for confirmation (2-10 minutes)

4. **Withdraw USD to bank account:**
   - Once USDC appears in Coinbase, click **"Sell"**
   - Select **"USDC"** → **"USD"**
   - Enter amount to sell
   - Click **"Preview Sell"** → **"Sell USDC"**
   - Click **"Withdraw"** → Select bank account
   - Enter amount to withdraw
   - Confirm withdrawal

**Timeline:** USDC → USD (instant), USD → Bank (1-3 business days)

**Fees:**
- USDC deposit: Free
- USDC → USD conversion: ~0.5%
- USD withdrawal (ACH): Free

### Option B: Kraken (Alternative)

**Steps:**

1. Create Kraken account: https://www.kraken.com
2. Complete KYC verification
3. Get USDC deposit address (Ethereum network)
4. Send USDC from MetaMask to Kraken
5. Convert USDC → USD (0.26% fee)
6. Withdraw USD to bank account (free ACH)

**Timeline:** Similar to Coinbase

### Option C: Wise Direct (If Supported)

Some users report being able to deposit USDC directly to Wise via third-party integrations, but this is not officially supported by Wise. **Stick with Coinbase/Kraken for reliability.**

---

## Step 7: Transfer USD from Bank to Wise

Once USD is in your US bank account (from Coinbase/Kraken):

1. Log in to **Wise Business**
2. Click **"Add money"**
3. Select **"USD balance"**
4. Choose **"ACH"** or **"Wire transfer"**
5. Wise will provide bank details (routing number, account number)
6. Initiate transfer from your bank to Wise
7. Wait for transfer to complete (1-3 business days for ACH)

**Fees:**
- ACH: Free (most banks)
- Wire: $15-30 (if you use wire instead of ACH)

---

## Complete Flow Summary

```
PulseChain LP (pDAI/pWBTC)
    ↓ (Harvest yields)
LP Tokens + Rewards
    ↓ (Remove liquidity)
pDAI + pWBTC + Reward Tokens
    ↓ (Swap to PLS)
PLS
    ↓ (Swap to USDC)
USDC (PulseChain)
    ↓ (Bridge to Ethereum)
USDC (Ethereum)
    ↓ (Send to Coinbase)
USDC (Coinbase)
    ↓ (Sell to USD)
USD (Coinbase)
    ↓ (Withdraw to bank)
USD (Your Bank Account)
    ↓ (Transfer to Wise)
USD (Wise Business)
    ↓ (Pay salary to personal account)
USD (Your Personal Account)
```

---

## Gas Fees and Costs

| Step | Network | Gas Cost (USD) |
|------|---------|----------------|
| Harvest LP yields | PulseChain | $0.01-0.10 |
| Remove liquidity | PulseChain | $0.05-0.20 |
| Swap tokens to PLS | PulseChain | $0.05-0.15 per swap |
| Swap PLS to USDC | PulseChain | $0.05-0.15 |
| Bridge USDC to Ethereum | PulseChain + Ethereum | $5-20 |
| Send USDC to Coinbase | Ethereum | $2-10 |
| **Total Gas Costs** | | **$7-30** |

**Additional Fees:**
- Coinbase USDC → USD: ~0.5% ($15-30 on $3,000-$6,000)
- Bank → Wise ACH: Free
- **Total Fees:** ~$22-60 per $3,000-$6,000 harvest

**Net Yield:** If you're earning 5-15% APY on $50,000-$100,000 in LPs, monthly yield is $200-$1,250. After fees, net is $140-$1,190/month.

---

## Optimization Tips

### Tip 1: Batch Transactions

Instead of harvesting weekly, harvest monthly to reduce gas fees.

**Example:**
- Weekly harvest: 4 transactions/month × $30 gas = $120/month
- Monthly harvest: 1 transaction/month × $30 gas = $30/month
- **Savings:** $90/month

### Tip 2: Use DEX Aggregators

Use **9inch.io** or **Matcha** to find best swap rates and reduce slippage.

### Tip 3: Monitor Gas Prices

Bridge USDC during low Ethereum gas periods (weekends, late night US time) to save $5-15 per bridge.

### Tip 4: Keep PLS Buffer

Always keep 20-50 PLS in your wallet for gas fees. Running out of PLS mid-harvest is frustrating.

### Tip 5: Automate with Scripts (Advanced)

If you're comfortable with Python, you can automate harvesting and swapping using Web3.py:

```python
from web3 import Web3

# Connect to PulseChain
w3 = Web3(Web3.HTTPProvider('https://rpc.pulsechain.com'))

# Your wallet address and private key
wallet_address = '0xYourAddress'
private_key = 'YourPrivateKey'

# Contract addresses (PulseX Router, LP contracts, etc.)
# ... (implementation details)

# Harvest, swap, bridge functions
# ... (implementation details)
```

**Caution:** Only use automation if you understand smart contract interactions and security risks.

---

## Security Best Practices

### 1. Use Hardware Wallet

Store large LP positions in a **Ledger** or **Trezor** hardware wallet, not MetaMask hot wallet.

### 2. Verify Contract Addresses

Always verify contract addresses on **https://scan.pulsechain.com** before interacting.

### 3. Test with Small Amounts

First time bridging or using a new DEX? Test with $10-50 first.

### 4. Revoke Approvals

After completing transactions, revoke token approvals to prevent future exploits:
- Go to **https://revoke.cash**
- Connect wallet
- Revoke unnecessary approvals

### 5. Use Separate Wallets

- **Wallet A:** Large LP holdings (hardware wallet)
- **Wallet B:** Active trading and harvesting (MetaMask)
- **Wallet C:** Off-ramping to exchanges (MetaMask)

Transfer from A → B → C as needed to minimize risk.

---

## Troubleshooting

**Q: Transaction failed with "insufficient funds for gas"**  
A: You need more PLS in your wallet. Buy 10-20 PLS on PulseX or bridge from Ethereum.

**Q: Bridge is taking longer than 30 minutes**  
A: Check bridge status on https://bridge.pulsechain.com. If stuck, contact bridge support or wait 24 hours (sometimes bridges have delays).

**Q: USDC not appearing in Coinbase**  
A: Check transaction on Etherscan. If confirmed, wait 10-30 minutes. If still not showing, contact Coinbase support with transaction hash.

**Q: Slippage too high on swap**  
A: Increase slippage tolerance to 1-3% in PulseX settings, or split large swaps into smaller batches.

**Q: Can I skip the bridge and off-ramp directly from PulseChain?**  
A: Not easily. Most centralized exchanges don't support PulseChain. You could use XPX Pay or Cake Pay to off-ramp directly, but Coinbase → Wise is more reliable for large amounts.

---

## Monthly Harvest Checklist

- [ ] Check LP positions on PulseX
- [ ] Harvest yields (if >$500 accumulated)
- [ ] Remove liquidity from LP positions (if needed)
- [ ] Swap all tokens to PLS
- [ ] Swap PLS to USDC
- [ ] Bridge USDC to Ethereum (monitor gas prices)
- [ ] Send USDC to Coinbase
- [ ] Sell USDC for USD on Coinbase
- [ ] Withdraw USD to bank account
- [ ] Transfer USD from bank to Wise Business
- [ ] Pay salary from Wise to personal account
- [ ] Document transaction for tax records

---

## Tax Considerations

**Important:** All crypto transactions are taxable events in the US.

### What You Need to Track

1. **LP deposits** (cost basis)
2. **LP yields** (ordinary income)
3. **Token swaps** (capital gains/losses)
4. **USDC off-ramp** (capital gains/losses)

### Recommended Tools

- **Koinly:** https://koinly.io (crypto tax software)
- **CoinTracker:** https://www.cointracker.io
- **TokenTax:** https://tokentax.co

Connect your MetaMask and Coinbase accounts to automatically track transactions.

### Reporting

- **Form 8949:** Capital gains/losses from crypto sales
- **Schedule C:** If foundation is receiving DeFi yields as business income
- **Form 1040:** Report on personal tax return

**Consult a crypto-savvy CPA** for proper reporting, especially if yields exceed $10,000/year.

---

## Summary

**This is your DeFi → Fiat pipeline. Master it, and you'll never worry about liquidity again.**

**Monthly routine:**
1. Harvest PulseChain LP yields
2. Convert to USDC
3. Bridge to Ethereum
4. Off-ramp via Coinbase
5. Transfer to Wise
6. Pay yourself salary

**Time required:** 1-2 hours per month  
**Cost:** $30-60 in fees per $3,000-$6,000 harvest  
**Result:** Consistent monthly income for Economic Solvency visa and living expenses in Mexico

**This is how the DeFi engine fuels the Grey Man architecture.**
