---
name: claims-and-elements-builder
description: Convert a list of claims/defenses into an element checklist and an allegation coverage table (element→paragraph plan→missing facts), using placeholders where jurisdiction-specific law is required.
metadata:
  short-description: Element mapping + coverage table generator
---

# Claims and Elements Builder

## Purpose
Create a structured element map and "coverage table" that can drive a pleading or help attack one.

## Inputs
Ask for:
- Claim/defense list (and any available authority the user trusts)
- Jurisdiction/venue (optional)
- Key facts (bullets are fine)
- Any known "must plead" items (notice, demand, conditions precedent, damages)

## Output format (always)
For each claim/defense:
1) **Elements** (jurisdiction-specific if supplied; otherwise placeholders)
2) **What we can allege now** (facts already provided)
3) **What we must confirm** (missing facts)
4) **Allegation plan**: where each element will be pleaded (section + paragraph range)
5) **Risk flags**: likely attack points (limitations, standing, causation, reliance, etc.)

## Rules
- Do not invent legal elements. If not provided, output:
  - `[ADD ELEMENTS: jurisdiction-specific]`
  - plus a list of the facts you would need to satisfy typical versions of the claim.
- Separate **ultimate facts** from **evidence** (exhibits, quotations) and identify where exhibits may help.

## Optional: pleading attack mode
If user asks to evaluate an opponent pleading, output:
- "Missing element" checklist
- Ambiguity list (who/what/when/how)
- Contradiction list
- Remedy/prayer mismatch list
