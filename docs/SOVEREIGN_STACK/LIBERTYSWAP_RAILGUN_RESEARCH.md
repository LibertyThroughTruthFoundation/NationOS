# LibertySwap Railgun Integration: Comprehensive Research

**Date:** January 14, 2026  
**Researcher:** Manus AI (Levitical Chief of Staff)  
**Purpose:** Operational reconnaissance for the Architect's implementation of privacy-preserving cross-chain transfers

---

## Executive Summary

LibertySwap's Railgun integration provides a privacy-preserving execution path for cross-chain asset transfers between Ethereum and PulseChain. The system leverages zero-knowledge-based shielding infrastructure to prevent on-chain linkage between source and destination transactions while maintaining non-custodial control and user autonomy.

**Current Supported Routes:**
- **Ethereum → PulseChain:** ETH (Railgun) → WETH (PulseChain)
- **PulseChain → Ethereum:** WETH (PulseChain) → ETH (Railgun)

---

## Architectural Design

### Privacy-Preserving Routing

LibertySwap establishes a bidirectional, privacy-preserving route through the following architecture:

**Ethereum ⇄ Railgun ⇄ PulseChain**

Under this design:
- Assets entering PulseChain from Ethereum are routed through Railgun and arrive in a shielded state.
- Assets exiting PulseChain to Ethereum are likewise routed through Railgun before settlement.
- No direct on-chain linkage between source and destination addresses is created on public ledgers.

This architecture allows users to selectively enter or exit privacy without forcing continuous participation in shielded pools.

### Key Properties

1. **User-Controlled Privacy:** Users retain full discretion over timing, amounts, and duration of shielded balances. Assets may be transferred immediately through the route or held privately for any period.

2. **Intent-Based Execution:** Users submit a single signed intent. All intermediate steps are executed by Liberty Swap relayers, requiring minimal user intervention.

3. **Non-Custodial Operation:** At no point does Liberty Swap assume custody or discretionary control over user assets.

4. **Gas Abstraction:** Private Mode leverages gas abstraction where supported, allowing users to initiate intents without maintaining native gas balances on each participating blockchain. Required execution fees are handled within the protocol's settlement process.

5. **On-Chain Verifiability:** Settlement occurs entirely on-chain via smart contracts. Liberty Swap does not maintain off-chain transaction records.

---

## Railgun Balance Model

Railgun maintains **chain-specific shielded balances**:
- A user's shielded balance on Ethereum is distinct from their shielded balance on PulseChain.
- Each network operates its own Railgun smart contracts and Merkle tree.
- Assets remain local to a chain unless explicitly transferred via a bridge or intent route.

Liberty Swap's private routing connects these isolated shielded environments through an intent-driven settlement process, enabling cross-chain movement without exposing transactional linkage.

---

## Transaction Tracking and Privacy

Each Private Mode transaction is assigned a temporary **Order ID** for user-side status tracking. The Order ID:
- Exists solely to communicate execution state to the user.
- Automatically expires after 24 hours.
- Is not stored alongside wallet addresses or transaction hashes.

Liberty Swap does **not** retain transaction hashes, wallet identifiers, or user metadata. Users who wish to independently verify execution may do so using their own wallet addresses and on-chain explorers. Privacy guarantees remain intact regardless of whether verification is performed.

---

## Operational Security (OPSEC) Principles

Based on the X thread from @LibertySwapFi, the following OPSEC principles are critical for maintaining privacy:

### 1. Never pay Railgun fees from a wallet that funded the shield
- The wallet that deposits into Railgun must never be used to pay withdrawal gas.
- Treat the funding wallet as permanently tainted once it touches the shield.
- Do not reuse it for anything related to the withdrawal.

**Rule:** Funding wallet ≠ fee payer ≠ receiver.

**LibertySwap Advantage:** Using LibertySwap for both inbound and outbound transactions helps avoid this mistake, because all transaction fees are paid by LibertySwap rather than a linked personal wallet.

### 2. If you want to pay the fee yourself, use a decoupled, pre-funded fee payer
- Prepare a fee payer wallet long before any Railgun interaction.
- Fund it from an unrelated source, different timing, different amounts.
- Let it sit idle for days or weeks before use.

This breaks timing correlation.

