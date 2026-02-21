# FlexNet/FlexDex Independent Research Notes
## Feb 20-21, 2026

### Website Verified Claims (flexnet.tech)
- L2 rollup on Conduit stack (ETH L2 infra)
- Wrapped HEX as native gas token (FLEX = 1:1 HEX)
- 1000 tx/s throughput claimed
- +100k community claimed
- FlexDex: Novel ERC token standard with built-in issuance, loss mitigation, LP
- FlexLab Incubator: funding, design, audits, community
- Ownership Units: Soulbound NFTs, 100k total supply
  - Angel: $70/unit, 5,272 of 10,000 sold ($247k deposited)
  - Seed: $140/unit, 14 of 10,000 sold
  - Expansion: $280/unit, coming soon
- Revenue: Sequencer fees, FlexDex LP, Incubator equity, Fundraising bonuses
- Roadmap: Q4'24 concept, Q1'25 pre-testnet, Q2'25 testnet, Q3'25 mainnet

### Key Observations
- Pre-mainnet, pre-testnet project
- $247k total deposited (very small)
- Internal/Claude-generated audit (no external big-name audit)
- HEX dependency for all value
- Soulbound NFTs = illiquid until benchmarks met
- Dev (@TantoNomini) pinned post: "sell all PulseChain tokens, bridge out, buy HEX on Ethereum"
- Dev calls PulseChain a "side quest"

### CRITICAL FINDING: FlexDex Dapp "Coming Soon"
- Clicking "Read Documentation" or "Explore FlexDex" shows popup: "Coming Soon - Dapp will be available soon on FlexNet Test Net"
- This means the product does NOT exist yet. No testnet. No mainnet. Pure vapor.

### FlexDex Tokenomics (from website page)
- 100M standard supply per token
- 80% allocated to liquidity depositors at fixed rate during launch period
- 20M + 25% of FLEX deposits go to constant product AMM pool inside the contract
- Remaining FLEX deposits establish price floor (min redemption value)
- Direct trading from token contract (no third-party DEX)
- No approvals required (uses native FLEX)
- Integrated limit orders in token contract
- Price floor = max possible loss known upfront, anti-rug

### CRITICAL FINDING: Docs Page = 404
- flexnet.tech/docs returns "404 Page Not Found - Did you forget to add the page to the router?"
- No documentation exists on the website itself
- Error message even reveals dev oversight ("Did you forget to add the page to the router?")

### CRITICAL FINDING: Strategy Page = 404
- flexnet.tech/strategy also returns 404
- Two of the main navigation links (Docs, Strategy) are broken

### OWNERSHIP MODEL (flexnet.tech/ownership)
- Sell "Ownership Units" as non-transferable NFTs on Ethereum and PulseChain
- 100,000 total supply cap
- Promise "Quadruple Income Streams":
  1. Sequencer Fees (from L2 network transactions)
  2. FlexDex LP Fees (from all locked liquidity)
  3. Incubator Equity (from FlexLab startups)
  4. Fundraising Rewards (bonus from new unit sales = classic pyramid incentive)
- Revenue paid in HEX and other tokens
- Units convert to liquid token "once certain network benchmarks are met"
- Currently: "No Active Offering" = nothing to buy
- Goal stated: "Exceed Coinbase's $120M sequencer earnings from Base L2"
- HIGH RISK disclaimer at bottom: "YOU SHOULD NOT DEPOSIT FUNDS YOU CANNOT AFFORD TO LOSE"

### RED FLAGS SUMMARY
1. FlexDex dapp = "Coming Soon" (not even on testnet)
2. Docs page = 404
3. Strategy page = 404
4. No active ownership offering
5. Fundraising Rewards = existing owners get bonus from new buyer funds (pyramid structure)
6. Comparing to Coinbase Base L2 ($120M) with zero product
7. Dev pinned post tells PulseChain community to "sell all tokens and bridge out"
8. Soulbound NFTs = illiquid by design, no exit until dev decides benchmarks are met
9. Claude AI wrote the manifesto (dev admits "some cringe")
10. No whitepaper, no on-chain contracts to verify

### TESTNET EXPLORER FINDINGS (scan-testnet.flexnet.tech)
- Built on Blockscout (Arbitrum Orbit L2 stack)
- Latest batch: 522 (extremely low)
- Average block time: 19,934.2 seconds = 5.5 HOURS per block
- Total transactions: 48,241 (lifetime, very low)
- Total addresses: 2,286
- Daily transactions: 0 (ZERO)
- Daily transactions chart shows near-zero activity with one tiny spike
- Latest batch was 2 hours ago, previous was 1 WEEK ago
- Most transactions involve only 2-3 addresses (0xC1...50f0 and 0xB0...3FDF)
- Large FLEX transfers: 53M FLEX and 49M FLEX between same addresses
- This is essentially a dead chain with dev-only activity

### ARCHITECTURE NOTE
- FlexNet is an Arbitrum Orbit L2 (uses ArbOS, ArbRetryableTx)
- This means it settles to Ethereum L1
- FLEX = wrapped HEX (HEX wrapper on Sepolia testnet)
- The entire chain's native currency is a HEX wrapper

### RED FLAG UPDATE (now 13 flags)
11. Testnet has 0 daily transactions
12. Average block time is 5.5 HOURS (should be seconds)
13. Only 2-3 addresses active on entire chain (dev wallets only)
