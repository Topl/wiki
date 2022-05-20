# Community Inclusive Organization

Central to Topl’s vision of creating a robust impact economy that prioritizes productive contribution is a firm foundation for governance. Without well-designed governance, the long-term vision and purpose of the project cannot be guaranteed.

Most crypto projects seeking to implement such a governance foundation adopt some combination of on-chain and off-chain voting. They then plan for all voting procedures and any associated fund dispersal to eventually be handled by a DAO.

To understand why we will introduce a new governance model, we must first address the shortcomings of traditional DAO-style setups for layer 1 protocols.

DAOs, or Decentralized Autonomous Organizations, come in three primary varieties (with the potential for hybridization):

* Smart-contract fund custodian: “The DAO” is perhaps the purest example of this DAO variety. In this variety, stakeholders pool capital into a smart contract in exchange for voting tokens. Voting tokens entitle them to vote (directly) on what to do with pooled funds and to participate in the potential returns of such investments on a pro rata basis.
* Variable tuning mechanism: Most commonly found in DeFi protocols such as Maker or Aave, a DAO-style setup can allow for the tuning of various parameters that are central to how these protocols operate, such as liquidation ratios and stability fees.
* Consensus rule validator: While DAOs are least commonly found in layer 1 projects, a notable and long-running exception to this is Decred. The Decred blockchain uses a well-developed on-chain process of voting to approve changes to the consensus-level rules of the protocol.

Although any Topl DAO would draw from all three DAO varieties, it is not this combined functionality that has shortcomings. Rather, it is the simplicity with which they must necessarily operate. If we explore the above DAO varieties further, we see that they are consistently paired with substantially less developed off-chain procedures, such as admin-moderated discussion forums, to handle everything except final execution. The challenge here for the governance of layer 1 blockchains like Topl stems from the long development cycles and the repeated rounds of approval for any substantial development effort.

As is apparent from examples like Eth2 or Cosmos Stargate, the critical compromises, decisions, and work of an upgrade is done long before network validators activate a new protocol version at a predetermined block number. Both in theory and in practice, the design of DAOs as presently conceived relegates any community governance to a mere rubber stamp for decisions that have already been made and often carry too much momentum to halt without harming the project.

## The Topl CIO (Community Inclusive Organization)

As an alternative to the DAO, we propose a new model of governance that we believe better addresses the realities faced by blockchain projects and more accurately solves the principal-agent problem. Upon decentralization (timeline here), the Topl Blockchain will be governed and led through a Community Inclusive Organization or CIO.

The first and most critical difference between a CIO and a DAO is that the former is intended to recognize the reality of long-term involvement by a legal entity in project custodianship and execution. By accepting this reality, the CIO can implement rigorous and well-founded protocols for its own governance and relationship with the project ecosystem rather than allowing such protocols and relationships to be relegated to a footnote and unrealistically dismissed.

The Topl CIO will be formed as a foundation in one of several jurisdictions. While the jurisdiction chosen may affect formation and reporting requirements, the chosen jurisdiction will allow the following:

Additionally, the chosen jurisdiction must offer a friendly legal environment for crypto projects while also providing tight regulatory integration with a major economic block. For these reasons, a number of jurisdictions are currently under consideration, including the Netherlands, Switzerland, Malta, and Portugal.

### CIO Governance

The CIO will be governed through a two-tier structure with a directly elected Governing Delegation along with a secondary Executive Council elected by and composed of members of the Governing Delegation. The purpose of this two-tier structure is to capture the viewpoint diversity that the Topl ecosystem hopes to foster while still allowing the CIO to provide effective and efficient guidance to the project.

The Governing Delegation will be variable in size depending on the number of monthly active addresses on the Topl Blockchain, with a minimum size of 10. Growth is governed by the following equation:

$$
governingDelegation= \max(10, \lceil monthlyActiveAddresses^{0.25} \rceil)
$$

Meanwhile, the Executive Council will initially consist of five members: an Executive Director, plus one Director for each established Committee. At inception, the four inaugural Committees will include Protocol Design, Research, Ecosystem Growth, and Monetary Policy. Committees can be added or removed at the election of Arbit holders.

