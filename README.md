# The TrustlessDAO Book

This book explains how security researchers can safely disclose vulnerabilities to protocols, even when no official bug bounty program exists. We explore:

## The Current Problem
- White-hat researchers limit themselves to bounty-covered code
- Black-hat hackers look everywhere 
- Many protocols remain under-examined by friendly researchers

## A Better Approach
IndependentDisclosure combines:
- A simple smart contract that records key commitments
- A standardized GitHub repository structure for secure communication
- Clear procedures that protect both parties through transparency

The system enables researchers to work as freely as black-hat counterparts while maintaining strong ethical standards.

## Key Resources
- [IndependentDisclosure Template Repository](https://github.com/TrustlessDAO/independent-disclosure)
- [IndependentDisclosure Smart Contract](https://gist.github.com/0xKorok/cb1925bd68cf919b6d18181d46dd3cce)
- [Protocol Guide](https://gist.github.com/0xKorok/3bcf7f66c62c9bd3f5a95b666b30ab16)
- [Researcher Guide](https://gist.github.com/0xKorok/3c01ba5a7478863cc76ce3cb43559632)
- Follow our progress on X: [@theTrustlessDAO](https://x.com/theTrustlessDAO) and [@0xKorok](https://x.com/0xKorok)

## Quick Start
Run locally with [mdBook](https://rust-lang.github.io/mdBook/):
```bash
mdbook serve
```