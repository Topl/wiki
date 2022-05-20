# DAML Layer

In order to provide even greater flexibility and use-case coverage than offered by the [Quivr DSL](smart-tokens.md), the Topl protocol supports a Layer 2 smart contract solution using the Turing-complete Digital Asset Modeling Language (DAML). [Developed by Digital Asset](https://www.digitalasset.com/developers), this open-source smart contract language is based on Haskell and as such is a typed, functional language. This design decision makes DAML extremely well suited to encouraging safer and more predictable development patterns, as well as [improved code audits and analysis](https://blog.digitalasset.com/developers/what-is-formal-verification-and-what-it-means-for-daml).

In 2014, the crypto space shifted from a focus on UTxO-ledger blockchains, such as Bitcoin, to account-ledger blockchains, such as Ethereum. This transition was driven in large part by the development of the Ethereum Virtual Machine (EVM) and by the model of smart contract execution chosen by the Ethereum team.

Thankfully, considering the benefits of a UTxO ledger model over an account model for scalability and traceability, the model popularized by Ethereum is not the sole model for the complex ledger logic atop a blockchain. As we discuss ([here](../extended-utxos.md)), extended-UTxOs currently being implemented into the Topl Blockchain represent another such model. The key limit of extended-UTxOs lies in the fact that multi-step computations must be carried out across multiple blocks. To offer a second method for _ledger_ _logic_ on the Topl Blockchain, a Chain Program Engine is currently under development to provide greater flexibility to Topl's users.

Thankfully, considering the benefits of a UTxO ledger model over an account model for scalability and traceability, the model popularized by Ethereum is not the sole model for the complex ledger logic atop a blockchain. As we discuss ([here](../extended-utxos.md)), extended-UTxOs currently being implemented into the Topl Blockchain represent another such model. The key limit of extended-UTxOs lies in the fact that multi-step computations must be carried out across multiple blocks. To offer a second method for _ledger_ _logic_ on the Topl Blockchain, a Chain Program Engine will provide greater flexibility to Topl's users.

While DAML has found strong adoption in private enterprise deployments, it has not as of yet been integrated with any major public chains, despite numerous [improvements over Solidity](https://blog.digitalasset.com/developers/ethereum-versus-daml-enterprise-blockchain) and other smart contract languages.

Topl's Chain Program Engine differs from Ethereum style smart contracts in a few key ways:

Topl's Chain Program Engine differs from Ethereum-style smart contracts in a few key ways:

Given that DAML smart contracts in fact combine logical execution with a virtual (UTxO) ledger model, it is an ideal tool for a Layer 2 smart contract platform. Through Topl's DAML integration, users can achieve the following:

* In order to affect state (carry out a transaction), a chain program must always be provided a signature, whether a simple signature or proxy signature, to execute. As many security vulnerabilities exploited in Ethereum smart contracts stem from these contracts being able to execute "autonomously", the requirement for a signature may considerably reduce the likelihood of such exploits.
* In line with the rest of Topl's ledger, chain programs function within the framework of UTxOs with special boxes, called _code boxes, state boxes, and execution boxes_ employed. Not only does this approach enable users to more easily (with fewer resources) verify chain programs than smart contracts, but it also substantially reduces the so-called miner-extractable value (MEV).

<!---->

* In order to affect state (carry out a transaction), a chain program must always be provided a signature, whether a simple signature or proxy signature, to execute. As many security vulnerabilities in Ethereum smart contracts stem from these contracts being able to execute "autonomously," the requirement for a signature may considerably reduce the likelihood of such exploits.
* In line with Topl's ledger, chain programs function within the framework of UTxOs, with special boxes, called _code boxes, state boxes, and execution boxes_ employed. Not only does this approach enable users to more easily (with fewer resources) verify chain programs than smart contracts, but it substantially reduces the so-called miner-extractable value (MEV).

<!---->

* Write and deploy Turing-complete contracts without the substantial gas fees found in EVM-style protocols;
* Achieve privacy domain separation between the public (Layer 1) Topl Blockchain and private (Layer 2) DAML contracts;
* Support bi-directional conditionality with DAML smart contracts capable of being triggered by on-chain transactions and vice versa.

Finally, in addition to the above benefits, the separation of its Turing-complete smart contract layer into a separated domain enables the Topl blockchain to achieve greater levels of scalability.
