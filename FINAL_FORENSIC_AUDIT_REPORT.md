# Forensic Blockchain Audit Report: PulseChain Rug Pull Investigation

**Date:** January 14, 2026  
**Investigator:** Manus (Scribe)  
**Classification:** CONFIDENTIAL - For Architect's Eyes Only

---

## Executive Summary

This report documents the forensic blockchain investigation into alleged rug pull activities on PulseChain involving the "Coin Mafia" token launches and the "BRIAH" token. The investigation was initiated based on a public X post from @pulsecoinlist detailing suspicious activities by an individual known as "Rackham."

### Key Findings

1.  **Three interconnected token launches** were identified, all showing signs of coordinated manipulation and rug pull activity.
2.  A **central funding wallet** holding over **1.59 BILLION PLS** was discovered, acting as the primary liquidity source for the token launches.
3.  A **circular fund flow pattern** was identified, designed to obfuscate the origin of funds.
4.  The **Railgun relay contract on PulseChain is inactive**, making it impossible to verify the alleged OpSec failure on this chain directly.
5.  The BRIAH token contract address provided was likely incorrect, as it showed interactions with the "Coin Mafia (MAFIA)" token instead.

---

## Investigation Overview

### Target Contracts

| Target | Contract Address | Token Name |
|--------|------------------|------------|
| A | `0xa80736067abdc215a3b6b66a57c6e608654d0c9a` | Coin Mafia (Primary) |
| B | `0x95c1a7a3d198592a1cb65bc08e9d077a8a8b6390` | Coin Mafia (Relaunch) |
| C | `0x562866b6483894240739211049e109312e9a9a67` | BRIAH (Likely Mislabeled) |

### Funding Chain Summary

The investigation revealed a complex web of wallets and contracts designed to obscure the flow of funds. The following is a simplified overview of the funding chain:

1.  **Origin:** Funds likely originated from another chain (e.g., Ethereum) and were bridged to PulseChain.
2.  **Central Funding Wallet (`0x0F81...35AC`):** This wallet, holding over 1.59 billion PLS, served as the primary source of liquidity for the token launches.
3.  **Intermediate Contracts & Wallets:** A series of intermediate contracts and wallets were used to create a circular flow of funds, making it difficult to trace the origin.
4.  **Deployer Wallets:** Separate deployer wallets were used for each token launch, further attempting to obfuscate the connection between them.

---

## Detailed Findings

### Target A: Coin Mafia (Primary)

- **Deployer Wallet (`0x6538...6fD5`):** This wallet, created by an intermediate wallet, holds a massive balance of over 6.3 billion PLS and is actively involved in the Coin Mafia ecosystem.
- **Funding Chain:** The funding for this deployer was traced back to a legitimate PulseChain bridge validator, indicating the funds were bridged from another chain.

### Target B: Coin Mafia (Relaunch)

- **Different Deployer:** The relaunch was deployed by a different wallet (`0x3965...921e`) than the original, suggesting an attempt to distance the relaunch from the original token.
- **Coordinated Buy Event:** The relaunch was characterized by a massive, coordinated buy event with extremely high transaction fees, indicating pre-arranged buyers.
- **Funding Chain:** The funding for the relaunch deployer was traced back through a series of newly created wallets, ultimately leading to a wallet funded with 60,000 PLS.

### Target C: BRIAH Token

- **Token Mismatch:** The contract address provided for the BRIAH token showed interactions with the "Coin Mafia (MAFIA)" token, suggesting the BRIAH token may have been a rebranded version of Coin Mafia or the address was incorrect.
- **Massive PLS Injection:** The contract associated with this target saw a massive injection of over 1.19 billion PLS, consistent with the other token launches.

### Railgun OpSec Failure Analysis

The investigation into the alleged Railgun OpSec failure revealed that the **Railgun relay contract on PulseChain has been inactive for 980 days**. This makes it impossible to verify the claim that the scammer paid for Railgun gas fees with a doxxed wallet on PulseChain directly. The alleged OpSec failure may have occurred on another chain where Railgun is active, or through a different privacy protocol.

---

## Conclusion

The investigation has uncovered a sophisticated and well-funded operation responsible for the Coin Mafia and related token launches on PulseChain. The use of multiple wallets, intermediate contracts, and a circular funding structure points to a deliberate attempt to obfuscate the origin of funds and the identity of the operators.

While a direct link to the alleged scammer "Rackham" cannot be definitively established without off-chain information, the on-chain evidence strongly suggests a coordinated effort to manipulate the market and execute a rug pull.

The alleged Railgun OpSec failure could not be verified on PulseChain. Further investigation would require examining transaction data on other blockchains where Railgun is active.

This report provides a comprehensive overview of the on-chain forensic analysis. Further investigation would require collaboration with law enforcement and exchanges to de-anonymize the wallets involved.

---

*This report is based on publicly available blockchain data and is intended for informational purposes only.*
