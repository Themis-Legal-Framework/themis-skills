---
name: claims-and-elements-builder
description: Convert a list of claims/defenses into an element checklist and an allegation coverage table (element→paragraph plan→missing facts), using placeholders where jurisdiction-specific law is required.
metadata:
  short-description: Element mapping + coverage table generator
---

# Claims and Elements Builder

## Purpose
Create structured element maps that drive pleading drafts or expose weaknesses in opposing pleadings.

---

## CRITICAL CONSTRAINTS

### Never Invent Elements
- If jurisdiction-specific elements are not provided, output:
  ```
  [ADD ELEMENTS: {claim type} under {jurisdiction} law]
  ```
- Provide **typical element structure** as guidance, clearly labeled as generic

### Always Distinguish
- **Ultimate facts** (what must be pleaded)
- **Evidence** (what proves the ultimate facts)
- **Legal conclusions** (labels that require factual support)

---

## Input Collection

| Input | Required? | Purpose |
|-------|-----------|---------|
| Claim/defense list | YES | What to map |
| Jurisdiction | Preferred | Determines elements |
| Authority provided | Preferred | User-trusted sources for elements |
| Key facts | YES | What we can allege |
| "Must plead" items | Preferred | Notice, demand, conditions precedent |

---

## Output Format

### For Each Claim/Defense

```
══════════════════════════════════════════════════════════
CLAIM: [Name of Cause of Action]
══════════════════════════════════════════════════════════

AUTHORITY: [Citation provided by user]
          OR: [ADD ELEMENTS: jurisdiction-specific]

ELEMENTS:
┌─────┬────────────────────────────────┬─────────────────┐
│ #   │ Element                        │ Pleading Type   │
├─────┼────────────────────────────────┼─────────────────┤
│ 1   │ [Element description]          │ Ultimate fact   │
│ 2   │ [Element description]          │ Ultimate fact   │
│ 3   │ [Element description]          │ Conclusion OK   │
└─────┴────────────────────────────────┴─────────────────┘

COVERAGE TABLE:
┌─────────┬──────────────────┬──────────────────┬──────────────────┬─────────┐
│ Element │ What We Allege   │ Supporting Facts │ Missing Facts    │ Risk    │
├─────────┼──────────────────┼──────────────────┼──────────────────┼─────────┤
│ 1       │ [Allegation]     │ [Fact from user] │ —                │ Low     │
│ 2       │ [Allegation]     │ [Fact from user] │ [Specific Q]     │ Medium  │
│ 3       │ [Allegation]     │ —                │ [Specific Q]     │ HIGH    │
└─────────┴──────────────────┴──────────────────┴──────────────────┴─────────┘

ALLEGATION PLAN:
┌─────────┬─────────────────────┬────────────────┐
│ Element │ Section             │ Paragraph Plan │
├─────────┼─────────────────────┼────────────────┤
│ 1       │ General Allegations │ ¶¶ 10-12       │
│ 2       │ First Cause         │ ¶¶ 25-27       │
│ 3       │ First Cause         │ ¶¶ 28-30       │
└─────────┴─────────────────────┴────────────────┘

RISK FLAGS:
• [Risk 1]: [Description] — [Mitigation suggestion]
• [Risk 2]: [Description] — [Mitigation suggestion]

EXHIBIT OPPORTUNITIES:
• [Document]: Supports Element [#] — [Attach/Reference recommendation]
```

---

## Example Output

