---
name: overlay-jurisdiction-pleadings
description: Apply jurisdiction/venue-specific pleading requirements (caption blocks, required sections, terminology, verifications, formatting, and pleading standards) to an existing pleading draft using a user-provided jurisdiction pack.
metadata:
  short-description: Jurisdiction customization layer for pleadings
---

# Overlay: Jurisdiction Pleadings

## Purpose
Convert a jurisdiction-agnostic pleading draft into a jurisdiction-compliant draft **based on user-supplied rules/templates**.

## Inputs
- Draft pleading text (required)
- Jurisdiction/venue (required)
- Local requirements (preferred via Jurisdiction Pack; otherwise user-provided notes)

## How to use a Jurisdiction Pack
If a Jurisdiction Pack is present (recommended), it should include:
- caption template(s)
- required sections (civil cover, verification, signature blocks)
- pleading standards and heightened pleading rules
- terminology differences (e.g., "statement of claim" vs "complaint")
- formatting defaults (fonts/margins/page limits if applicable)
- filing/service quirks (if any)

If no pack is available, ask the user to provide:
- caption example
- required sections checklist
- any heightened pleading requirements
- formatting constraints

## Output
1) Revised pleading with:
   - jurisdiction-compliant caption/format
   - required sections inserted
   - terminology normalized
2) Compliance checklist (jurisdiction-specific)
3) "Open questions" list for any missing local requirements

## Rules
- Do not guess local rules. If unknown, bracket: `[LOCAL RULE REQUIRED]`.
- Prefer minimal edits: change only what is necessary for compliance and clarity.
