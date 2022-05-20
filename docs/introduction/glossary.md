---
description: Definitions for common terms used throughout the Topl ecosystem
---

# Glossary

### Taktikos

The regularized Nakamoto-style proof-of-stake consensus algorithm that powers the Topl protocol.  The Taktikos staking mechanism reduces variance in the distribution of time intervals between blocks by means of a time-varying leader election process. This quality of _regularization_ significant improvements for transaction throughput and finality guarantees in a proof-of-stake protocol. Read [more](../fees-currency-and-consensus/taktikos-pos.md)

### Application Tiers

Fully decentralized applications can only be achieved by being completely transparent (like a DAO couldn't run as a Tier 2? That seems like it would be collusion), but there are several stages between traditional web 2.0 (or Tier 0) applications and fully decentralized and autonomous Tier 3 applications. Key to the progression between each tier is the identification of which party executes business logic and approves (signs) the final transaction.

**Tier 0:** Traditional centralized application where verifiable claims are neither committed to nor posted to a public network. In this model, business logic is executed by the organization and wallets are not part of the application.

**Tier 1:** Traditional centralized application where verifiable claims are committed to and posted to a public network. In this model, organizations both execute business logic and administer multiple wallets to manage their on-chain assets.

**Tier 2:** Partially decentralized application where verifiable claims are committed to and posted to a public network. In this model, users become participants by maintaining their own wallets and interacting with organizations to sign transactions. Organizations are responsible for executed business logic and constructing unsigned blockchain transactions which are then sent to the user for their signature. Upon approving and signing the transaction, the user sends the signed transaction back to the organization for any further processing before broadcast to the public network.

**Tier 3:** Fully decentralized application where verifiable claims are committed to and posted to a public network. In this model, users become fully autonomous and no longer rely on the organization to construct transactions on their behalf. Organizations make available their business logic on the public network and users execute this logic to construct their own transactions, sign them, and broadcast them to the public network.
