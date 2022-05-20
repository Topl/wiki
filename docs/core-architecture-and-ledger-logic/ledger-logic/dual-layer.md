# Ledger Logic

In order to extend the functionality of the blockchain protocol, Topl has conceived a dual layer _ledger logic_ system consisting of a highly optimized on-chain DSL along with support for off-chain Turing complete smart contracts.

Topl's on-chain DSL, known as [Quivr](smart-tokens.md), is intended to complement Topl's tokenization-first design and is built using extended-UTxO functionality. This tightly optimized DSL, made up of roughly a dozen composable functions can cover the vast majority of use cases without the need for fully generalized (and more complex) smart contracts.

For the ~20% of use-cases where Quivr proves to be too limiting, the second half of Topl's ledger logic system comes into play. Topl has elected to integrate the fully Turing-complete [Digital Asset Modeling Language (DAML)](chain-program-engine.md) into its protocol.
