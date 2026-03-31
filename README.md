# Recovery Loop — Open Rehabilitation Protocol

> DISCLAIMER: This content is provided as a reference framework for clinical education and software development. It does NOT constitute medical advice. Actual clinical decisions must be made by qualified healthcare professionals based on individual patient assessment. The authors and contributors assume no liability for clinical outcomes resulting from the use of this content.

---

**Recovery Loop** (康復飛輪) is an open protocol for post-surgical rehabilitation, defining the continuous cycle of:

**Evaluate → Prescribe → Exercise → Re-evaluate**

This repository provides the clinical protocol definitions, assessment criteria, pain management presets, and SOAP templates that any healthcare system, app, or clinic can use to implement structured post-operative rehabilitation.

## What is the Recovery Loop?

```
┌─────────────┐
│  Evaluate    │ ← Assess ROM, VAS, function, PROM
│             │
└──────┬──────┘
       ▼
┌─────────────┐
│  Prescribe   │ ← Create exercise Rx based on phase + assessment
│             │
└──────┬──────┘
       ▼
┌─────────────┐
│  Exercise    │ ← Patient performs exercises, logs completion
│             │
└──────┬──────┘
       ▼
┌─────────────┐
│ Re-evaluate  │ ← Assess again → adjust Rx → repeat
│             │
└──────┬──────┘
       │
       └────────→ back to Evaluate (continuous loop)
```

The loop runs continuously from post-op day 1 through discharge and beyond. Each iteration generates data for the next clinical decision. Override (deviation from protocol) is expected and tracked — it represents clinical judgment.

## What's in this repo

| Directory | Contents |
|-----------|----------|
| [`loop/`](loop/) | The Recovery Loop definition (plain language) |
| [`protocols/`](protocols/) | Phase-based rehab protocols by procedure (TKA, THA, ACLR...) |
| [`assessment/`](assessment/) | Advancement criteria + red flags per phase |
| [`pain-combos/`](pain-combos/) | Anesthesia nerve block combo presets by surgery type |
| [`soap-snippets/`](soap-snippets/) | SOAP note quick-text templates (5 languages) |
| [`schema/`](schema/) | JSON Schema for validation |
| [`examples/`](examples/) | Sample protocol files |

## Quick Start

**For clinicians**: Read [`loop/recovery-loop.md`](loop/recovery-loop.md) to understand the workflow. Browse [`protocols/`](protocols/) for your procedure.

**For developers**: Use the JSON schemas in [`schema/`](schema/) to build compatible systems. All protocol files are machine-readable JSON.

**For contributors**: See [CONTRIBUTING.md](CONTRIBUTING.md) for how to submit new protocols, translations, or corrections.

## Supported Procedures

| Procedure | Protocol | Pain Combo |
|-----------|----------|------------|
| TKA (Total Knee Arthroplasty) | 5-phase, Week 0-52 | Femoral + ACB + iPACK |
| THA (Total Hip Arthroplasty) | 5-phase | Fascia Iliaca + LFCN |
| ACLR (ACL Reconstruction) | 5-phase | ACB + AFCN + iPACK |
| RCR (Rotator Cuff Repair) | Protocol pending | Supraclavicular + Serratus Anterior |
| ORIF (Fracture Fixation) | Protocol pending | Per fracture type |

## Languages

SOAP snippets are available in: 繁體中文, English, 日本語, 한국어, Español

## Related Projects

| Project | Description |
|---------|-------------|
| [open-rehab-exercises](https://github.com/open-rehab/open-rehab-exercises) | 76 exercise definitions × 7 languages (coming soon) |
| [open-prom-scoring](https://github.com/open-rehab/open-prom-scoring) | PROM instrument scoring logic (coming soon) |
| [rehab-data-schema](https://github.com/open-rehab/rehab-data-schema) | Data interchange JSON schemas (coming soon) |

## License

Clinical content (protocols, pain combos, SOAP snippets): **CC BY 4.0** — use freely, attribution required.

Code and schemas: **MIT** — no restrictions.

## Maintainer

Maintained by [De Novo Orthopedics](https://denovortho.com) (谷盺生物科技).

The Recovery Loop protocol is designed to be system-agnostic. You do not need to use any specific software to implement it.

---

*This repository is intentionally versioned and structured to support future conformance and certification workflows.*
