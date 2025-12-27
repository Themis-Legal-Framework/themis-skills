---
name: draft-amended-pleading
description: Draft or revise an amended pleading by curing identified deficiencies, integrating new facts cleanly, and producing a change-log plus a deficiency-cure map and QC report.
metadata:
  short-description: Amendments that cure defects + track changes
---

# Draft Amended Pleading

## Purpose
Produce an amended pleading that cures identified deficiencies while preserving successful allegations and avoiding new vulnerabilities.

---

## CRITICAL CONSTRAINTS

### Never
- Lose track of what changed (always provide change-log)
- Create contradictions with preserved allegations
- Add unnecessary new admissions
- Cure one deficiency by creating another

### Always
- Map each deficiency to its cure
- Preserve paragraph structure where possible
- Flag any new risks introduced
- Produce comparison documentation

---

## Input Collection

**STOP if not provided**:
| Input | Why Required |
|-------|--------------|
| Prior pleading | Need baseline to amend |
| Reason for amendment | Drives what to change |

**Strongly Preferred**:
| Input | Purpose |
|-------|---------|
| Deficiency findings | Court order, tentative, M&C letter |
| New facts/documents | What to add |
| Claims to add/remove | Structural changes |
| Jurisdiction | For overlay requirements |

---

## Workflow

### STEP 1 — Deficiency Analysis

**Output**:
```
═══════════════════════════════════════════════════════════════
DEFICIENCY ANALYSIS
═══════════════════════════════════════════════════════════════

REASON FOR AMENDMENT:
☐ Court order (demurrer/MTD sustained with leave)
☐ Meet-and-confer agreement
☐ Strategic revision
☐ New facts discovered
☐ Add/remove claims or parties

SOURCE OF DEFICIENCY FINDINGS:
[Document: Order dated X / Letter dated X / Internal review]

DEFICIENCIES IDENTIFIED:
┌─────┬────────────────────────────────┬──────────────┬─────────────┐
│ #   │ Deficiency                     │ Location     │ Severity    │
├─────┼────────────────────────────────┼──────────────┼─────────────┤
│ 1   │ [Description]                  │ ¶ X, Claim Y │ Must cure   │
│ 2   │ [Description]                  │ ¶ Z          │ Must cure   │
│ 3   │ [Description]                  │ Prayer       │ Should cure │
└─────┴────────────────────────────────┴──────────────┴─────────────┘

DEADLINE: [Date or placeholder]
AMENDMENT NUMBER: [First / Second / Third, etc.]
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Cure Strategy

**For each deficiency**:
```
DEFICIENCY #1: [Description]
Location: Original ¶ [X]
Court/opposing counsel said: "[Quote or paraphrase]"

CURE STRATEGY:
- Add facts: [What specific facts will cure this]
- Restructure: [How to reorganize if needed]
- Document support: [What exhibits help]

DRAFT CURE LANGUAGE:
"On [DATE], [ACTOR] [SPECIFIC CONDUCT]. [DOCUMENT REFERENCE]."

NEW PARAGRAPH LOCATION: Amended ¶ [X] or new ¶ [Y]

RISKS OF THIS CURE:
- [Any new vulnerabilities introduced]
- [Any admissions implicit in new language]
```

---

### STEP 3 — Draft Amended Pleading

**Approach**:
```
AMENDMENT APPROACH:

☐ SURGICAL: Change only what's necessary
  - Preserve paragraph numbers where possible
  - Insert new paragraphs as ¶ 15A, 15B or renumber
  - Track every change

☐ COMPREHENSIVE: Substantial rewrite
  - New paragraph numbering throughout
  - Reorganize structure
  - Provide full redline comparison
```

**Structure**:
```
[CAPTION — update to reflect amendment number]

         [FIRST] AMENDED COMPLAINT

     Plaintiff [NAME] alleges as follows:

[Body — incorporating cures while preserving effective allegations]

[Ensure all paragraph references are updated if renumbered]
```

---

### STEP 4 — Deficiency-Cure Map

**Required output**:
```
═══════════════════════════════════════════════════════════════
DEFICIENCY-CURE MAP
═══════════════════════════════════════════════════════════════

┌─────┬──────────────────────────┬──────────────┬──────────────────────────────┐
│ #   │ Deficiency               │ Cured At     │ How Cured                    │
├─────┼──────────────────────────┼──────────────┼──────────────────────────────┤
│ 1   │ No facts showing scienter│ FAC ¶¶ 18-20│ Added: D's prior knowledge   │
│     │                          │              │ from internal emails         │
├─────┼──────────────────────────┼──────────────┼──────────────────────────────┤
│ 2   │ Reliance not alleged     │ FAC ¶ 22    │ Added: P relied by signing   │
│     │                          │              │ contract after representation│
├─────┼──────────────────────────┼──────────────┼──────────────────────────────┤
│ 3   │ Damages speculative      │ FAC ¶¶ 30-32│ Added: specific lost revenue │
│     │                          │              │ figures with documentation   │
└─────┴──────────────────────────┴──────────────┴──────────────────────────────┘