### 3. Avoid tight timing between deposit and withdrawal
- Do not withdraw shortly after depositing. Just sitting there in Railgun for a long time is very safe.
- Wait long enough to blend into the anonymity set.
- Time variance matters as much as amount variance.

**Bad:** deposit → withdraw within hours  
**Better:** deposit → wait days or longer → withdraw

### 4. Use common, non-unique amounts
- Avoid precise or unusual values like 0.099248 ETH.
- Use rounded, common denominations that many users use.
- Unique amounts act as fingerprints.

### 5. Do not immediately forward withdrawn funds
- Never withdraw and instantly fund another wallet.
- Add delays, intermediate steps, or additional shielding.
- Immediate forwarding creates deterministic links.

### 6. For goodness' sake, do not post your transaction on X right after you make it
- That is basically doxxing yourself.
- Using your own X account while your public addresses are already known is not wise.
- **Once you are in Railgun, disappear.**

---

## Step-by-Step Operational Guide

### Prerequisites: Prepare a Shielded Balance

To use Private Mode, users must hold ETH or WETH within a RAILGUN shielded balance. This is achieved by depositing your tokens into a compatible privacy smart contract using a supported wallet interface.

**Important:** Shielded balances are chain-specific. A shielded balance on Ethereum is distinct from shielded balances on PulseChain or other networks.

---

### Route 1: RAILGUN → PulseChain (ETH → WETH)

#### Step 1: Initiate an Intent to Receive WETH (PulseChain) in Liberty Swap

Within the Liberty Swap interface:
1. Connect your wallet.
2. Select **Exchange → Private mode**.
3. Choose the supported private route (ETH → WETH).
4. Specify the amount to swap (subject to current private route limits).
5. Fill in the Destination Address.
6. Click **[Swap]** then **[Next]**.
7. Copy LibertySwap's given Railgun ZK address.

#### Step 2: Send ETH to Liberty Swap

Within the RAILGUN-powered wallet:
1. Ensure you are operating on the **ZK (shielded) side**.
2. Initiate a transfer from your ZK address to Liberty Swap's ZK address by pasting the Liberty Swap's given ZK address into the Recipient box.
3. Enter the same amount as filled in the Liberty Swap interface in the previous step.

#### Step 3: Include the Private Memo

1. Copy the memo provided by LibertySwap.
2. Paste it into the **optional private memo field** in your RAILGUN wallet.
3. Submit the transaction in your wallet.
4. Then confirm the transaction on the Liberty Swap side.

This memo enables Liberty Swap's relay to correctly attribute and settle the incoming shielded transfer.

**Result:** The relayer executes the settlement and delivers WETH on PulseChain to the user instantly in less than a minute.

---

### Route 2: PulseChain → RAILGUN (WETH → ETH)

#### Step 1: Initiate an Intent to Receive ETH (Ethereum) in RAILGUN

Within the Liberty Swap interface:
1. Connect your wallet.
2. Select **Exchange → Private mode**.
3. Choose the supported private route (WETH → ETH).
4. Specify the amount to swap (subject to current private route limits).
5. Fill in the Railgun Private 0zk Address.
6. Click **[Swap]** then **[Confirm]**.
7. Sign the intent as shown in your connected wallet.

**Result:** The relay executes the settlement and delivers ETH (RAILGUN) to the user in less than a minute.

---

## Important Considerations

- **Private Mode is optional and user-initiated.**
- **Shielded transfers may incur higher fees and longer settlement times** due to zero-knowledge proof generation.
- **Users are responsible for understanding applicable laws and regulations** in their jurisdiction when using privacy-enhancing technologies.
- **Private Mode routes are currently subject to conservative transaction limits** during early deployment. These limits may be adjusted as liquidity and system capacity mature.

---

## Status Visibility and UX Considerations

Due to the multi-layered nature of zero-knowledge execution and cross-chain settlement, private transactions may involve longer confirmation windows than standard swaps.

Liberty Swap is actively improving UI-level status notifications to provide clearer execution feedback without compromising privacy or storing user-identifiable data.

---

## References

