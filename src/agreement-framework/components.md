# Core Components

Effective decentralized agreements require more than just smart contracts. They need a carefully designed system of components that work together to create trust, verify actions, and encourage honest behavior. Our framework consists of three core components:

## The On-Chain Agreement

At the heart of the framework is [IndependentDisclosure](https://gist.github.com/0xKorok/cb1925bd68cf919b6d18181d46dd3cce) a minimal smart contract that serves as an immutable record of key moments in an agreement. It captures just three essential states:
- When an agreement is initiated
- When initial terms are accepted
- When final terms are accepted

This simplicity is intentional. Rather than trying to encode complex rules or arbitration logic on-chain, the contract serves as an anchor point - a source of truth for the most crucial state transitions in an agreement.

## The Authorization Process

Between the on-chain states lies a careful dance of verification and trust-building:
1. The agreement initiator creates private documentation
2. The responding party verifies their authority to participate
3. Both parties create permanent, verifiable records of their intentions

This process uses existing platforms (like GitHub) and social proof (like public messages) to create strong evidence of authorization and intent, without requiring complex on-chain verification.

## The Gradual Disclosure Process

When participation in an agreement is time-sensitive, encouraging prompt engagement becomes crucial. The Gradual Disclosure Process (GDP) provides this encouragement through carefully staged information release:

1. Initial private outreach with minimal details
2. Progressive revelation of relevance
3. Increasing public visibility
4. Full public disclosure as a last resort

GDP turns information timing into leverage, creating strong incentives for timely engagement while remaining ethical by:
- Providing multiple opportunities to engage
- Moving slowly enough for considered response
- Pausing immediately upon good faith engagement
- Protecting both parties' interests throughout

## Working Together

These components complement each other in crucial ways:
- The on-chain contract provides immutable evidence
- The authorization process creates verifiable identity
- GDP encourages timely, good faith participation

None of these components alone would enable effective agreements. But together, they create an environment where:
- Intentions become verifiable
- Actions become accountable
- Good faith participation becomes the most practical choice

This hybrid approach - combining minimal on-chain state with carefully designed off-chain processes - enables agreements that are both truly decentralized and practically effective.