### Election Process

Voting for the Governing Delegation will be conducted off-chain but with cryptographic guarantees made available by verifiable token ownership.

Elections will be regularly scheduled at two-year intervals, with the added possibility for snap elections to be called if necessary. A snap election may be called by submission of a request supported by a yet-to-be-determined percentage of Arbit ownership. In the event of a snap election, the subsequent regular election will occur two years from the date of the snap election (provided there is no subsequent intervening snap election).

Following either a regular or snap election, the Governing Delegation will have 60 days to appoint a full Executive Council. If such an appointment is not successfully made, an election for a new Governing Delegation will be held.

### Voting

While maximum voting power will be determined by Arbit ownership, Arbits must be “spent” to cast a vote. Spent Arbits will enter a CIO reserve fund that can be used to incentivize network development, growth, and participation.

While potentially counter-intuitive, the purpose of such a “pay-to-vote” scheme works to address one of the central criticisms of PoS governance, namely that they enable self-reinforcing plutocracies. With conventional POS governance, holding of the network token grants a user control in all votes in perpetuity (at least as long as they maintain such a holding). In Topl’s voting model, ownership grants such influence in only a single vote.

### (Potential) Need for Legal Entity

Topl's [Quivr DSL](../core-architecture-and-ledger-logic/ledger-logic/smart-tokens.md) and [DAML smart contract layer](../core-architecture-and-ledger-logic/ledger-logic/chain-program-engine.md) will enable the Topl CIO to manage its Development Ecosystem Fund (consisting of Polys) and its Reserve Fund (consisting of Arbits) as well as manage upgrades and forks. Despite this, the possibility remains, and may in fact be a strong likelihood, that the Topl CIO would benefit from the creation of a legal entity that can act as a tightly controlled legal agent. Such a legal entity may be necessary to contract third-party service providers and enter into legal agreements with other parties.

This legal entity, an agent of the Topl CIO, will be formed as a foundation in one of several contemplated jurisdictions. While the jurisdiction chosen may affect some formation and reporting requirements of the foundation, the chosen jurisdiction will necessarily allow the following:

* The entity will not have any capital stock or other form of capital ownership. There will be no “owners” of the entity, only a governing board.
* The governing board of the legal entity must be able to be defined as identical to the current Executive Council of the CIO, which is in turn elected by the Arbit holders.

While initially counterintuitive, the purpose of such a “pay-to-vote” scheme works to address one of the central criticisms of PoS governance — that they are plutocracies. With conventional POS governance, holding the network token grants a user control in all votes in perpetuity (at least as long as they keep their holding). In Topl’s voting model, ownership grants such influence in only a single vote.

In addition to allowing the preceding two features for the foundation, the chosen jurisdiction must offer a consistent and friendly legal environment for crypto projects while also providing tight regulatory integration with a major economic block. For these reasons, a number of jurisdictions are currently under consideration including, the Netherlands, Switzerland, Malta, and Portugal.

## CIO Activities and Token Holder Control

Many blockchain projects seek to eliminate (or minimize) the role of any organizational entity beyond the full set of token holders. The goal here is to resolve the potentially conflicting interests that result from the principal-agent dichotomy simply by eliminating the agent. While appealing, such an argument neglects that the realities of governance for complex projects will in one way or another produce agents. The only question is how well these agents are governed and aligned. You can find more on the “agent-vacuum” here (blog coming soon).

The Topl CIO will propose and discuss priorities for ecosystem growth and protocol development, as well as work to formulate standards and potential revisions to the project’s architecture, tokenomics, and monetary policy. The CIO will be controlled by Arbit holders through annual budget submissions and approvals. As the CIO's reserves will be composed only of Polys (Topl's value-stable currency) and Arbits, the CIO has no ability to fund its activities without the explicit approval of the Arbit holders.

A second key activity of the CIO will be to act as a supervisory body on any and all contractors or developers who have received project funds. As research and software development efforts can require extended periods of work, benefiting from multiple steps of review and reporting, such oversight will be greatly beneficial to the quality and consistency of work funded by the project.


