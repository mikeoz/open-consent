> **History.** This Position Paper (version 4.0, 10 April 2026) was posted that day as [Issue #162](https://github.com/webmachinelearning/webmcp/issues/162) in the WebMCP repository of the W3C Web Machine Learning Community Group. It was closed the same day as not actionable for the WebMCP specification; the maintainers asked for concrete proposals for the specification instead. It is published here unchanged as the record of that submission. Names and product status have since changed; the current framework is described in this project's README.

---

**POSITION PAPER**

**The Human Consent Layer:**

A Standardizable Consent Mechanism

for AI Agents Acting on Behalf of Humans

The Openly Trusted Company

Version 4.0 • April 10, 2026 • Final for W3C Submission

*Submission Target: W3C Web Machine Learning Community Group*

*Cross-reference: AI Agent Protocol CG • Agentic Integrity Verification Specification CG • Agent-to-Web Framework CG*

*My data + Your AI + My control = Living Intelligence*

## Version History

| **Version** | **Date**     | **Change Summary**                                                                                                                                                                                                                   |
|-------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1.0         | Feb 2026     | Initial submission: CARD architecture for agentic web trust                                                                                                                                                                          |
| 1.2         | Feb 27, 2026 | Enforcement tier precision amendments; PPA Exhibit alignment                                                                                                                                                                         |
| 2.0         | Apr 2, 2026  | Green Shield (CBE) operational. Claude Code source leak validates trust gap. Industry validation expanded.                                                                                                                           |
| 3.0         | Apr 4, 2026  | Human Consent Layer (HCL) canonical definition. Consent chain thesis. CARD-as-context framework. DTG convergence.                                                                                                                    |
| 4.0         | Apr 10, 2026 | Final W3C submission. HCL as standardizable mechanism; ATL as reference architecture. W3C landscape alignment: AIVS CG, AI Agent Protocol CG, A2WF CG, AIJE CG cross-references. Company name updated to The Openly Trusted Company. |

# Abstract

AI agents increasingly act on behalf of humans—reading files, executing code, making purchases, sending messages. Every major platform is racing to deploy agents with maximum autonomy. Multiple industry frameworks address pieces of the resulting trust gap: OWASP catalogs threats, AWS classifies deployment architectures, Meta constrains agent design, NVIDIA isolates execution, Mastercard governs agentic payments, and the Decentralized Trust Graph (DTG) standardizes agent identity and delegation.

Each framework answers a question about the agent. None answers the question about the human: did the human actually say yes—and did they understand what they were saying yes to?

This Position Paper proposes the Human Consent Layer (HCL) as a standardizable consent mechanism for the agentic web. The HCL is the specific technical contribution: the mechanism that presents context a human can understand, captures their Allow or Block decision, and enforces it with cryptographic proof. No override. No bypass. Silence is denial.

The Agent Trust Layer (ATL) is the reference architecture that demonstrates how the HCL operates within a complete trust stack—alongside identity, delegation, guardrails, and audit infrastructure. The relationship is analogous to WebMCP and the broader browser-agent interaction model: the standard is the specific mechanism; the architecture is the ecosystem it operates within.

*MCP standardized the connection between AI agents and tools. The HCL standardizes the consent between AI agents and humans. CROCbox is the proof that it works.*

# 1. The Trust Gap: April 2026

## 1.1 The Market Has Chosen Speed Over Safety

The agent economy in April 2026 is defined by a single pattern: every major platform is racing to deploy agents with maximum autonomy and minimum human oversight. Three developments crystallize this pattern:

OpenClaw’s MCP announcement promised “self-spawning agents in 5 lines of code”—with no consent layer, no trust signal, and no audit trail. Anthropic’s Claude Code source leak revealed an always-on agent architecture consolidating memory, controlling the computer, and running while the user is idle. And the XZ Utils supply chain attack—which took a human two years to engineer—was replicated by an AI agent in two weeks, demonstrating that agents can rapidly exploit trust-building mechanics.

## 1.2 The Stakes

Without standardized human authority mechanisms, agents operate with minimal oversight, users have no real-time control over agent actions, no accountability trail exists when agents make mistakes, and trust becomes provider-dependent rather than user-controlled.

# 2. The Three Realities of Trust

**Reality 1: Trust is an inherently human emotion that cannot be met by science alone.** OWASP provides threat lists. AWS provides scoping matrices. Meta provides design constraints. The DTG provides cryptographic identity and delegation. All are necessary contributions. None addresses the human’s need to feel confident in the system. The HCL bridges this gap by providing a visible, understandable trust signal—the Shield—that translates technical assessment into human confidence.

**Reality 2: Confidence requires transparency.** The human must see the agent’s trust posture (Shield color), understand what consent level they are receiving (CBE vs. CBD), and have access to a tamper-evident record of every decision (audit log). CARDs translate machine information into human-comprehensible context. The HCL requires all three.

**Reality 3: Trust is a choice that must be respected and enforced if it is to be offered.** The human’s Allow or Deny decision is not advisory. It is machine-enforced. No code path exists to override the human’s denial. This is the architectural distinction that separates the HCL from monitoring tools, guardrail frameworks, and advisory systems.

# 3. The Human Consent Layer (HCL)

The Human Consent Layer is this paper’s core contribution—the specific, bounded mechanism that no other entity in the agent trust space provides. The HCL begins where CARD context is presented to the human and ends where the human’s decision is cryptographically recorded.

## 3.1 The Canonical Consent Chain

The HCL thesis reduces to a chain of four claims. Each link depends on the one before it. If any link fails, the chain fails.

| **Link** | **Claim**                      | **Grounding**                                                                                                                  | **Normative Force**                                                                                                                |
|----------|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| 1        | Only a human can give consent. | Trust is a human emotion. Machines can verify, enforce, and record consent, but cannot originate it.                           | No system-generated approval constitutes consent. The human MUST be in the decision loop.                                          |
| 2        | Consent requires context.      | The legal definition of consent requires that the person understands what they are consenting to.                              | An HCL-conformant implementation MUST present context the human can comprehend before soliciting a consent decision.               |
| 3        | CARDs provide context.         | CARDs translate machine-readable requirements into human-comprehensible context. Four types: Entity, Data, Use, Boundary.      | An HCL-conformant implementation MUST present CARD-typed context. The four CARD types define the minimum context envelope.         |
| 4        | The HCL enforces the decision. | The HCL is the technical mechanism: consent card presentation, Allow/Block binary, fail-closed invariant, SHA-256 audit chain. | Consent MUST be machine-enforced. No code path may override a Deny. Silence is Deny. Every decision is cryptographically recorded. |

## 3.2 The Informed Consent Standard

The legal definition of consent—across medical, contractual, and regulatory domains—requires two conditions: (a) the person giving consent understands what they are consenting to, and (b) the decision is voluntary.

Every digital consent mechanism that exists today fails this standard. Cookie banners, terms of service, permission dialogs—all solicit “consent” without providing context the human can comprehend. The Agent Economy compounds this failure. Agents operate on tool catalogs, API scopes, file paths, and shell commands—information that is inherently machine-readable and inherently opaque to humans.

The CARD model maps to the informed consent standard: Entity CARDs answer “Who is asking?” Data CARDs answer “What data?” Use CARDs answer “What will be done?” Boundary CARDs answer “Where and when?” The consent card presents the Allow/Block decision with a fail-closed invariant: no response equals Deny.

## 3.3 The HCL’s Position in the Combined Architecture

The HCL does not operate in isolation. It occupies a specific and bounded position in a five-layer agent trust architecture:

| **Layer**              | **Function**              | **Who Builds It**        | **Inside HCL?** | **Consent?** | **W3C Cross-Ref**          |
|------------------------|---------------------------|--------------------------|-----------------|--------------|----------------------------|
| Identity & Delegation  | Proves agent identity     | DTG (ToIP, DIF)          | No              | No           | AI Agent Protocol CG       |
| Safety & Guardrails    | Protects from danger      | OWASP, AWS, Meta, NVIDIA | No              | No           | WebML CG (WebMCP security) |
| Context (CARDs)        | Translates for human      | OpenlyTrusted (ATL)      | YES — input     | Yes          | A2WF CG (governance)       |
| Consent (HCL)          | Enforces human decision   | OpenlyTrusted (ATL)      | YES — core      | Yes          | This Position Paper        |
| Audit & Accountability | Records with crypto proof | ATL audit chain + DTG    | Partial         | N/A          | AIVS CG, AIJE CG           |

The critical distinction: Every other layer answers a question about the agent. The HCL answers a question about the human: “Did the human say yes—and did they understand what they were saying yes to?”

## 3.4 The CVS Pharmacy Analogy

You walk into a CVS pharmacy to pick up a prescription for someone else. At the pharmacy counter, the pharmacist asks for your driver’s license and insurance card. You hand them over without hesitation. Why? Because you fully understand the context: the person is authorized by the healthcare system (Entity), your license proves identity and your insurance card proves payment authority (Data), they will verify and dispense the prescription (Use), and this is happening at the pharmacy counter within the healthcare system’s rules (Boundary). You consent because the context is legible.

Now you walk to the front of the store with a Coke and a candy bar. You have cash. The same person comes to the register and asks for your driver’s license and insurance card. Same person. Same cards. Different context. You say no—instantly and effortlessly. A cash purchase does not require identity verification. The request does not match the context.

That is informed consent. That is what CARDs enable in the digital world. The decision is inherently human (Link 1); the decision quality depends on context (Link 2); the four CARD types map to the four kinds of context the human naturally evaluates (Link 3); and the pharmacy counter is the enforcement environment (Link 4).

## 3.5 Calibrated Consent: The Expert Ski-Rental Model

The Expert Ski-Rental model (Beginner/Intermediate/Expert) allows the human to calibrate how much context they need for future consent decisions of a given type. At Expert level, the human may choose “trust this tool type” for a session. This is calibrated consent, not reduced consent. Four constraints ensure this: (a) initial decisions establishing Expert level MUST be fully informed; (b) Expert-level session grants MUST be revocable at any time; (c) the audit chain MUST record both original and subsequent decisions; (d) Expert level MUST be per-tool-type, not blanket.

# 4. Two-Shield Conformance Model

The HCL defines two conformance levels, reflecting the reality that not all platforms provide identical consent hooks. As of April 2026, both levels are operational:

| **Attribute**     | **Green Shield (CBE)**                                          | **Yellow Shield (CBD)**                                               |
|-------------------|-----------------------------------------------------------------|-----------------------------------------------------------------------|
| Normative Level   | MUST (normative)                                                | SHOULD (conformant)                                                   |
| Consent Timing    | Before Execution — action does not occur until human authorizes | Before Delivery — action executed, result held pending human decision |
| Human Control     | Whether the action happens                                      | Whether the result is delivered                                       |
| Status (Apr 2026) | OPERATIONAL — CROCbox Green Shield                              | OPERATIONAL — CROCbox v1.0-alpha                                      |

# 5. The HCL in the Standards and Industry Landscape

The HCL occupies a distinct position in a layered trust architecture. SSL secured the pipe. OAuth secured the handshake. The DTG proves who the agent is and who authorized it. The HCL ensures the human actually said yes. It is the consent enforcement mechanism that makes all other security and identity frameworks visible and controllable by the human.

| **Layer**    | **Function**      | **Who**              | **Example**        | **Human Visible?** | **Human Control?** | **Consent?**     |
|--------------|-------------------|----------------------|--------------------|--------------------|--------------------|------------------|
| Threat ID    | Catalog risks     | OWASP                | ASI01–10           | No                 | No                 | No               |
| Scoping      | Classify deploy   | AWS                  | Scope 1–4          | No                 | No                 | No               |
| Design       | Constrain arch    | Meta                 | Rule of Two        | No                 | No                 | No               |
| Sandbox      | Isolate exec      | NVIDIA               | NemoClaw           | No                 | No                 | No               |
| Payment Gov. | Govern txns       | Mastercard           | Agent Pay          | Partial            | Pre-auth           | Txn only         |
| Identity     | Agent ID          | DTG/ToIP             | VRCs, PHCs         | No                 | No                 | No               |
| **Consent**  | **Human control** | **HCL (this paper)** | **CARDs + Shield** | **YES**            | **Every action**   | **Every action** |

# 6. The DTG Convergence: Identity and Delegation Meet Consent

The Decentralized Trust Graph (DTG) is a joint specification effort of the Trust Over IP Foundation (ToIP) and the Decentralized Identity Foundation (DIF), chartered under LF Decentralized Trust. The DTG validates the HCL thesis from the identity side—and the HCL fills a gap the DTG does not address: per-action runtime consent.

**What the DTG provides:** Agent identity via DIDs, authenticated delegation via Verifiable Relationship Credentials (VRCs), proof of personhood via Personhood Credentials (PHCs), and trust network scalability via Verifiable Trust Communities (VTCs) and the Trust Registry Query Protocol (TRQP).

**What the HCL provides that the DTG does not:** Per-action runtime consent (the consent card), a visible trust indicator (the Shield), a tamper-evident runtime audit trail (SHA-256 hash chain), and fail-closed enforcement (timeout = Deny).

**The combined architecture:** The DTG proves who the agent is and who authorized it. The HCL ensures the human actually said yes.

# 7. Relationship to Active W3C Groups

This Position Paper is submitted to the W3C Web Machine Learning Community Group (WebML CG) as the home of WebMCP. The HCL complements WebMCP by providing the consent mechanism that WebMCP’s “human-in-the-loop” design principle requires but does not itself specify.

Four additional W3C groups are working on adjacent problems. This section maps the HCL’s relationship to each:

**AI Agent Protocol CG.** Develops protocols for agent discovery, identity, and collaboration. The HCL’s CARD credential schema and consent records are transportable over any agent protocol this group standardizes. The HCL does not compete with agent communication protocols—it rides on top of them.

**Agentic Integrity Verification Specification (AIVS) CG.** Explores open formats for cryptographic proof of AI agent sessions. The HCL’s SHA-256 hash chain audit trail is a candidate implementation of AIVS-conformant session proof. The ATL reference implementation demonstrates exactly the kind of tamper-evident action-level recording AIVS aims to standardize.

**Agent-to-Web Framework (A2WF) CG.** Develops machine-readable governance policies for AI agents, including human-in-the-loop verification. CARDs are a concrete implementation of the governance metadata A2WF envisions—translating machine requirements into human-comprehensible context at the point of action.

**AI Judgement Event (AIJE) CG.** Investigates cryptographically verifiable AI judgments portable across platforms. The HCL’s consent decision records (Allow/Block with cryptographic chain) are precisely “judgement events” in AIJE’s framing—human judgments about agent actions.

# 8. Normative Requirements

**MUST:** Provide a machine-readable trust signal (Shield) visible to the human at all times during agent operation.

**MUST:** Implement a consent mechanism (consent card) that presents CARD context and holds agent action pending human decision (Allow/Deny).

**MUST:** Maintain a tamper-evident audit log recording every consent decision with cryptographic chain integrity.

**MUST:** Implement fail-closed behavior: timeout or system failure results in Deny, not Allow.

**MUST:** Display the conformance level (Green/Yellow/Red Shield) honestly to the human.

**SHOULD:** Implement Consent Before Execution (Green Shield) where the platform provides pre-execution hooks.

**SHOULD:** Provide a Verification Endpoint (VE) integration for Trust Network enrollment and third-party verification.

**MAY:** Implement adaptive enforcement that automatically selects the strongest available consent level per platform.

**MAY:** Integrate with agentic payment frameworks to extend consent enforcement to financial transactions.

**MAY:** Implement delegation_vrcs in the CARD credential schema for interoperability with DTG Verifiable Relationship Credentials.

# 9. Reference Implementation

CROCbox serves as the HCL reference implementation, demonstrating both conformance levels on a production agent platform (OpenClaw). As of April 2026, Green Shield (Consent Before Execution) is fully operational. The user sees every tool call—process, read, exec, write—before it executes. Each action is presented with CARD context and an Allow/Block decision. Nothing executes without explicit human consent.

The ATL DevKit, published as @opnli/atl-devkit v0.1.0 on npm, extracts the consent engine from CROCbox into a standalone module any developer can adopt. Three lines of code to add consent enforcement to any agent.

| **Asset**              | **Details**                                                               |
|------------------------|---------------------------------------------------------------------------|
| npm package            | @opnli/atl-devkit@0.1.0 — Apache 2.0 — zero dependencies — 6.9 kB         |
| GitHub repository      | github.com/mikeoz/human-consent-layer — PUBLIC                            |
| CARD credential schema | schema/card-credential.schema.json v0.1.0 — includes delegation_vrcs hook |
| Install command        | npm install @opnli/atl-devkit                                             |

# 10. Open Design Questions

The following questions are offered for W3C community engagement. Each is mapped to the most relevant W3C group:

**DTG Interoperability (AI Agent Protocol CG):** Should Entity CARDs be expressed as W3C Verifiable Credentials bound to agent DIDs? What credential schema alignment is required with the DTG Credentials Task Force?

**Audit Trail Standardization (AIVS CG):** Should the HCL’s SHA-256 audit chain conform to an AIVS-specified session proof format? What interoperability is required between HCL decision records and AIVS session proofs?

**Governance Policy Integration (A2WF CG):** How should CARDs relate to A2WF’s machine-readable governance policies? Should CARDs be publishable as A2WF governance metadata?

**Proof of Personhood (AI Agent Protocol CG):** How should HCL consent mechanisms authenticate that the human is a real human? Should the CARD credential schema support PHC references?

**WebMCP Trust Extension (WebML CG):** Should the W3C define a WebMCP trust extension, or should the HCL remain a complementary layer with its own specification?

**Informed Consent Metrics:** How should the community measure whether CARD context achieves “informed” consent? What usability testing frameworks should apply?

**Sub-Agent Delegation:** When a primary agent spawns sub-agents, how does Use CARD scope propagate? The DTG’s VRC delegation chain model may inform scope-narrowing enforcement.

# 11. Ecosystem Benefits

**For Agent Developers:** npm install @opnli/atl-devkit. Three lines to trust. Retrofit existing agents. CARDs make your agent’s actions legible to the human. The HCL makes their decision enforceable.

**For Platform Operators:** Risk management through human oversight. Visible trust indicators increase adoption. Audit trails support compliance requirements.

**For End Users:** Real control—Allow/Block decisions are machine-enforced. Transparency—CARDs translate machine requirements into context you can understand. Portability—CARDs work across any HCL-compliant platform.

**For the Identity/SSI Community:** The HCL completes the DTG stack. Entity CARDs with delegation_vrcs bridge per-action consent to decentralized trust governance.

**For Standards Bodies:** Interoperability across platforms. Innovation enablement through trust infrastructure. Clear coordination surface with five active W3C groups.

# 12. Community and Governance

**Open Standard Commitment:** Apache 2.0 License. W3C Community Group participation. No vendor lock-in. Multiple implementations encouraged.

**Standards Coordination:** W3C WebML CG (primary submission). AI Agent Protocol CG (agent identity). AIVS CG (audit standardization). A2WF CG (governance policies). AIJE CG (judgement events). ToIP/DIF DTGWG (liaison).

# 13. An Invitation to Design Partnership

OpenlyTrusted is not building this consent layer in isolation, and we are not building it in secret. CROCbox Green Shield is operational. Both consent levels are shipping. The Trust Network is live. The ATL DevKit is on npm. The CARD credential schema is on GitHub. The Human Consent Layer is named, defined, and shipping.

We are sharing this architecture at the point where working code meets open standard.

We are seeking design partners who share three commitments: that agent trust is infrastructure, not a feature; that the human principal is always the authorizing party; and that auditability is a structural property, not a logging afterthought.

The W3C is the right forum for ensuring these layers interoperate under an open standard.

Technical contact: [mikeoz@opn.li](mailto:mikeoz@opn.li)

Reference implementation: [github.com/mikeoz/human-consent-layer](https://github.com/mikeoz/human-consent-layer)

DevKit: npm install @opnli/atl-devkit

*Everyone else protects systems FROM agents.*

**We protect the human’s AUTHORITY OVER agents.**

*MCP standardized the connection. The HCL standardizes the consent.*

*My data + Your AI + My control = Living Intelligence*
