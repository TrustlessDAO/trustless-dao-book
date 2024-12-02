# For Researchers

IndependentDisclosure is a simple smart contract designed to be combined with carefully structured off-chain processes to enable effective and fair peer-to-peer vulnerability disclosure.

---

## Git Safety Tips

**Important Warning**: If you ever receive errors or warnings when trying to push or pull changes during the disclosure process, STOP and examine the repository on GitHub before proceeding. Messages about "non-fast-forward" updates or divergent histories could indicate that someone has rewritten the repository history, potentially modifying terms or commitments maliciously. Never use `--force` with git commands unless you fully understand the implications. Your local copy serves as proof of the original history.

While history modification is considered a very unlikely event (as it's easily detectable bad faith that immediately kills the deal), maintaining a local copy provides simple but robust protection against such attempts. We describe how to do so below.

---

## Phase 1: Create Report and Begin Contact Attempts  

1. Finalize the vulnerability report locally, then begin reaching out to the affected protocol through all available private channels (Discord, email, Telegram, etc.). Document these attempts thoroughly.

---

## Phase 2: Make Disclosure (Best Case Scenario)  

1. Once contact is established, start by sharing details of the peer-to-peer disclosure process to set clear expectations for the protocol. TrustlessDAO's [protocol guide](protocol.md) can be used for this.

2. Clone the [IndependentDisclosure repository template](https://github.com/TrustlessDAO/independent-disclosure) provided by TrustlessDAO to your GitHub account as a private repository.  
   * TrustlessDAO is not notified when the public template is used.  

3. Deploy an [IndependentDisclosure contract](https://gist.github.com/0xKorok/cb1925bd68cf919b6d18181d46dd3cce) and call the `setCommitHash` function, passing the initial commit hash of the private GitHub repository created in the previous step.  

4. Edit your repository's [initial-terms.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/initial-terms.md) file to add your terms. Initial terms are suggestions for the protocol; only final terms are binding.  

5. Update your repository's [report.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/report.md) file to include the full vulnerability report.  
   * These steps establish a provable timestamp of your discovery, ensuring that anyone intercepting or receiving the disclosure details from you cannot falsely claim they found it first.

6. If you haven't already created a local backup of your repository:
   ```bash
   git clone <your-private-repo-url> local-backup
   ```
   This local copy provides evidence if the protocol attempts to modify history later.

7. Invite protocol representatives to the repository and direct them to the ["Protocol Action Items"](https://github.com/TrustlessDAO/independent-disclosure/blob/main/README.md#protocol-action-items) section of the README, which summarizes their required actions.  

8. Wait for the protocol to update the [protocol-assessment.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/protocol-assessment.md) file with their response.  
   * Bad-faith negotiation tactics, such as disregarding an agreed-upon waiting period, can be exposed at any time by either party. This can be done without revealing disclosure details and will be judged by the court of public opinion.

9. Once the protocol updates protocol-assessment.md, sync your local copy:
   ```bash
   git pull origin main
   ```
   This ensures you have proof of their original assessment.

10. The protocol's assessment should be considered binding. Each response dictates a distinct path:  

|  Status  | Implications |
|----|---------|
| **`Confirmed`** | Initiates the extended timeline for settlement/mitigation. The protocol should proceed to complete [authorization.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/authorization.md).   |
| **`Non-Issue`** | Grants immediate permission to go public with the full report.  |
| **`Won't-Fix`** | Indicates acknowledgment. If the protocol prefers the issue remain private, negotiate a fair confidentiality price. If no timely settlement is reached, permission is granted to make the report public.   | 

11. Once authorization is complete, call the `setParticipant` function on the IndependentDisclosure contract with the specified wallet address. Proceed to collaborate with the protocol to agree on final terms.  
   * If needed, remind the protocol to DM the commit hash for the authorization from their official Telegram or Twitter. This ensures commitment authenticity.  

12. After final terms are agreed, sync your local copy one last time:
    ```bash
    git pull origin main
    ```
    This ensures you have proof of the final agreed terms.

13. The disclosure process is now complete. If the report was not confirmed, periodically check the protocol's deployed contract for fixes.
    * If a fix is implemented without prior agreement, present the case for payment to the court of public opinion, citing verifiable on-chain evidence from the disclosure process.  

> **Note**: TrustlessDAO's Arbiter system will streamline the process of resolving disputes in cases of on-chain dishonesty or bad faith.

---

### Alternative Phase 2: Protocol Cannot Be Reached (Worst Case Scenario)  

> **Note**: TrustlessDAO is implementing solutions to minimize this scenario. For now, researchers must use their judgment on how to proceed.  

If the protocol does not respond to your contact attempts, consider a **gradual disclosure process**. The primary goal is to establish communication, not to disclose full details immediately. Once communication is established, the protocol assumes control.  

#### Disclosure Stages:  
1. **Chain ID**: e.g., "Vulnerability on Ethereum mainnet."  
2. **Vulnerability Category**: e.g., "Access control in governance."  
3. **Impact Description**: e.g., "Unauthorized admin control."  
4. **Technical Preview**: e.g., "Timelock validation issue."  
5. **Protocol Name**  
6. **Full Report**  

> Another approach is to gradually disclose to individuals indirectly associated with the protocol (e.g., investors, contributors, or known security teams). Document these attempts and their results. Start with **Protocol Name + Chain ID** as the first stage to assess their willingness to help.  

If the protocol begins engaging in good faith, pause the gradual disclosure process and transition to [Phase 2: Make Disclosure (Best Case Scenario)](#phase-2-make-disclosure-best-case-scenario).  

---

## Recourse and Evidence  

If either party fails to honor the agreed terms:  
- Present evidence from GitHub repositories and the on-chain contract publicly.  
- Use the contract’s state transitions and Git commit history as immutable proof of the disclosure process and commitments.  
- Leverage the court of public opinion by presenting the most compelling, verifiable evidence.  

By using IndependentDisclosure, you maintain leverage through controlled information disclosure while creating a clear evidence trail. This process encourages good-faith participation from protocols and provides a fair resolution path for disputes.  
