# For Protocols

IndependentDisclosure is a peer-to-peer vulnerability disclosure framework that combines smart contracts with carefully structured off-chain processes to enable fair and transparent security disclosures.

---

## Git Safety Tips

**Important Warning**: If you ever receive errors or warnings when trying to push or pull changes during the disclosure process, STOP and examine the repository on GitHub before proceeding. Messages about "non-fast-forward" updates or divergent histories could indicate that someone has rewritten the repository history, potentially modifying terms or commitments maliciously. Never use `--force` with git commands unless you fully understand the implications. Your local copy serves as proof of the original history.

While history modification is considered a very unlikely event (as it's easily detectable bad faith that immediately kills the deal), maintaining a local copy provides simple but robust protection against such attempts. We describe how to do so below.

---

## Phase 1: Initial Contact  

A security researcher has identified a potential vulnerability in your protocol and intends to disclose it responsibly. Here's what to expect:

1. The researcher will contact you through available private channels (e.g., Discord, email, Telegram).  
2. They will share this guide to explain the peer-to-peer disclosure process.  
3. They will have already deployed an [IndependentDisclosure smart contract](https://gist.github.com/0xKorok/cb1925bd68cf919b6d18181d46dd3cce) and created a private GitHub repository [based on this template](https://github.com/TrustlessDAO/independent-disclosure).  

---

## Phase 2: Accessing the Disclosure  

When you're ready to proceed:  

1. The researcher will invite you to their private GitHub repository.  

2. Inside the repository, you'll find the following key files:  
   * [report.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/report.md): Contains the full vulnerability details.  
   * [initial-terms.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/initial-terms.md): Contains the researcher's suggested terms.  
   * [protocol-assessment.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/protocol-assessment.md): Where you will provide your assessment.  
   * [README.md](https://github.com/TrustlessDAO/independent-disclosure/blob/main/README.md): Contains complete process documentation.  

3. Create a local copy of the repository:
   ```bash
   git clone <private-repo-url> local-backup
   ```
   This backup protects you against potential history modifications.

4. Review the report and initial terms carefully. The initial terms are non-binding suggestions and can be negotiated.  

---

## Phase 3: Assessment  

Before submitting your assessment:
1. Sync your local copy to ensure you have the latest version:
   ```bash
   git pull origin main
   ```
2. This pull ensures you have evidence of the original disclosure and terms.

You have full control over assessing the validity of the disclosure. Your assessment options are:  

| Status | What it means | Implications |
|--------|---------------|--------------|
| **Confirmed** | You acknowledge the vulnerability | - Initiates timeline for settlement/mitigation<br>- You'll need to complete `authorization.md`<br>- Maintains confidentiality during fix. |
| **Non-Issue**  | You determine it's not a vulnerability | - Researcher can publish the report immediately.<br>- No further action required. |
| **Won't Fix**  | You acknowledge but won't address it | - Negotiate confidentiality terms if privacy is desired.<br>- If no settlement is reached, the researcher can publish. |  


### Important Notes About Assessment:  

* The suggested timeframe for assessment is 24–72 hours.  
* If you require additional time, provide evidence to justify the extension.  
* Your assessment is considered binding once submitted.  
* Bad-faith negotiation tactics can be publicly exposed by either party.  

---

## Phase 4: Authorization (If Confirmed)  

If you confirm the vulnerability:  

1. Complete the `authorization.md` file in the repository.  
2. Send the commit hash from your official Twitter/Telegram account to the researcher.  
   * This ensures the authenticity of your commitment.  
3. The researcher will add your specified wallet address to the smart contract.  
4. Collaborate with the researcher to agree on settlement terms in `final-terms.md`.  
5. After final terms are agreed, sync your local copy one last time:
   ```bash
   git pull origin main
   ```
   This ensures you have proof of the final agreed terms.

---

## Evidence and Transparency  

The IndependentDisclosure process creates an evidence trail that protects both parties:  

* The smart contract records key events and commitments on-chain.  
* The GitHub repository preserves all communication and agreements.  
* Your local copy of the repository is crucial evidence. Git will warn you if the other party attempts to modify history, requiring a force-pull to accept their changes. These warnings are your signal that bad faith actions may be occurring. You can prove this by sharing your local copy, which contains the original unmodified history.
* Commit hashes serve as timestamps without exposing sensitive vulnerability details.  
* Either party can prove bad faith using the evidence trail.  

This transparency encourages good-faith participation while maintaining confidentiality during the disclosure process.  

---

## Recommendations for Success  

1. **Respond Promptly**: Aim to acknowledge receipt within 48 hours.  
2. **Communicate Clearly**: Use the GitHub repository for all disclosure-related communication.  
3. **Be Professional**: Treat the disclosure process as a collaborative effort.  
4. **Document Everything**: Ensure all relevant communication is recorded in the repository.  
5. **Honor Commitments**: Assessments and agreements are binding.  

---

## Contact Information  

For questions or concerns about the IndependentDisclosure process:  
- Contact the researcher directly through the communication channels they provided.  
- Alternatively, reach out to a [TrustlessDAO representative](https://x.com/0xKorok). Our DMs are open, and we aim to respond within 24 hours.  

---

Thank you for participating in responsible security disclosure. Your cooperation helps make the ecosystem safer for everyone.