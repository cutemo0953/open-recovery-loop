# Advancement Criteria — TKA Standard Protocol

> DISCLAIMER: This content is provided as a reference framework for clinical education and software development. It does NOT constitute medical advice. Actual clinical decisions must be made by qualified healthcare professionals based on individual patient assessment.

---

## Overview

Each phase of the TKA rehabilitation protocol defines explicit **advancement criteria** that must be met before a patient progresses to the next phase. All phase transitions require a clinical decision by the treating physical therapist or physician (`ptDecisionRequired: true`).

Advancement is never automatic. Meeting the numeric thresholds is necessary but not sufficient — the clinician always has the final say.

---

## Phase 0 (Prehab) → Phase 1 (Acute)

| Criterion | Value |
|-----------|-------|
| Minimum weeks in phase | 0 (no minimum — phase ends at surgery) |
| ROM flexion target | N/A |
| ROM extension target | N/A |
| Pain max (VAS) | N/A |
| Effusion max | N/A |
| Functional gate | `surgery_scheduled` — surgery date confirmed |
| PT decision required | Yes |

**Narrative**: The patient transitions out of prehab when surgery is scheduled and performed. There is no minimum time requirement. The goal of this phase is to optimize baseline strength and ROM before the operation.

---

## Phase 1 (Acute) → Phase 2 (Subacute)

| Criterion | Value |
|-----------|-------|
| Minimum weeks in phase | 2 |
| ROM flexion | >= 90 degrees |
| ROM extension | 0 degrees (full extension) |
| Pain max (VAS) | <= 5/10 |
| Effusion max | Mild or less |
| Functional gate | `transfer_independently` — patient can transfer in/out of bed and chair without assistance |
| PT decision required | Yes |

**Narrative**: The acute phase focuses on pain and edema control, early mobilization, and weight bearing. To advance, the patient must demonstrate at least 90 degrees of flexion, full extension, manageable pain (VAS <= 5), no more than mild effusion, and the ability to transfer independently. At least 2 weeks must have elapsed since surgery.

---

## Phase 2 (Subacute) → Phase 3 (Strengthening)

| Criterion | Value |
|-----------|-------|
| Minimum weeks post-op | 6 |
| ROM flexion | >= 110 degrees |
| ROM extension | 0 degrees (full extension) |
| Pain max (VAS) | <= 3/10 |
| Effusion max | Trace or less |
| Functional gate | `walk_without_assistive_device` — patient ambulates without walker or cane |
| PT decision required | Yes |

**Narrative**: The subacute phase focuses on restoring ROM, normalizing gait, and weaning off assistive devices. Advancement requires at least 110 degrees of flexion, minimal pain (VAS <= 3), trace or no effusion, and the ability to walk without any assistive device. The patient must be at least 6 weeks post-op.

---

## Phase 3 (Strengthening) → Phase 4 (Return to Function)

| Criterion | Value |
|-----------|-------|
| Minimum weeks post-op | 12 |
| ROM flexion | >= 120 degrees |
| ROM extension | 0 degrees (full extension) |
| Pain max (VAS) | <= 2/10 |
| Effusion max | None |
| Functional gate | `stair_reciprocal` — patient can climb stairs with reciprocal pattern (step-over-step) |
| PT decision required | Yes |

**Narrative**: The strengthening phase focuses on functional strength, endurance, and return to daily activities. Advancement requires 120 degrees of flexion, near-pain-free status (VAS <= 2), no effusion, and the ability to climb stairs reciprocally. The patient must be at least 12 weeks post-op.

---

## Phase 4 (Return to Function) → Discharge / Maintenance

| Criterion | Value |
|-----------|-------|
| Minimum weeks post-op | 26 |
| ROM flexion | N/A (maintained) |
| ROM extension | N/A (maintained) |
| Pain max (VAS) | N/A |
| Effusion max | N/A |
| Functional gate | `maintenance` — patient is on a self-directed long-term maintenance program |
| PT decision required | Yes |

**Narrative**: The final phase focuses on maintaining strength and ROM, returning to recreational activities, and establishing long-term self-management. Transition to maintenance/discharge occurs at or after 26 weeks, at the clinician's discretion.

---

## Summary Table

| Transition | Min Weeks | ROM Flexion | Pain (VAS) | Effusion | Functional Gate |
|-----------|-----------|-------------|------------|----------|-----------------|
| Phase 0 → 1 | 0 | — | — | — | Surgery scheduled |
| Phase 1 → 2 | 2 | >= 90 | <= 5 | Mild | Transfer independently |
| Phase 2 → 3 | 6 | >= 110 | <= 3 | Trace | Walk without device |
| Phase 3 → 4 | 12 | >= 120 | <= 2 | None | Stair reciprocal |
| Phase 4 → Done | 26 | — | — | — | Maintenance |
