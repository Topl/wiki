# UTxO Ledger

An early decision in the development of a blockchain network is to choose the ledger model. How the evolution of state is tracked from block to block has deep implications on a blockchain's overall design and functionality.

With the benefit of a combined 10 years of blockchain experience at inception, Topl opted to adopt a UTxO ledger model instead of an account-based model, resulting in greater **scalability** and **traceability** for the Topl Blockchain.

### Scalability

The scalability benefit of UTxO ledgers comes from that the common method of achieving layer 1 blockchain scalability, sharding, is easier and more natural to implement atop a UTxO ledger. With sharding, the major challenge is determining how to form shards. How do we group users or contracts onto one shard compared to another? The answer is critical. Realizing scaling benefits through sharding assumes that intra-shard communication and state updating is roughly 20x or more higher than inter-shard communication.

With UTxO ledgers, the lines for sharding can be drawn intelligently and even dynamically as the blockchain's state is simply the expression of all UTxO boxes or encapsulations, with each new UTxO linking explicitly to the segments of state on which it builds. In contrast, account-based ledgers rely on monolithic state [tries](https://medium.com/@eiki1212/ethereum-state-trie-architecture-explained-a30237009d4e) that have no natural points of fracture, thus increasing the demand for inter-shard communication and substantially limiting the scalability improvements offered.

With UTxO ledgers, the lines for sharding can be drawn intelligently and even dynamically, as the blockchain's state is simply the expression of all UTxO boxes or encapsulations, with each new UTxO linking explicitly to the segments of state on which it builds. In contrast, account-based ledgers rely on monolithic state tries that have no natural points of fracture, thus increasing the demand for inter-shard communication and substantially limiting scalability improvements.

### Traceability

Perhaps simplest to discuss among the advantages of a UTxO ledger is the idea of improved traceability. Consider the analogy of cash versus bank balances. When cash is transferred, it is possible to trace exact bills through a chain of transactions regardless of how long. The bills themselves remain economically fungible, but nevertheless they can gather history. This is the exact model of a UTxO ledger with an important exception. Because blockchains are digital and persistent, the ability to trace a singular asset such as a carbon credit or diamond changing hands countless times is practical (and already happening on the Topl Blockchain) instead of theoretical.

On the other hand, account-based ledgers track assets like banks do. If two transactions affect a single balance at the same time (in the same block) traceability is broken. It is not longer possible to match the specific inputs to the balance uniquely to the new outputs.
