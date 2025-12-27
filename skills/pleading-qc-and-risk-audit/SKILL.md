---
name: pleading-qc-and-risk-audit
description: Audit a pleading for missing elements, contradictions, unclear actors/timing, remedy mismatch, and common attack points (limitations, standing, notice), producing a prioritized fix list and client questions.
metadata:
  short-description: Pleading QC + attack surface analysis
---

# Pleading QC and Risk Audit

## Purpose
Provide comprehensive quality control and vulnerability analysis for pleadings before filing, identifying weaknesses that opponents will exploit.

---

## CRITICAL CONSTRAINTS

### Never
- Invent facts to fill gaps (propose questions instead)
- Assume legal standards (mark as jurisdiction-dependent)
- Minimize risks (be direct about vulnerabilities)

### Always
- Prioritize fixes by impact
- Provide specific paragraph citations
- Generate actionable client questions
- Distinguish "must fix" from "should fix"

---

## Input Collection

| Input | Required? | Purpose |
|-------|-----------|---------|
| Draft pleading text | YES | What to audit |
| Claim/defense list | Preferred | Element coverage check |
| Jurisdiction | Preferred | Standard-specific analysis |
| Risk tolerance | Preferred | Conservative vs. aggressive |

---

## Audit Framework

### STEP 1 — Quick Scan (Red Flags)

**Immediate issues to identify**:
```
═══════════════════════════════════════════════════════════════
QUICK SCAN — RED FLAGS
═══════════════════════════════════════════════════════════════

CRITICAL ISSUES (blocks filing):
☐ Missing required section (parties, jurisdiction, prayer)
☐ No allegations for stated claim
☐ Wrong party named
☐ Obvious factual impossibility

SERIOUS ISSUES (invites immediate challenge):
☐ Statute of limitations on face
☐ Standing not alleged
☐ Jurisdiction not alleged
☐ Heightened pleading not met (fraud, etc.)

NOTABLE ISSUES (weakens pleading):
☐ Conclusory allegations without facts
☐ Timeline gaps or inconsistencies
☐ Vague party references
☐ Damages not tied to conduct
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Element Coverage Audit

**For each claim/defense**:
```
═══════════════════════════════════════════════════════════════
ELEMENT COVERAGE AUDIT
═══════════════════════════════════════════════════════════════

CLAIM: [Name]
ELEMENTS: [List or "ADD ELEMENTS: jurisdiction-specific"]

┌─────────┬────────────────────────────┬────────────┬────────────────────────┐
│ Element │ Description                │ Alleged?   │ Assessment             │
├─────────┼────────────────────────────┼────────────┼────────────────────────┤
│ 1       │ [Element]                  │ ¶¶ X-Y     │ ✓ Sufficient           │
│ 2       │ [Element]                  │ ¶ Z        │ ⚠ Thin — needs facts   │
│ 3       │ [Element]                  │ —          │ ✗ MISSING              │
│ 4       │ [Element]                  │ ¶ W        │ ✓ Sufficient           │
└─────────┴────────────────────────────┴────────────┴────────────────────────┘