CONFIRMATION:
☐ All "must cure" deficiencies addressed
☐ All "should cure" deficiencies addressed
☐ No deficiency left unaddressed
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Change-Log

**Required output**:
```
═══════════════════════════════════════════════════════════════
CHANGE-LOG: ORIGINAL → FIRST AMENDED
═══════════════════════════════════════════════════════════════

STRUCTURAL CHANGES:
┌─────────────────────────────────────────────────────────────┐
│ Change Type        │ Description                            │
├─────────────────────────────────────────────────────────────┤
│ Claims ADDED       │ Fourth COA: Negligent Misrepresentation│
│ Claims REMOVED     │ None                                   │
│ Parties ADDED      │ None                                   │
│ Parties REMOVED    │ Defendant DOE removed                  │
└─────────────────────────────────────────────────────────────┘

PARAGRAPH-LEVEL CHANGES:
┌───────────────┬───────────────┬─────────────────────────────┐
│ Original ¶    │ Amended ¶     │ Change                      │
├───────────────┼───────────────┼─────────────────────────────┤
│ ¶ 15          │ ¶ 15          │ Added date and specifics    │
│ —             │ ¶ 16-18 (NEW) │ New scienter allegations    │
│ ¶ 16          │ ¶ 19          │ Renumbered only             │
│ ¶ 20          │ ¶ 23          │ Revised damages figures     │
│ ¶ 25          │ DELETED       │ Removed speculative claim   │
└───────────────┴───────────────┴─────────────────────────────┘

EXHIBIT CHANGES:
┌─────────────────────────────────────────────────────────────┐
│ Exhibit │ Change                                            │
├─────────────────────────────────────────────────────────────┤
│ Ex. A   │ No change                                         │
│ Ex. D   │ NEW: Internal emails re: knowledge                │
│ Ex. E   │ NEW: Revenue documentation                        │
└─────────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 6 — QC Report

**Required output**:
```
═══════════════════════════════════════════════════════════════
AMENDED PLEADING QC REPORT
═══════════════════════════════════════════════════════════════

1. DEFICIENCY CURE VERIFICATION
┌─────────────────────────────────┬────────────┬─────────────────┐
│ Deficiency                      │ Status     │ Paragraph       │
├─────────────────────────────────┼────────────┼─────────────────┤
│ [Deficiency 1]                  │ CURED      │ FAC ¶¶ 18-20   │
│ [Deficiency 2]                  │ CURED      │ FAC ¶ 22       │
│ [Deficiency 3]                  │ PARTIALLY  │ FAC ¶ 30 [note]│
└─────────────────────────────────┴────────────┴─────────────────┘

2. INTERNAL CONSISTENCY CHECK
┌─────────────────────────────────────────────────────────────────┐
│ Issue                           │ Status                        │
├─────────────────────────────────────────────────────────────────┤
│ Dates consistent throughout     │ ✓ OK                          │
│ Party names consistent          │ ✓ OK                          │
│ New ¶s don't contradict old     │ ✓ OK                          │
│ Paragraph references updated    │ ✗ Check: ¶ 45 refs old ¶ 20   │
└─────────────────────────────────────────────────────────────────┘

3. NEW VULNERABILITIES INTRODUCED
┌─────────────────────────────────────────────────────────────────┐
│ New Allegation                  │ Potential Risk                │
├─────────────────────────────────────────────────────────────────┤
│ FAC ¶ 18 (D knew from emails)   │ Must produce emails           │
│ FAC ¶ 31 (specific revenue)     │ Locked into damages figure    │
└─────────────────────────────────────────────────────────────────┘

4. ELEMENT COVERAGE (re-check)
[Re-run element coverage for any modified claims]

5. FILING REQUIREMENTS
┌─────────────────────────────────────────────────────────────────┐
│ Requirement                     │ Status                        │
├─────────────────────────────────────────────────────────────────┤
│ Leave of court                  │ [Required? / Obtained?]       │
│ Redline required                │ [CHECK local rules]           │
│ Service requirements            │ [New parties? / All parties?] │
│ Filing deadline                 │ [Date]                        │
└─────────────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

## Output Checklist

Before delivering:
- [ ] Deficiency analysis complete
- [ ] Every deficiency has cure strategy
- [ ] Deficiency-cure map with paragraph references
- [ ] Change-log (structural + paragraph-level)
- [ ] No contradictions between old and new allegations
- [ ] Paragraph references updated if renumbered
- [ ] Element coverage re-verified for changed claims
- [ ] New vulnerabilities identified
- [ ] Filing requirements noted
