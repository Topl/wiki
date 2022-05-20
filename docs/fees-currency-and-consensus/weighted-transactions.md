# Weighted Transactions

When it comes to costs, there are few technologies that present users with a range comparable to competing blockchains. Transaction fees may range from a thousandth of a cent to surges above 100 dollars (US). While we will not concern ourselves with the various reasons that this range exists, we will lay out the issues with each of these two extremes and then demonstrate how the resulting apparent no-win situation can be resolved.

First, let’s establish the upper constraints on transaction fees. As a technology that presents itself as inclusive and opening both finance and general economic opportunity, it is a paramount concern that the fee structure presented by blockchain technology be aligned with this goal. The World Bank currently sets an income of $1.90 per day as the threshold for extreme poverty, accounting for nearly 700 million individuals. Meanwhile, just shy of half (43.5%) of the world’s population subsists on less than $5.50 per day. From this it is easy to establish the requirement that if blockchain usage is intended to become a daily reality for groups such as smallholder farmers in the Global South, daily expenditures towards transaction fees must come in at or below $0.01 with each transaction falling in the range of $0.001 to $0.002.

Having established at least one upper bound on transaction fees, we must establish the second condition, namely that in order to be considered maximally secure, a proof-of-stake blockchain network must collect (or expect to collect) a certain amount of transaction fees. The logic behind this requirement has three parts.

1. A POS blockchain is rendered unsecure when the cost of attacking the blockchain falls below the benefit one could theoretically obtain by launching such an attack.
2. The cost of attacking a POS blockchain linearly scales with its total market capitalization (assuming constant levels of staking participation).

The total market capitalization of a POS blockchain can be best approximated as the net present value of future transaction fees.

While we expound on this argument here (blog coming soon, 1), let us move on for a moment to the consequence of accepting the simplified premise that to be secure a proof of stake blockchain must collect sufficient transaction fees.

In 2020, payment card networks processed a combined total of 468 billion transactions worldwide with the largest processor, Visa, handling 188 billion transactions. Even at such scales, more than 400 times the current Ethereum network usage, the upper bound established by our desire to see adoption across the Global South would cap the total transaction fees that could be collected at ~$280MM, far below the threshold required to support a secure market capitalization.

Given that we both do not wish to push the limits of affordability for the most vulnerable populations and recognize that an essential global infrastructure cannot be sustained on revenues of around a quarter billion dollars, we must identify a way to “square the circle”.




In 2014, Ethereum introduced the concept of differentiated transaction costs based on the idea of computational complexity. While this is an essential spam prevention mechanism for any blockchain that presents a Turing-complete execution layer, it fails to capture the most expensive resource involved in maintaining a blockchain network. Given that blockchains are both fully redundant and maintain a complete ledger history from genesis, storage, rather than computation, represents the most constrained and expensive resource in maintaining a blockchain network.

Given this, we propose a system by which transactions on the Topl Blockchain are priced based on their ledger weight, or how much previous ledger state they may either require or rely on. To understand this system, let us begin with simple transactions, the minting and transfer of user-defined assets in Topl’s UTxO-ledger blockchain.

![](<../assets/Weighted Transactions - Frame 1.jpg>)

In the above transaction flow, we can see that each UTxO (_asset box_) is assigned a weight. This weight begins at 1 upon minting and increments by 1 for each child box. In the event that two boxes are combined (e.g. representing when two batches of coffee or are blended together at roasting), the produced output carries the combined weight plus 1.

The ledger weight of boxes is connected to transaction fees (paid in Polys), through the following formula:

$$
\sqrt{(1+\sum_{\textit{inputBoxes}} \textit{ledgerWeight} )}\times \textit{baseFee}
$$
