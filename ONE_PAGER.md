# Recovery Loop 康復飛輪 — One Pager

## What

An open protocol for post-surgical rehabilitation. Four steps, continuous loop:

**Evaluate → Prescribe → Exercise → Re-evaluate**

## Why

Post-surgical rehab outcomes depend on consistent, structured follow-up. But most clinics run rehab as ad-hoc visits without a shared framework. Recovery Loop provides the shared clinical language so that surgeons, PTs, and patients are on the same page.

## What's Included

- **Protocol templates** — TKA 5-phase protocol with ROM targets, advancement criteria, exercise prescriptions
- **Pain management combos** — Nerve block presets for TKR, ACLR, RCR/TSA, Hip (per anesthesiologist feedback)
- **Assessment criteria** — When to advance, when to hold, red flags per phase
- **SOAP snippets** — 29 clinical quick-text templates in 2 languages (more coming)
- **JSON Schema** — Machine-readable, validated, interoperable

## What's NOT Included

- Software (this is a protocol, not an app)
- Patient data
- Automation or alerting
- PROM questionnaire text (requires separate license)

## Who Can Use It

Anyone. CC BY 4.0 — use freely, modify freely, just credit the source.

- **PT / Therapist**: Use the protocol as a clinical reference
- **Developer**: Build compatible systems using the JSON schema
- **Researcher**: Reference the protocol structure in studies
- **Hospital / Clinic**: Adopt as your rehab standard
- **Medtech company**: Integrate into your product (no share-alike restriction)

## How to Contribute

Submit a Pull Request on GitHub. New protocols, translations, corrections welcome. Every contributor gets named authorship. Clinical content reviewed by our Clinical Review Board.

## Numbers

| Metric | Count |
|--------|-------|
| Phases (TKA) | 5 |
| Exercise references | 46 per protocol |
| Pain combo presets | 5 surgery types |
| SOAP snippets | 29 × 2 languages |
| Languages (SOAP) | zh-TW, en (ja, ko, es coming) |

## License

Clinical content: **CC BY 4.0** (attribution required, no other restrictions)
Code/schema: **MIT** (no restrictions)

## Link

**github.com/cutemo0953/open-recovery-loop**

## Maintained by

De Novo Orthopedics 谷盺生物科技
denovortho.com

---

*Recovery Loop is system-agnostic. You don't need any specific software to use it. But if you want the full automated implementation — iRehab is free.*
