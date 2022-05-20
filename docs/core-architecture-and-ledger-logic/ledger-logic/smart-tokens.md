# Quivr DSL

Within 2 years of the launch of Bitcoin, developers and users have sought to extend the basic functionality offered by the Bitcoin blockchain. These efforts reached their first peak with the launch of the Ethereum blockchain in 2015 and have continued ever since, with a wide array of efforts to bring more computing power and flexibility to blockchain networks. Despite this, the most exciting use cases for blockchain logic remain centered around the movement and transacting of assets. Given the unique ability of blockchain's to disintermediate the trust required for parties to interact economically, this makes sense.

Within 2 years of Bitcoin's launch, developers and users were already seeking to extend the basic functionality offered by the Bitcoin blockchain. These efforts reached their first peak with the launch of Ethereum in 2015, and a wide array of efforts to bring more computing power and flexibility to blockchain networks has continued ever since.

_More information coming soon_

Despite the expansion, the most exciting use cases for blockchain logic remain centered around the movement and transacting of assets. Given the ability of blockchain's to disintermediate the trust required for parties to interact economically, this makes sense.

To complement blockchain's natural fit with asset focused use cases, Topl has endeavored to tightly and efficiently couple advanced functionality with tokenized-assets themselves on our blockchain. To do this we employ a _smart_ _token_ framework which combines user-defined, protocol-level assets and ledger logic functionality expressed through both [extended-UTxOs](../extended-utxos.md) and [chain programs](chain-program-engine.md).

To complement blockchain's natural fit with asset-focused use cases, the Topl Blockchain couples advanced functionality with tokenized assets. To do this, we employ a _smart_ _token_ framework combining user-defined, protocol-level assets and ledger logic functionality expressed through both [extended-UTxOs](../extended-utxos.md) and [chain programs](chain-program-engine.md).

To unpack this, let's first introduce what is meant by user-defined, protocol-level assets. Unlike with many other blockchains, a user can classify and mint their own arbitrary assets on chain without the use of any additional code beyond the protocol itself. By not having to rely on abstractions to simply create and mint new assets, Topl makes user-defined assets "first-class citizens" on our blockchain.

To unpack this, let's introduce user-defined, protocol-level assets. Unlike many other blockchains, the Topl Blockchain lets a user classify and mint their own arbitrary assets on chain without the use of any additional code beyond the protocol itself. By not relying on abstractions to simply create and mint new assets, the Topl Blockchain makes user-defined assets "first-class citizens."

Beyond simply minting and transferring more complex controls and properties such as those found in Topl's [token ontology](token-ontology.md) will be achieved through a combination of extended-UTxOs (simply understood as complex locks or propositions that must be satisfied) and a special form of chain program known as a coordination program. In particular, coordination programs will be used to store asset properties either in plain text or as fingerprints of data stored off-chain.

Beyond minting and transferring, more complex controls and properties such as those found in Topl's [token ontology](token-ontology.md) will be achieved through extended-UTxOs (complex locks or propositions that must be satisfied) and a special form of chain program known as a coordination program. In particular, coordination programs will be used to store asset properties either in plain text or as fingerprints of data stored off-chain.
