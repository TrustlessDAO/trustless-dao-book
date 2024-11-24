# The Agreement Framework

Smart contracts excel at maintaining simple, verifiable state - recording what has happened and when. Where they often fall short is in managing complex human agreements that require nuanced interpretation, negotiation, and flexibility.

Yet some of the most powerful smart contracts are also the simplest. Consider [UniswapV2's core contracts](https://github.com/Uniswap/v2-core/tree/master/contracts) - these few hundred lines of code have enabled billions in trustless trading. The power comes not from complex on-chain logic, but from careful design.

This insight drives our approach to decentralized agreements: use minimal but sufficient on-chain state to anchor carefully designed off-chain processes. The blockchain serves as an immutable record of key moments - when terms were offered, when they were accepted, when agreements were finalized. Everything else - the detailed terms, the disclosure, and the negotiation - happens off-chain using established tools and platforms. The specifics of final payment are up to the involved parties.

> The key is that if payment doesn't occur as agreed, either side can publicly reveal information that proves the actions of the other side are deviating from the agreed terms.

This hybrid design creates something powerful - agreements that are truly decentralized yet practically enforceable, with clear incentives for honest behavior by all parties. Let's examine how.