```
══════════════════════════════════════════════════════════
CLAIM: Breach of Contract
══════════════════════════════════════════════════════════

AUTHORITY: [ADD ELEMENTS: breach of contract under California law]

TYPICAL ELEMENTS (generic — confirm for jurisdiction):
┌─────┬────────────────────────────────┬─────────────────┐
│ #   │ Element                        │ Pleading Type   │
├─────┼────────────────────────────────┼─────────────────┤
│ 1   │ Existence of contract          │ Ultimate fact   │
│ 2   │ Plaintiff's performance        │ Ultimate fact   │
│ 3   │ Defendant's breach             │ Ultimate fact   │
│ 4   │ Resulting damages              │ Ultimate fact   │
└─────┴────────────────────────────────┴─────────────────┘

COVERAGE TABLE:
┌─────────┬──────────────────────────┬──────────────────────────┬────────────────────────┬─────────┐
│ Element │ What We Allege           │ Supporting Facts         │ Missing Facts          │ Risk    │
├─────────┼──────────────────────────┼──────────────────────────┼────────────────────────┼─────────┤
│ 1       │ Written agreement 1/1/24 │ Signed contract Ex. A    │ —                      │ Low     │
│ 2       │ Delivered goods per spec │ Invoices, delivery logs  │ [Who signed for goods?]│ Medium  │
│ 3       │ Failed to pay by 2/1/24  │ Due date in contract     │ [Any partial payment?] │ Low     │
│ 4       │ $50,000 in damages       │ Invoice amount           │ [Interest rate?]       │ Medium  │
└─────────┴──────────────────────────┴──────────────────────────┴────────────────────────┴─────────┘

ALLEGATION PLAN:
┌─────────┬─────────────────────┬────────────────┐
│ Element │ Section             │ Paragraph Plan │
├─────────┼─────────────────────┼────────────────┤
│ 1       │ General Allegations │ ¶¶ 8-10        │
│ 2       │ General Allegations │ ¶¶ 11-14       │
│ 3       │ Breach Count        │ ¶¶ 20-22       │
│ 4       │ Damages             │ ¶¶ 25-27       │
└─────────┴─────────────────────┴────────────────┘

RISK FLAGS:
• Statute of limitations: Contract dated 1/1/24, breach 2/1/24 — confirm SOL for jurisdiction
• Conditions precedent: [CHECK: does contract require notice before suit?]
• Damages certainty: Lost profits may require heightened pleading

EXHIBIT OPPORTUNITIES:
• Contract (Ex. A): Supports Elements 1, 2, 3 — ATTACH (central document)
• Invoices: Support Element 4 — Reference only (voluminous)
• Delivery logs: Support Element 2 — ATTACH (authenticates performance)
```

---

## Pleading Attack Mode

When analyzing an **opponent's pleading**, output:

### Missing Element Checklist
```
| Claim | Element | Alleged? | Paragraphs | Assessment |
|-------|---------|----------|------------|------------|
| Fraud | Misrepresentation | Yes | ¶¶ 15-16 | Conclusory |
| Fraud | Scienter | NO | — | MISSING — MTD target |
| Fraud | Reliance | Weak | ¶ 18 | No facts re: actual reliance |
```

### Ambiguity List
```
| Issue | Paragraph | Problem |
|-------|-----------|---------|
| WHO made the statement | ¶ 15 | "Defendants" — which one? |
| WHEN did reliance occur | ¶ 18 | No date alleged |
| WHAT was the statement | ¶ 15 | Paraphrase, not actual words |
```

### Contradiction List
```
| Contradiction | Paragraphs | Issue |
|---------------|------------|-------|
| Contract date | ¶ 8 vs ¶ 12 | Says 1/1/24 and 1/15/24 |
| Knowledge timing | ¶ 20 vs ¶ 25 | Knew before told? |
```

### Remedy/Prayer Mismatch
```
| Remedy Sought | Factual Support | Gap |
|---------------|-----------------|-----|
| Lost profits | None alleged | No causation to lost business |
| Punitive | "Malice" conclusory | No facts showing malice |
```

---

## Output Checklist

- [ ] Every claim/defense has element table
- [ ] Coverage table shows facts vs. gaps
- [ ] Allegation plan maps to paragraph ranges
- [ ] Risk flags identify attack points
- [ ] Exhibit opportunities noted
- [ ] No elements invented (placeholders used)