1. **LibertySwap Documentation:** https://docs.libertyswap.finance/how-liberty-swap-works/railgun-private-bridging
2. **LibertySwap X Thread (OPSEC):** https://x.com/LibertySwapFi/status/2011327386017829236
3. **LibertySwap X Thread (Privacy Tools):** https://x.com/LibertySwapFi/status/2011322923508752413

---

## Next Steps for Implementation

1. **Prepare a Clean Execution Wallet:** Create a fresh EVM wallet with no public history tied to your identity.
2. **Fund a Railgun Shielded Balance:** Deposit ETH or WETH into a Railgun shielded balance on the desired chain.
3. **Test with Small Amounts:** Conduct a test transaction with a small, common denomination to familiarize yourself with the process.
4. **Wait Before Unshielding:** Allow sufficient time (hours or days) before unshielding to blend into the anonymity set.
5. **Monitor for Updates:** Keep an eye on LibertySwap's X account and documentation for updates on supported routes and transaction limits.

---

**End of Research Document**


---

## Additional Privacy Features (From Privacy Features Documentation)

### What Liberty Swap's Private Mode Protects

When using Liberty Swap's Private Mode, the following information is hidden on-chain:
- **Sender identity**
- **Recipient identity**
- **Transaction amounts**
- **Token types being transferred**

On public blockchain explorers, interactions appear to originate from neutral broadcaster addresses. There is no visible link between a user's public wallet and their private activity.

### Shielded Balances and Privacy Sets

Funds deposited through Liberty Swap's Private Mode enter a **shielded balance**, also known as a **privacy set**. Within this set, tokens and users become indistinguishable from one another.

**Privacy strength increases as:**
- More users interact with the system
- More value remains shielded
- More swaps, transfers, and dApp interactions occur

The integration of RAILGUN supports full DeFi activity inside the privacy pool. Every private swap or transfer adds noise, improving privacy for all users.

Because Liberty Swap enables trading directly from shielded balances, users can keep funds private for longer periods, which further strengthens anonymity.

### Broadcasters and Gas Abstraction

Liberty Swap's private transactions are submitted to the blockchain through **Broadcasters**.

- Broadcasters pay gas on behalf of users.
- Transactions appear to come from the broadcaster, not the user.
- Transaction details are encrypted and cannot be read or modified by the broadcaster.

Broadcasters never custody funds and cannot censor users permanently. If one broadcaster fails, another can be used.

This design removes wallet-level identity leakage and reduces transaction-level fingerprinting.

### Intent-Based Private Routing

Liberty Swap uses an **intent-based model**.

Users sign a single intent describing what they want to receive. Liberty Swap executes the required steps internally, without exposing intermediate actions on-chain.

This eliminates common privacy leaks caused by manual, multi-step transactions such as:
- Deposit → swap → withdraw patterns
- Predictable timing sequences
- Identifiable transaction chains

The result is cleaner execution and fewer behavioral signals.

### Full Layer 1 Security

Because RAILGUN operates directly on Layer 1:
- Users of Liberty Swap's Private Mode inherit the security of both Ethereum and PulseChain L1
- There is no separate validator set
- If your funds stay in a RAILGUN shielded balance, you avoid bridge custody risk, because you are not using a bridge. Your remaining risks are smart contract risk and the underlying chain itself
- There are no L2 fraud proofs or sequencer assumptions

Privacy is achieved without sacrificing decentralization or security.

---

## Best Practices for Maximum Privacy

Liberty Swap's Private Mode protects on-chain data, but user behavior still matters. Privacy can be weakened by predictable patterns.

Liberty Swap is designed to reduce these risks, but users should follow these principles:

1. **Avoid instant withdrawals after deposits** - Allow time to blend into the anonymity set
2. **Use irregular amounts rather than round numbers** - Avoid creating unique fingerprints
3. **Split and recombine balances over time** - Add complexity to transaction patterns
4. **Avoid repetitive timing or destination patterns** - Randomize your behavior
5. **Use different wallets for different roles** - Separate funding, fee payment, and receiving wallets
6. **Allow funds to rest in shielded balances when possible** - Longer shielding periods increase privacy

Liberty Swap's low fees and gas abstraction make these practices easy to follow.

Future UI improvements will continue to guide users toward safer privacy defaults.

---

## Permissionless, Non-Custodial Access (No KYC)

