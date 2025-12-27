---
name: convert-facts-to-numbered-allegations
description: Turn a fact chronology into litigation-ready numbered allegations with defined actors, dates, and document references, minimizing legal conclusions and flagging missing details.
metadata:
  short-description: Fact packet → numbered paragraphs
---

# Convert Facts to Numbered Allegations

## Inputs
Ask for:
- Chronology or narrative (bullets ok)
- Parties list (names + roles)
- Key documents (titles/dates; excerpts if available)
- Amounts and dates (if damages matter)
- Any "do not include" items (privacy/strategy/privilege)

## Output
1) **Defined terms list** (Parties/Entities/Documents)
2) **Numbered allegations** (chronological unless user requests topical)
3) **Document reference map** (Doc → paragraph numbers)
4) **Missing details list** (specific questions)

## Drafting rules
- One paragraph = one idea.
- Anchor: actor + date (or approximate date) + act + consequence.
- Avoid conclusory legal labels unless requested; prefer the underlying conduct.
- If uncertain, bracket it: `[CONFIRM DATE]`, `[CONFIRM AMOUNT]`, `[CONFIRM IDENTITY]`.

## QC checks
- Consistent names/defined terms
- Date order coherence
- No "floating pronouns" (unclear who "they" refers to)
- Damages traceable to events (if relevant)