GAPS TO CURE:
• Element 2: Add specific facts showing [what's needed]
• Element 3: MUST add allegations — currently fatal

[Repeat for each claim/defense]
═══════════════════════════════════════════════════════════════
```

---

### STEP 3 — Factual Integrity Audit

```
═══════════════════════════════════════════════════════════════
FACTUAL INTEGRITY AUDIT
═══════════════════════════════════════════════════════════════

1. TIMELINE COHERENCE
┌──────────────────────────┬────────────┬────────────────────────────────┐
│ Event                    │ Paragraph  │ Date Alleged                   │
├──────────────────────────┼────────────┼────────────────────────────────┤
│ Contract signed          │ ¶ 8        │ January 1, 2024                │
│ Performance began        │ ¶ 12       │ January 15, 2024               │
│ Breach occurred          │ ¶ 16       │ March 1, 2024                  │
│ Discovery of breach      │ ¶ 18       │ February 15, 2024 ⚠ BEFORE BREACH │
│ Demand sent              │ ¶ 20       │ March 15, 2024                 │
│ Suit filed               │ —          │ [Filing date]                  │
└──────────────────────────┴────────────┴────────────────────────────────┘

TIMELINE ISSUES:
• ¶ 18: Discovery date before breach date — CONTRADICTION
• Gap: What happened March 1-15?

2. ACTOR CLARITY
┌──────────────────────────┬────────────┬────────────────────────────────┐
│ Actor                    │ Defined At │ Consistency Issues             │
├──────────────────────────┼────────────┼────────────────────────────────┤
│ ACME Corp.               │ ¶ 1        │ ✓ Consistent                   │
│ John Smith               │ ¶ 3        │ ⚠ Called "Defendant" at ¶ 15   │
│ "the Company"            │ Not defined│ ✗ Who is this? ¶ 12            │
└──────────────────────────┴────────────┴────────────────────────────────┘

3. SPECIFICITY CHECK
┌────────────┬────────────────────────────────────────────────────────────┐
│ Paragraph  │ Vagueness Issue                                            │
├────────────┼────────────────────────────────────────────────────────────┤
│ ¶ 10       │ "various communications" — what specifically?              │
│ ¶ 14       │ "approximately" — can we get exact date?                   │
│ ¶ 22       │ "significant damages" — need amount or range               │
└────────────┴────────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 4 — Attack Surface Analysis

```
═══════════════════════════════════════════════════════════════
ATTACK SURFACE ANALYSIS
═══════════════════════════════════════════════════════════════

PROCEDURAL ATTACKS:
┌─────────────────────────────┬────────────┬───────────────────────────────┐
│ Attack                      │ Exposure   │ Basis in Pleading             │
├─────────────────────────────┼────────────┼───────────────────────────────┤
│ Statute of Limitations      │ [L/M/H]    │ Breach date ¶ 16; SOL = ?     │
│ Standing                    │ [L/M/H]    │ Assignment alleged? ¶ ?       │
│ Personal Jurisdiction       │ [L/M/H]    │ Contacts alleged? ¶ ?         │
│ Venue                       │ [L/M/H]    │ Basis alleged? ¶ ?            │
│ Failure to Join Party       │ [L/M/H]    │ Necessary party missing?      │
└─────────────────────────────┴────────────┴───────────────────────────────┘

SUBSTANTIVE ATTACKS:
┌─────────────────────────────┬────────────┬───────────────────────────────┐
│ Attack                      │ Exposure   │ Basis in Pleading             │
├─────────────────────────────┼────────────┼───────────────────────────────┤
│ Failure to State Claim      │ [L/M/H]    │ [Specific element gaps]       │
│ Heightened Pleading (fraud) │ [L/M/H]    │ Who/what/when/where/how?      │
│ Economic Loss Rule          │ [L/M/H]    │ Tort claim + contract?        │
│ Preemption                  │ [L/M/H]    │ Federal statute applies?      │
│ Immunity                    │ [L/M/H]    │ Government party?             │
└─────────────────────────────┴────────────┴───────────────────────────────┘

FACTUAL ATTACKS:
┌─────────────────────────────┬────────────┬───────────────────────────────┐
│ Attack                      │ Exposure   │ Basis in Pleading             │
├─────────────────────────────┼────────────┼───────────────────────────────┤
│ Causation gap               │ [L/M/H]    │ How did breach cause harm?    │
│ Damages speculative         │ [L/M/H]    │ Basis for amount?             │
│ Reliance implausible        │ [L/M/H]    │ Why would P rely?             │
│ Contradictory positions     │ [L/M/H]    │ [Specific contradictions]     │
└─────────────────────────────┴────────────┴───────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Remedy/Prayer Alignment

```
═══════════════════════════════════════════════════════════════
REMEDY ALIGNMENT CHECK
═══════════════════════════════════════════════════════════════

┌─────────────────────────────┬───────────────────────┬──────────────────────┐
│ Remedy in Prayer            │ Factual Support       │ Gap?                 │
├─────────────────────────────┼───────────────────────┼──────────────────────┤
│ Compensatory damages        │ ¶¶ 25-27             │ ✓ Linked to breach   │
│ Lost profits                │ ¶ 28                 │ ⚠ No causation shown │
│ Punitive damages            │ ¶ 30                 │ ✗ No malice/fraud    │
│ Specific performance        │ —                    │ ✗ Not alleged        │
│ Attorneys' fees             │ ¶ 9 (contract term)  │ ✓ Basis identified   │
│ Injunctive relief           │ ¶¶ 32-33            │ ⚠ Irreparable harm?  │
└─────────────────────────────┴───────────────────────┴──────────────────────┘

ISSUES:
• Lost profits: Add causation allegations connecting breach to lost business
• Punitive: Either add malice/fraud facts or remove from prayer
• Injunction: Add irreparable harm allegations
═══════════════════════════════════════════════════════════════
```

---

### STEP 6 — Top 10 Fixes

**Prioritized action list**:
```
═══════════════════════════════════════════════════════════════
TOP 10 FIXES — PRIORITIZED
═══════════════════════════════════════════════════════════════

MUST FIX (blocks filing or invites dismissal):
┌─────┬───────────────────────────────────────┬────────────┬─────────────────┐
│ #   │ Issue                                 │ Location   │ Fix             │
├─────┼───────────────────────────────────────┼────────────┼─────────────────┤
│ 1   │ Missing scienter for fraud claim      │ 3rd COA    │ Add ¶¶ re: knowledge │
│ 2   │ Timeline contradiction                │ ¶ 18 vs ¶ 16│ Correct dates   │
│ 3   │ Standing not alleged                  │ ¶¶ 1-2     │ Add assignment  │
└─────┴───────────────────────────────────────┴────────────┴─────────────────┘

SHOULD FIX (significant improvement):
┌─────┬───────────────────────────────────────┬────────────┬─────────────────┐
│ #   │ Issue                                 │ Location   │ Fix             │
├─────┼───────────────────────────────────────┼────────────┼─────────────────┤
│ 4   │ Causation for lost profits thin       │ ¶ 28       │ Add link to breach │
│ 5   │ "the Company" undefined               │ ¶ 12       │ Clarify identity│
│ 6   │ Damages amount vague                  │ ¶ 22       │ Add range/basis │
│ 7   │ Punitive damages unsupported          │ Prayer     │ Add facts or remove │
└─────┴───────────────────────────────────────┴────────────┴─────────────────┘

NICE TO FIX (polish):
┌─────┬───────────────────────────────────────┬────────────┬─────────────────┐
│ #   │ Issue                                 │ Location   │ Fix             │
├─────┼───────────────────────────────────────┼────────────┼─────────────────┤
│ 8   │ Actor inconsistency (Smith/Defendant) │ ¶ 15       │ Use defined term│
│ 9   │ "Approximately" for key date          │ ¶ 14       │ Get exact date  │
│ 10  │ Verbose allegations                   │ ¶¶ 10-11   │ Tighten language│
└─────┴───────────────────────────────────────┴────────────┴─────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 7 — Client Questions

```
═══════════════════════════════════════════════════════════════
CLIENT QUESTIONS — TO RESOLVE GAPS
═══════════════════════════════════════════════════════════════

PRIORITY 1 (need before filing):
1. [Specific question] — needed to cure [issue]
2. [Specific question] — needed to cure [issue]
3. [Specific question] — needed to cure [issue]

PRIORITY 2 (would strengthen):
4. [Specific question] — would support [element]
5. [Specific question] — would support [element]

DOCUMENTS TO REQUEST:
• [Document type] — to support [allegation]
• [Document type] — to support [allegation]
═══════════════════════════════════════════════════════════════
```

---

## Output Checklist

Before delivering:
- [ ] Quick scan for red flags complete
- [ ] Element coverage audit for each claim/defense
- [ ] Timeline coherence verified
- [ ] Actor clarity verified
- [ ] Attack surface analyzed (procedural + substantive + factual)
- [ ] Remedy alignment checked
- [ ] Top 10 fixes prioritized and actionable
- [ ] Client questions specific and answerable
- [ ] No legal standards assumed (jurisdiction placeholders used)
