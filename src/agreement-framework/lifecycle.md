# Agreement Lifecycle

Let's walk through how these components work together in practice, following the complete lifecycle of an agreement from initiation to completion.

## Initial Steps

The process begins when a security researcher finds a bug. They:
1. Create a private GitHub gist containing their vulnerability report
2. Deploy the on-chain agreement using this gist hash
3. Document and begin thorough contact attempts through all available channels (Discord, Twitter, Email, Telegram, etc.)

This creates a timestamped foundation for the agreement while keeping sensitive details private until appropriate.

## Authorization Verification

Once contact is established, the researcher creates a private GitHub repository containing our standard authorization template. This template provides a structured way for protocols to verify their authority to participate in the agreement.

The responding party then:
- Accesses the private repository
- Updates the template with their details and authorized wallet address
- Commits these changes directly in GitHub
- Sends the commit hash through a public channel (e.g., Twitter, Telegram)

This creates multiple forms of proof:
- Git commit history shows who authorized what wallet
- Public message proves intent to authorize
- Both pieces of evidence are permanently timestamped

## Agreement Progression

With authorization verified, the formal agreement process begins:

1. Initiator sets the verified wallet as the authorized participant
2. Participant accepts initial terms through their wallet
3. Initiator shares full agreement details
4. Both parties negotiate as needed
5. Participant accepts final terms once agreement is reached

Each step is recorded on-chain, creating an immutable record of progression.

## The GDP Alternative

If the responding party doesn't engage, the Gradual Disclosure Process provides a structured alternative:

For Critical Issues (48-hour stages):
1. Day 1: Private contact attempts
2. Day 3: Reveal affected blockchain
3. Day 5: Disclose impact severity
4. Day 7: Identify specific protocol

For Standard Issues (24-hour stages):
1. Day 1: Private contact attempts
2. Day 2: Reveal affected blockchain
3. Day 3: Disclose impact severity
4. Day 4: Identify specific protocol

This timeline:
- Gives multiple chances to engage
- Creates increasing urgency
- Maintains leverage without immediate exposure
- Pauses immediately upon engagement

## Evidence Trail

Throughout the process, a comprehensive trail of evidence is created:
- On-chain: State transitions and participant addresses
- Git: Authorization and agreement details
- Public channels: Cross-platform verification
- Private channels: Contact attempts and negotiation

This evidence becomes crucial if disputes arise, as it provides clear, timestamped proof of:
- Who was involved
- What was agreed to
- When each step occurred
- How the process was followed