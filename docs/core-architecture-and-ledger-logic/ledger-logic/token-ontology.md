# Smart Token Ontology

Tokenizing "real world" assets is a key use case of any blockchain. Among the most common manner one hears blockchain being applied is to _create and track digital twins of X._ This idea has become so common around blockchain that it has begun to obscure the hidden complexities in accomplishing this task effectively. While it may seem almost trivial (or at least as trivial as any task involving a barely 10 year old technology can be) to just digitize an asset, there are a myriad of hidden assumptions that users and businesses inevitably have regarding how should behave. We expect some things to be divisible and interchangeable while others ought to be fixed and unique, or we assume that there exist some items that can be separated and recombined while there are others whose entropy is irreversible.

Tokenizing "real world" assets is a key blockchain use case. Blockchain is often applied to _create and track digital twins of X._ This idea has become so common that it has begun to obscure the hidden complexities in accomplishing this task effectively.

Tokenizing "real world" assets is a key use case of any blockchain. Among the most common manner one hears blockchain being applied is to _create and track digital twins of X._ This idea has become so common around blockchain that it has begun to obscure the hidden complexities in accomplishing this task effectively.

While digitizing an asset may seem almost trivial, there are a myriad of hidden assumptions that users and businesses inevitably have regarding how a digital asset should behave. We expect some to be divisible and interchangeable while others to be fixed and unique, or we assume some can be separated and recombined while others have irreversible entropy.

To address these complexities, Topl has gone beyond the simplistic dichotomy of fungible and non-fungible tokens represented by the ERC20 versus ERC721 created by Ethereum and adopted by numerous other chains. Instead, Topl has developed a rigorous ontology for tokens created on the Topl Blockchain. We believe such a strong foundation is necessary in order to accurately capture the universe of "real world" assets that can be tokenized and build a robust set token-centered functionality without introducing confusion and difficulty to developers and users.

To address these complexities, Topl has gone beyond the simplistic dichotomy of fungible and non-fungible tokens represented by the ERC20 versus ERC721 created by Ethereum and adopted by numerous other chains. Instead, Topl has developed a rigorous ontology for tokens created on the Topl Blockchain. We believe such a strong foundation is necessary to capture the universe of "real world" assets that can be tokenized and to build a robust, set, token-centered functionality without introducing confusion and difficulty to developers and users.

For this reason, Topl has endeavored to tightly and efficiently couple advanced functionality with tokenized-assets themselves in the core design of our blockchain. We employ a _smart_ _token_ _ontology_ framework which combines user-defined, protocol-level assets and our [Quivr DSL](smart-tokens.md). Unpacking this, let's first introduce what is meant by user-defined, protocol-level assets. Unlike with many other blockchains, a user can classify and mint their own arbitrary assets on chain without the use of any additional code beyond the protocol itself. By not having to rely on abstractions to simply create and mint new assets, Topl makes user-defined assets "first-class citizens" on our blockchain.

While it may seem almost trivial (or at least as trivial as any task involving a barely 10 year old technology can be) to just digitize an asset, there are a myriad of hidden assumptions that users and businesses inevitably have regarding how should behave. We expect some things to be divisible and interchangeable while others ought to be fixed and unique, or we assume that there exist some items that can be separated and recombined while there are others whose entropy is irreversible.

To address these complexities, Topl has gone beyond the simplistic dichotomy of fungible and non-fungible tokens represented by the ERC20 versus ERC721 created by Ethereum and adopted by numerous other chains. Instead, Topl has developed a rigorous ontology for tokens created on the Topl Blockchain. We believe such a strong foundation is necessary in order to accurately capture the universe of "real world" assets that can be tokenized and build a robust set token-centered functionality without introducing confusion and difficulty to developers and users.

Within Topl's token ontology, an asset is categorized through five questions:

* What is the **atomicity** of the asset? Or what is the base unit that we use to count instances of the asset?
* Is the asset **fungible**? Can any two units be interchanged with each other without any effect?
* Is the asset **unique**? Can only one instance of the asset exist?
* Is the asset **divisible**? Can the asset be separated into multiple parts without becoming something different?
* Are such divisions **reversible**? When the asset is divided can it be recombined without any additional work?

Seeing as four of these questions are binary (yes/no), we might expect our ontology to produce 16 distinct categories. However, 10 of these potential categorizations are not logically possible. For example, if an asset is fungible, it cannot also be unique; if an asset is not divisible, such divisions obviously cannot be reversible (since they're already impossible). Ruling out these impossibilities, we have six distinct categories of tokens in our ontology, as pictured below.

![](<../../assets/Brown Bag Sessions - Frame 1.jpg>)

These six asset categories are capable of capturing the fundamental behavior of tangible assets ranging from coffee (fungible, reversibly divisible) to diamonds (non-fungible, non-reversibly divisible), as well as intangible assets ranging from commodity futures (fungible, non-divisible) to loan agreements (non-fungible, non-divisible).

Topl's token ontology forms the basis for future token functionality as we will see when discussing [Smart Tokens](smart-tokens.md) and Impact Credits.

Topl's token ontology forms the basis for future token functionality, as we will see when discussing [Smart Tokens](smart-tokens.md) and Impact Credits.