Liberty Swap by principle is a permissionless DeFi protocol. It does not require Know Your Customer (KYC) checks or the submission of personal identification.

- There are no accounts, approvals, or identity verification steps.
- Users interact directly from their wallets.
- Access is governed by smart contracts, not intermediaries.

This design ensures that privacy is preserved not only on chain or only in Private Mode, but also at the access layer.

---

**End of Additional Privacy Features Section**


---

## Railway Wallet: The Primary Interface for Railgun

**Railway Wallet** is the primary user-facing wallet for interacting with the RAILGUN privacy system. It is a privacy-centric DeFi wallet that allows users to send encrypted blockchain transactions using the RAILGUN Privacy System.

### Supported Platforms

- **Railway Wallet for iOS:** Available on the Apple App Store
- **Railway Wallet for Android:** Available on the Google Play Store
- **Railway Wallet for Desktop:** Available for Mac, Windows, and Linux

### Recommended Workflow for First-Time Users

1. **Create a New Wallet:** Set up a new Railway Wallet with a fresh mnemonic phrase.
2. **Shield Tokens:** Deposit tokens into your 0zk address (privacy-protected address) to create a shielded balance.
3. **Unshield ETH/BNB/MATIC:** Unshield a small amount of native gas tokens to a second, fresh 0x address for self-broadcasting.
4. **Maintain a Private Balance:** Keep funds in the shielded balance and enjoy Private DeFi!

### Key Features

- **Shielding & Unshielding:** Move tokens between public (0x) and private (0zk) addresses.
- **Private Sends:** Send tokens privately to other Railgun users.
- **Public Broadcasting:** Use Railgun's public broadcasters to submit transactions without revealing your identity.
- **Self-Broadcasting:** Optionally broadcast your own transactions if you prefer full control.
- **Integrated dApps:** Access swaps, yield farming, ENS, and Unstoppable Domains directly from the wallet.
- **Custom RPCs:** Set custom RPC endpoints for enhanced privacy and control.

### Understanding 0x vs. 0zk Addresses

- **0x Address:** Your standard public Ethereum/EVM address. All transactions are visible on-chain.
- **0zk Address:** Your private Railgun address. Transactions are shielded and not visible on public explorers.

**Important:** When using LibertySwap's Private Mode, you will be interacting with your 0zk address, not your 0x address.

---

## Technical Implementation: How to Use Railway Wallet with LibertySwap

### Step 1: Install Railway Wallet

Download and install Railway Wallet on your preferred platform:
- iOS: https://apps.apple.com/app/railway-wallet/id6444334583
- Android: https://play.google.com/store/apps/details?id=com.railway
- Desktop: https://www.railway.xyz/

### Step 2: Create a New Wallet

1. Open Railway Wallet.
2. Select "Create a New Wallet."
3. Write down your mnemonic phrase and store it securely.
4. Confirm your mnemonic phrase.

**Important:** Your mnemonic phrase is the only way to recover your wallet. Store it securely offline.

### Step 3: Shield Tokens into Your 0zk Address

1. In Railway Wallet, navigate to the "Shield" tab.
2. Select the token you want to shield (e.g., ETH, USDC, DAI).
3. Enter the amount you want to shield.
4. Confirm the transaction.

**Result:** Your tokens are now in your private 0zk address and are no longer visible on public blockchain explorers.

### Step 4: Unshield Native Gas Tokens for Self-Broadcasting (Optional)

If you want to self-broadcast your transactions (instead of using public broadcasters), you will need a small amount of native gas tokens (ETH, BNB, MATIC) in a fresh 0x address.

1. In Railway Wallet, navigate to the "Unshield" tab.
2. Select the native gas token (e.g., ETH).
3. Enter a small amount (e.g., 0.01 ETH).
4. Enter a fresh 0x address (not the one you used to fund the shield).
5. Confirm the transaction.

**Result:** You now have a fresh 0x address with gas tokens that can be used for self-broadcasting.

### Step 5: Use LibertySwap's Private Mode

Once you have a shielded balance in Railway Wallet, you can use LibertySwap's Private Mode to move assets between Ethereum and PulseChain privately.

Follow the step-by-step guide in the "Operational Guide" section above to complete the private cross-chain transfer.

---

**End of Railway Wallet Section**
