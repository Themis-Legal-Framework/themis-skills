---
name: pleading-qc-and-risk-audit
description: Audit a pleading for missing elements, contradictions, unclear actors/timing, remedy mismatch, and common attack points (limitations, standing, notice), producing a prioritized fix list and client questions.
metadata:
  short-description: Pleading QC + attack surface analysis
---

# Pleading QC and Risk Audit

## Inputs
- Draft pleading text
- Claim/defense list (if not obvious)
- Any known jurisdiction/venue requirements (optional)
- User risk tolerance (conservative vs aggressive)

## Outputs (always)
1) **Top 10 fixes** (ranked by impact)
2) **Element coverage gaps** (by claim/defense)
3) **Contradictions & ambiguities** (paragraph citations)
4) **Attack points** (limitations/standing/notice/causation/reliance/etc.) as placeholders if jurisdiction-specific
5) **Client questions** (specific, answerable)
6) **Rewrite instructions** (by section)

## Audit checklist
- Parties/capacities consistent?
- Timeline coherent?
- Who/what/when/where/how stated for key events?
- Causation/damages traced to conduct?
- Remedies supported by facts?
- Any "bad facts" addressed/contained?
- Overpleading: unnecessary admissions or locked-in theories?
- Underpleading: missing specifics that make the claim implausible?

## Rules
- Don't invent missing facts; propose targeted questions.
- Where legal standards vary, mark: `[CHECK STANDARD: jurisdiction-specific]`.
