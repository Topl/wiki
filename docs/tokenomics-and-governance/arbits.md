# Arbits

The Arbit acts as protocol token of Topl’s proof-of-stake blockchain. Arbit ownership entitles parties to participate in block creation and ecosystem governance. Critically, however, Arbits are not used for the payment of transactions fees (i.e. as a currency), drawing a distinction between Arbits and similar PoS protocol tokens such as Ada (Cardano), Dots (Polkadot), and SOL (Solana). We elaborate on this decision to separate staking from payment functionality in a dedicated section on the Poly, Topl’s currency token, but fundamentally this design was driven by recognition of the complex and conflicting dynamics (tokenomics) required in an effective token of either variety.

### Inflation

Through the 13-year history of the blockchain space, questions of inflation have loomed large for every new blockchain project. While these questions initially focused solely on a monetary perspective, as all early protocol tokens were intended to be pure currencies, these questions were altered by the proliferation of ICOs and other launches of blockchain-enabled projects and new proof-of-stake blockchains. As projects began seeking seed or launch capital, inflation questions shifted to be driven by investor concerns over future dilution, with total token caps being sought to protect ownership shares rather than recreate something like the gold standard.

While we fully recognize the desire for blockchain investors to protect themselves from inflationary dilution, we believe that the sustained viability of the endeavor must be considered primary. A large stake in a worthless asset is still worthless.

To this end, Topl has designed an issuance plan for Arbits intended to support both robust community involvement and strong continued development and improvement efforts.

### Revenue Correlated Minting

The first component of Topl’s token issuance protocol establishes the network’s inflation schedule. Instead of electing for either issuing new Arbits at a fixed percentage annually (following Milton Friedman’s K-Percent Rule) or with a fixed number of Arbits per year (after Ethereum’s original disinflationary model), Arbit inflation will be dynamic, based on positive changes in collected transaction fees (_protocol revenue_). If protocol revenue increases by $\Delta$, the supply of Arbits will also be increased by $\Delta$. However, if protocol revenue decreases, the Arbit supply will remain unchanged.

!!! Note
    While several variables were consider as potential drivers for Arbit supply changes, including Arbit price, protocol revenue was chosen in part because this information in endogenous to the system, meaning there is no oracle required.

Algorithmically, this will be carried out as follows starting at epoch _n_ (more on epochs [here](../fees-currency-and-consensus/taktikos-pos.md)):

* When $>\frac{2}{3}$ of slots in epoch $n$ have elapsed, the protocol will calculate $\Delta$ in protocol revenue between epochs $n-1$ and $n-2$;
* If $\Delta>0$, the protocol will calculate the number of new Arbits to be issued in epoch $n+2$ that will create an inflation rate equal to the current $\Delta$.
* During epoch $n+2$, new Arbits totaling $\Delta\times \textit{totalSupplyArbits}$ will be distributed proportionally to block producers.

The motivation for this choice is network security. In a proof-of-stake blockchain, the ledger’s security is linearly correlated with the percentage of participating stake (that portion involved in block production). What the price-correlated minting achieves is a design in which those token holders not actively participating (either directly or through delegation) in securing the network do not participate in any price appreciation of the asset that they hold. This strengthens the incentive to participate in block production, boosting the network’s security, which, in turn, according to analysis provided by the Fat Protocol Thesis, increases the total value of other assets (currencies, commodities, etc.) that can be hosted on the Topl Blockchain.

### Funding development through baseline inflation

Having established our base inflation mechanism for Arbits, we now consider how such inflation can be used to incentivize continued protocol and tooling development in addition to supporting network security. This feat can be accomplished by electing to divert a portion of new Arbit creation into an ecosystem development fund. However, diverting from a fixed available supply will create misalignment between those securing the network and those working to improve it. Instead, we can keep these two interests aligned by revising our inflation equation to the following equation:

$$
(\Delta + B) * \textit{totalArbitSupply}
$$

where $B$ is the rate of new Arbit minting (chosen by Arbit holders on a periodic basis) that will fill the protocol’s ecosystem development fund.

While determined through Arbit governance, this rate of inflation will nevertheless be constrained to be within certain ranges depending on the total market capitalization of Arbits.

[//]: # (Comment: Who determines the market cap?)

| Market Capitalization | Annual Inflation Rate $B$ |
| --------------------- | ------------------------- |
| <$500MM               | 8% - 16%                  |
| $500MM to $2bn        | 4% - 8%                   |
| $2bn to $10bn         | 2% - 4%                   |
| >$10bn                | <2%                       |

### A bias toward productive contribution

Given the non-neutrality in design and potential for high rates of nominal inflation that may be experienced especially in the early years of Topl’s ecosystem development, our differentiated token issuance mechanism requires motivation beyond even that which has been provided.

While a first defense may claim that the need to continually fund protocol and ancillary development, there are other “permanent incentive models” such as Joel Monegro’s _buyback and make_ proposal. The majority of these existing perpetual funding models are neutral between capital and productive contribution, whereas we seek to bias Topl’s economy toward productive contribution.

In addition to the desire to prevent Arbit ownership from becoming a rent-seeking activity driving the system toward self-reinforcing centralization, we believe our design’s imposed bias toward those actively securing the network and contributing to its continued development can drive a substantial long-term advantage, a fact hopefully made apparent through the following argument.

1. In a proof-of-stake blockchain, the value of the staking token is most fundamentally the net present value discounted cash flows of all transaction fees that the network will collect.
2. Maximizing user adoption requires continuous improvement to the blockchain’s technological core and ancillary tooling, as well as consistent investment in community building.
3. For a fixed market capitalization, a proof-of-stake blockchain with a higher participation rate for block production can support a greater amount of user-generated assets.
4. From 2 & 3, a design that incentivizes both continued development and greater participation in block production will drive greater adoption and usage.
5. From 1 & 4, a proof-of-stake blockchain with higher levels of usage will collect more transaction fees and thus have a more valuable staking token.

It is possible that even in the absence of such direct and preferential incentives, a blockchain’s token holders will themselves act in the protocol’s best interest both in providing robust security and funding continual development. However, such a setup has all the markings of creating a tragedy of the commons, a potentially fatal design flaw to which so-called rational markets have proven reliably vulnerable.
