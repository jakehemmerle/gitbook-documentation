# Consensus

Dock is built on [Substrate](https://substrate.dev/) and uses the consensus mechanism offered by Substrate which is a _hybrid_ as it separates block production and finality and achieves them through different methods. The finality is achieved through a finality gadget called GRANDPA \(**G**HOST-based **R**ecursive **AN**cestor **D**eriving **P**refix **A**greement\). It finalizes chains rather than individual blocks and offers provable finality. More details on GRANDPA are available on the Web3 Foundation's [research page](https://research.web3.foundation/en/latest/polkadot/GRANDPA.html). It is implemented in Substrate in [this pallet](https://github.com/paritytech/substrate/tree/master/client/finality-grandpa).

Dock will start with a Proof of Authority \(PoA\) network and therefore the block production algorithm in this phase will be [Aura](https://openethereum.github.io/wiki/Aura). This algorithm divides time into fixed intervals and gives each validator an equal chance to produce 1 block in round-robin intervals. It is implemented in Substrate in [this pallet](https://github.com/paritytech/substrate/tree/master/client/consensus/aura).

When Dock transitions into utilizing PoS, the block production algorithm changes from Aura to BABE \(**B**lind **A**ssignment for **B**lockchain **E**xtension protocol\) which selects a validator for each _slot_ \(interval of time\) randomly using a VRF \(Verifiable Random Function\). BABE is similar to IOHK's [Ouroboros Praos](https://eprint.iacr.org/2017/573.pdf). More information about this is available on Web3 Foundation's [research page](https://research.web3.foundation/en/latest/polkadot/BABE/Babe.html). It is implemented in Substrate in [this pallet](https://github.com/paritytech/substrate/tree/master/client/consensus/babe).

For development purposes, we will bundle [instant-seal](https://github.com/paritytech/substrate/tree/master/client/consensus/manual-seal) consensus which produces a block as soon as the transaction reaches the node rather than wait for blocks to be produced at a fixed interval. This is helpful when running the SDK against a local node during development.



