# Contributing to Recovery Loop

Thank you for your interest in contributing to the Recovery Loop open protocol. This project aims to standardize post-surgical rehabilitation protocols in a machine-readable, multilingual, and clinically reviewed format.

---

## How to Submit a New Protocol

1. **Fork** this repository and create a branch named `protocol/<procedure>-v1` (e.g., `protocol/tha-standard-v1`).

2. **Create the protocol file** in `protocols/` following the naming convention:
   ```
   protocols/<procedure>-<variant>-v<version>.json
   ```
   Example: `protocols/tha-standard-v1.json`

3. **Follow the schema**. Validate your file against `schema/protocol.schema.json`. Every protocol file must:
   - Include the `_disclaimer` field.
   - Define all phases with `name` in at least `en` and `zh`.
   - Specify `advancementCriteria` for every phase.
   - Use `exerciseId` references from the exercise library (or propose new exercise IDs).

4. **Include advancement criteria** and, if applicable, **restrictions** for each phase.

5. **Open a Pull Request** with the title format: `Add protocol: <Procedure> <Variant> v<Version>`.

---

## How to Add Translations

Translations are welcome for all content types:

### Protocol Translations
- Protocol files support `en`, `zh`, `vi`, `id`, and `es` in the `name` and `goals` fields.
- To add a translation, edit the existing protocol JSON and add your locale strings.

### SOAP Snippet Translations
- Create a new file in `soap-snippets/orthopedic/<locale>.json` (e.g., `ja.json`, `ko.json`, `es.json`).
- Use the same keys as `en.json` and provide translated values.

### Translation PRs
- Title format: `Add <locale> translation for <content-type>`
- Example: `Add ja translation for SOAP snippets`
- One language per PR to simplify review.

---

## Review Process

All contributions go through a two-stage review:

### Stage 1: Clinical Reviewer
A clinician (physician, physical therapist, or other qualified healthcare professional) reviews:
- Clinical accuracy of the content
- Appropriateness of advancement criteria values
- Correctness of medication dosages and routes (for pain combos)
- Completeness of red flags and restrictions

Clinical reviewers are identified by the `clinical-reviewer` label on their GitHub profile or by prior contributions to this repository.

### Stage 2: Maintainer
A project maintainer reviews:
- JSON schema compliance
- File naming conventions
- Proper `_disclaimer` field inclusion
- Code style and formatting
- No inclusion of patient-identifiable information

Both approvals are required before merge.

---

## Authorship Policy

Contributors are credited in two ways:

1. **In-file attribution**: Your name (or handle) is added to the file's metadata when applicable.
2. **CONTRIBUTORS.md**: All contributors are listed in the project's `CONTRIBUTORS.md` file with their role (clinician, translator, developer, reviewer).

To be added, include your preferred name and role in your PR description.

---

## Schema Validation Requirements

Before submitting a PR, validate your JSON files:

### Protocol files
```bash
# Using ajv-cli (install: npm install -g ajv-cli)
ajv validate -s schema/protocol.schema.json -d protocols/your-protocol.json
```

### Manual checklist
- [ ] Valid JSON (no trailing commas, proper quoting)
- [ ] `_disclaimer` field present
- [ ] All required fields per schema are populated
- [ ] Exercise IDs use `ex-` prefix convention
- [ ] Phase numbers are sequential starting from 0
- [ ] `startWeek` and `endWeek` are consistent across phases (no gaps, no overlaps)

---

## Medical Disclaimer Requirement

**Every JSON file containing clinical content must include the `_disclaimer` field:**

```json
{
  "_disclaimer": "Reference framework only. Not medical advice."
}
```

For markdown files, include the following at the top:

```markdown
> DISCLAIMER: This content is provided as a reference framework for clinical education
> and software development. It does NOT constitute medical advice.
```

PRs missing the disclaimer will not be merged.

---

## Code of Conduct

- Be respectful and constructive in reviews.
- Clinical disagreements should cite evidence (guidelines, literature) rather than appeal to authority.
- Never include patient-identifiable information in any file.
- When in doubt about a clinical value, mark it with a `TODO` comment and flag it for clinical review.

---

## Questions?

Open an issue with the `question` label, or reach out to the maintainers.
