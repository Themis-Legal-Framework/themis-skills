---
name: pleadings-core
description: Draft or revise civil pleadings (complaints, answers, counterclaims, amended pleadings) using element mapping, allegation planning, and numbered-paragraph drafting with a pleading-risk QC pass.
metadata:
  short-description: Pleadings workflow + risk controls
---

# Pleadings Core

## Purpose
Provide a consistent workflow for pleadings that is adaptable to any jurisdiction via overlays.

## What this skill produces
- Element map + allegation coverage plan
- Draft pleading in numbered paragraphs
- "Missing facts" question list
- Pleading-risk QC report

## Input checklist
Ask for:
1) Pleading type: complaint / answer / counterclaim / amended pleading / other
2) Parties and capacities (individual/entity; roles)
3) Forum (if known): jurisdiction + venue + court level
4) Causes of action / defenses to include (list)
5) Remedies sought (damages types, equitable relief, fees, punitive, etc.)
6) Fact packet (chronology + documents + key communications)
7) Known weak points (limitations, notice, immunity, standing, contract terms, etc.)
8) Any required exhibits or referenced documents (contracts, policies, notices)
9) Style constraints (tone, length, level of detail)

## Core workflow
### Step 1 — Element mapping
- Build (or request) an **element checklist** for each claim/defense.
- If authority is not provided, use placeholders: `[ADD ELEMENTS: jurisdiction-specific]`.
- Then build an **allegation coverage table**: element → paragraph(s) → supporting facts → missing facts.

(Invoke `claims-and-elements-builder` if useful.)

### Step 2 — Allegation planning
- Draft a section-by-section plan:
  - Parties
  - Jurisdiction/venue (placeholders if unknown)
  - General allegations (chronology)
  - Claim/defense counts
  - Damages/remedies/prayer
- Flag where heightened pleading may apply (as a **jurisdiction-dependent** placeholder): `[CHECK HEIGHTENED PLEADING STANDARD]`.

### Step 3 — Drafting rules
- Use numbered paragraphs.
- Define actors consistently (full names first, then defined terms).
- Prefer **facts over conclusions**; where legal conclusions are necessary, keep them tight and tied to facts.
- Avoid unnecessary admissions and avoid overstating certainty.

### Step 4 — QC pass (pleading-focused)
Provide a report with:
- Missing elements / thin elements
- Timeline gaps and identity gaps (who/what/when/where)
- Contradictions (dates, actors, amounts, sequences)
- Remedy alignment (facts support requested relief)
- Defensive risks (limitations, standing, preemption, immunity, exhaustion/notice)
- Exhibit/attachment risks (incorporation by reference; authenticity; unintended admissions)

## Jurisdiction customization
If jurisdiction is known (or user provides a pack), invoke `overlay-jurisdiction-pleadings` to apply:
- caption blocks / filing components
- required verifications / signatures / civil cover sheets
- pleading standard nuances and required allegations
