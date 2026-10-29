# Open Consent

**Make human consent the default for every AI agent interaction.**

Open Consent is an umbrella project by [Opnli Corporation](https://opn.li) that open-sources the [Human Consent Layer](https://github.com/mikeoz/human-consent-layer) — the trust infrastructure that gives humans real-time, machine-enforced control over what AI agents do with their data.

The project has one goal: when the market asks "how do I trust agents?" — the Human Consent Layer is the answer.

*My data + Your AI + My control = Living Intelligence*

---

## Start here

- **Watch it:** [Green Shield Payments in 45 seconds](https://youtu.be/UKdwVPk2Agw) · [Why agents need the Green Shield, in 70 seconds](https://youtu.be/kE1Hu4gRCu0)
- **Read the standard:** the [HCL Specification](https://github.com/mikeoz/human-consent-layer/blob/main/SPEC.md)
- **Add it to your tool:** a Green Shield quickstart, "Add the Green Shield to your MCP tool", is in preparation.

---

## The Three Tiers

```text
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│ Tier 1 — The Standard (Open)                                │
│ The HCL specification, CARD schemas, and developer tools.   │
│ Apache 2.0. Anyone can implement it.                        │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Tier 2 — Starting-Point Products (Open)                     │
│ Reference implementations designed to fork back into        │
│ the major open-source AI projects. Apache 2.0.              │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Tier 3 — The Openly Trusted Network (Proprietary)           │
│ Green Shield protections: the consent card, each            │
│ member's chain, and signed proofs others verify.            │
│ Operated by Opnli Corporation.                              │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```


Open the standard. Release the products. Keep the network. Let the community carry the consent layer into every agent.

---

## The Repos

### Tier 1 — The Standard

| Repo | What It Is | Status |
|------|-----------|--------|
| [human-consent-layer](https://github.com/mikeoz/human-consent-layer) | The HCL specification, CARD schemas (Entity, Data, Use, Boundary), and the ATL DevKit (runs locally; not yet connected to the network). The normative definition of what human consent means in the agent context. | Live |
| [hcl-devkit](https://github.com/mikeoz/hcl-devkit) | Developer tools: Verification Endpoint client, SHA-256 audit chain library, CARD schema validators. For developers building HCL-conformant agents and platforms. | Quick start out of date (see its note) |

### Tier 2 — Starting-Point Products

| Repo | What It Is | Fork-Back Target | Status |
|------|-----------|------------------|--------|
| [webmcp-hcl](https://github.com/mikeoz/webmcp-hcl) | Adds HCL consent gates to WebMCP tool registrations. The highest-leverage bridge: WebMCP standardizes tool discovery, the HCL standardizes consent. | WebMCP / W3C Web Machine Learning CG | Live |
| [crocbox](https://github.com/mikeoz/crocbox) | The reference HCL implementation for OpenClaw agents. Desktop app wrapping OpenClaw with Green Shield consent, tamper-evident audit, and Openly Trusted Network integration. | OpenClaw | Audit in progress |
| [mydatabkt](https://github.com/mikeoz/mydatabkt) | Consent-gated personal data bucket. Your data stays on your machine. Read and write gated by the HCL consent chain with signed proofs. | Local-first AI / AnythingLLM | Live |

### Tier 3 — The Openly Trusted Network (OTN)

The Openly Trusted Network (OTN) is the network Opnli Corporation operates. It provides Green Shield protections for HCL-compliant trust transactions: the Green Shield card where a member decides, each member's tamper-evident chain of decisions, and signed consent proofs that websites and banks verify for themselves. The network Opnli operates is proprietary. It is the Visa/Mastercard layer: the standard is open; the operating network that certifies compliance and carries trusted transactions is the service provided by Opnli.

[opn.li](https://opn.li) — The Openly Trusted Network
[openlytrusted.ai](https://openlytrusted.ai) — Give trust a try

---

## Why Open Consent Exists

The Agent Economy is arriving. AI agents read files, execute commands, access APIs, send messages, and make decisions on behalf of humans. The industry has built sandbox isolation (NVIDIA NemoClaw), deployment scoping (AWS), design constraints (Meta Rule of Two), and tool discovery (WebMCP). Nobody has built the consent layer — the part where the human says yes or no, understands what they are agreeing to, and can verify the record later.

The Human Consent Layer fills that gap. Open Consent makes it available to everyone.

The strategic model is Let's Encrypt for agent consent: make the standard free and ubiquitous, while Opnli operates the Openly Trusted Network that certifies compliance. The starting-point products are designed as fork-backs — each one flows back into its parent open-source community, carrying the HCL with it:

- **WebMCP sites add HCL consent annotations** → the W3C WebMCP draft gets human consent.
- **OpenClaw adopts CROCbox's consent gate** → every OpenClaw agent gets the Green Shield.
- **Local-first AI tools adopt MyDataBkt's consent model** → personal data stays under human control.

Each fork-back creates a new constituency for the HCL standard and new participants on the Openly Trusted Network.

---

## The Core Idea in Four Sentences

Only a human can give consent. Consent requires context. CARDs provide context. The Human Consent Layer enforces the decision.

---

## Learn More

- [HCL Specification](https://github.com/mikeoz/human-consent-layer/blob/main/SPEC.md) — The normative spec: four-link consent chain, CARD model, Shield conformance levels, five invariants.
- [CARD Schemas](https://github.com/mikeoz/human-consent-layer/tree/main/schema) — JSON Schema definitions for CARD credentials and CARD Sets.
- [WebMCP + HCL Demo](https://github.com/mikeoz/webmcp-hcl/tree/main/demo) — Working demo of HCL consent gating on WebMCP tool calls.
- [W3C Position Paper](w3c-position-paper.md) — The Human Consent Layer as a proposed standard (version 4.0, April 2026, with its submission history).

---

## License

All Tier 1 and Tier 2 repos are Apache 2.0.

Certain enforcement mechanisms implemented in products built on the HCL specification are the subject of Provisional Patent Application #63/992,579 filed February 27, 2026. The HCL specification, schemas, and developer tools are open and freely implementable under the Apache 2.0 license.

---

*Only a human can give consent. Consent requires context. CARDs provide context. The Human Consent Layer enforces the decision.*

*— Open Consent, October 2026. Opnli Corporation.*
