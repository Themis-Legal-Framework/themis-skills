---
name: draft-answer-and-defenses
description: Draft an answer responding paragraph-by-paragraph with admissions/denials/insufficient knowledge, plus affirmative defenses and preservation language, and a risk audit for inadvertent admissions.
metadata:
  short-description: Answer + defenses with admission-risk controls
---

# Draft Answer and Defenses

## Inputs (must ask)
1) Complaint text (or a paste of allegations)
2) Client's position: what is true/false/unknown (high level is fine)
3) Known affirmative defenses (list; if unknown, ask for likely categories)
4) Counterclaim intent (yes/no; if yes, invoke counterclaim skill)
5) Jurisdiction/venue (optional, for overlay)
6) Any sensitive facts to avoid pleading (privacy/strategy/privilege)

## Output (always)
1) **Answer** (organized to match complaint sections/causes, if possible)
2) **Affirmative defenses** (labeled; jurisdiction placeholders if needed)
3) **Admission-risk audit** (what to confirm before filing)

## Drafting rules
- Respond to each numbered paragraph with:
  - Admit / Deny / Admit in part and deny in part / Lacks sufficient knowledge (as applicable)
- Keep denials precise; avoid denying indisputable background facts unnecessarily.
- Avoid pleading privileged content.
- For affirmative defenses:
  - plead as ultimate facts where possible
  - avoid legal conclusions without supporting factual context

## Affirmative defenses workflow
- If jurisdiction-specific defenses/standards are not provided:
  - list common defense categories as **placeholders**
  - ask user to select which apply and provide supporting facts

## Admission-risk audit (required)
Output a list of:
- Paragraph responses that depend on missing documents or client confirmation
- Any response that could be construed as an admission of duty, agency, contract formation, or notice
- Any defense that needs factual support (dates, notices, contract clauses)
- Inconsistencies (e.g., denying facts that the defenses rely on)

## Jurisdiction overlay
If needed, invoke `overlay-jurisdiction-pleadings` to:
- conform terminology (general denial availability, verification requirements, etc.)
- apply required formatting and caption conventions
