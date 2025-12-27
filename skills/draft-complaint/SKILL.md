---
name: draft-complaint
description: Draft a civil complaint from a fact packet: parties/capacities, jurisdiction/venue placeholders, general allegations, claim counts with element coverage, and remedies/prayer, with a pleading-risk QC report.
metadata:
  short-description: Complaint drafting with element coverage + QC
---

# Draft Complaint

## Purpose
Produce a complete, well-structured complaint with element coverage tracking and defensive awareness.

---

## CRITICAL CONSTRAINTS

### Never Invent
- Facts not provided by user
- Case citations or statutory authority
- Jurisdictional requirements for unknown forums
- Damage amounts without factual basis

### Always Include
- Element coverage table for each cause of action
- Placeholders for missing information
- Pleading-risk QC report
- Missing facts question list

---

## Input Collection

**STOP if not provided**:
| Input | Why Required |
|-------|--------------|
| Parties | Cannot draft caption or party allegations |
| Core facts | Cannot draft general allegations |
| Claims to plead | Cannot structure causes of action |

**Strongly Preferred**:
| Input | Default if Missing |
|-------|-------------------|
| Forum | Use `[JURISDICTION]` placeholders throughout |
| Damages/remedies | Generic prayer; flag for specifics |
| Pre-suit steps | Flag potential exhaustion/notice issues |
| Vulnerabilities | Unknown risk exposure |
| Tone preference | Neutral, professional |

---

## Workflow

### STEP 1 — Strategy Memo (Brief)

**Output**: 1-page max strategic framing

```
═══════════════════════════════════════════════════════════════
COMPLAINT STRATEGY MEMO
═══════════════════════════════════════════════════════════════

CASE THEORY:
[2-3 sentences: what happened and why defendant is liable]

PRIMARY THEME:
[One sentence the factfinder should remember]

CLAIMS (ranked by strength):
1. [Claim]: [Strength assessment] — [Key vulnerability]
2. [Claim]: [Strength assessment] — [Key vulnerability]

ANTICIPATED DEFENSES:
┌─────────────────────┬────────────────────┬──────────────────┐
│ Defense             │ Exposure Level     │ Pleading Response│
├─────────────────────┼────────────────────┼──────────────────┤
│ Statute of limits   │ Low/Med/High       │ [How addressed]  │
│ Standing            │ Low/Med/High       │ [How addressed]  │
│ Failure to state    │ Low/Med/High       │ [How addressed]  │
└─────────────────────┴────────────────────┴──────────────────┘

STRATEGIC NOTES:
• [Key point 1]
• [Key point 2]
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Element Coverage Table

**Invoke** `claims-and-elements-builder` logic.

**Output for each claim**:
```
CLAIM: [Name]
AUTHORITY: [Citation or ADD ELEMENTS placeholder]

┌─────────┬────────────────────┬────────────────┬────────────────┬────────┐
│ Element │ Allegation         │ Paragraph(s)   │ Missing Facts  │ Risk   │
├─────────┼────────────────────┼────────────────┼────────────────┼────────┤
│ 1       │ [What we allege]   │ ¶¶ X-Y         │ [Gaps]         │ L/M/H  │
│ 2       │ [What we allege]   │ ¶¶ X-Y         │ [Gaps]         │ L/M/H  │
└─────────┴────────────────────┴────────────────┴────────────────┴────────┘
```

---

### STEP 3 — Draft Complaint

**Structure**:

```
[CAPTION BLOCK — use overlay or placeholder]

                              COMPLAINT

     Plaintiff [NAME] alleges as follows:

                         I. PARTIES

¶ 1.  [Plaintiff capacity, residence/PPB, standing basis]

¶ 2.  [Defendant capacity, residence/PPB, basis for liability]

[Additional parties as needed]

                   II. JURISDICTION AND VENUE

¶ X.  [Subject matter jurisdiction — or placeholder]

¶ Y.  [Personal jurisdiction — or placeholder]

¶ Z.  [Venue — or placeholder]

                    III. GENERAL ALLEGATIONS

[Chronological fact narrative in numbered paragraphs]
[Each paragraph: one fact, anchored in time, with document references]
[Use invoke of convert-facts-to-numbered-allegations for complex facts]

               IV. FIRST CAUSE OF ACTION
                   [Claim Name]
               (Against [Defendant(s)])

¶ A.  Plaintiff incorporates by reference paragraphs 1 through [X]
      as though fully set forth herein.

¶ B.  [Element 1 as ultimate fact with supporting allegations]

¶ C.  [Element 2 as ultimate fact with supporting allegations]

[Continue for each element]

¶ Z.  As a direct and proximate result of [Defendant's conduct],
      Plaintiff has suffered damages in an amount to be proven at
      trial, but not less than $[AMOUNT].

              V. SECOND CAUSE OF ACTION
                   [Next Claim]
[Repeat structure]

                    VI. PRAYER FOR RELIEF

     WHEREFORE, Plaintiff prays for judgment against Defendant(s)
as follows:

     1. For compensatory damages according to proof;

     2. For [special damages: lost profits, etc.] according to proof;

     3. For [punitive/exemplary damages if applicable];

     4. For [equitable relief: injunction, specific performance, etc.];

     5. For prejudgment interest at the legal rate;

     6. For costs of suit incurred herein;

     7. For attorneys' fees [if contractual or statutory basis];

     8. For such other and further relief as the Court deems just
        and proper.

                      VII. JURY DEMAND

     Plaintiff hereby demands a trial by jury on all issues so triable.


DATED: [DATE]                    Respectfully submitted,

                                 [SIGNATURE BLOCK]
                                 Attorneys for Plaintiff
```

---

### STEP 4 — Deliverables Package

**Deliver all of the following**:

#### A. Draft Complaint
Full text as above.

#### B. Missing Facts List
```
MISSING FACTS — QUESTIONS FOR CLIENT

PRIORITY 1 (blocks filing):
• [Question]: Needed for [paragraph/element]
• [Question]: Needed for [paragraph/element]

PRIORITY 2 (strengthens pleading):
• [Question]: Would support [element]
• [Question]: Would support [element]

PRIORITY 3 (nice to have):
• [Question]: Additional context for [section]
```

#### C. Pleading-Risk QC Report

```
═══════════════════════════════════════════════════════════════
PLEADING-RISK QC REPORT
═══════════════════════════════════════════════════════════════

1. THIN ELEMENTS / CONCLUSORY ALLEGATIONS
┌─────────┬────────────┬─────────────────────────────────────────┐
│ Claim   │ Paragraph  │ Issue                                   │
├─────────┼────────────┼─────────────────────────────────────────┤
│ [Claim] │ ¶ [X]      │ [Description of weakness]               │
└─────────┴────────────┴─────────────────────────────────────────┘

2. TIMELINE GAPS
┌─────────────────────┬────────────────────────────────────────────┐
│ Gap Period          │ Significance                               │
├─────────────────────┼────────────────────────────────────────────┤
│ [Date range]        │ [Why this matters]                         │
└─────────────────────┴────────────────────────────────────────────┘

3. PARTY / AGENCY / ALTER EGO ISSUES
• [Issue]: [Recommendation]

4. CAUSATION / DAMAGES LINKAGE
┌─────────────────────┬─────────────────────┬─────────────────────┐
│ Damages Claimed     │ Causal Allegations  │ Gap?                │
├─────────────────────┼─────────────────────┼─────────────────────┤
│ [Type]              │ ¶¶ [X-Y]            │ [Assessment]        │
└─────────────────────┴─────────────────────┴─────────────────────┘

5. DEFENSIVE EXPOSURE
┌─────────────────────┬────────────┬──────────────────────────────┐
│ Defense             │ Risk Level │ Mitigation in Pleading       │
├─────────────────────┼────────────┼──────────────────────────────┤
│ Statute of limits   │ [L/M/H]    │ [How addressed or flag]      │
│ Standing            │ [L/M/H]    │ [How addressed or flag]      │
│ Notice/exhaustion   │ [L/M/H]    │ [How addressed or flag]      │
│ Preemption          │ [L/M/H]    │ [CHECK: applicable?]         │
│ Immunity            │ [L/M/H]    │ [CHECK: applicable?]         │
└─────────────────────┴────────────┴──────────────────────────────┘

6. EXHIBIT / ATTACHMENT DECISIONS
┌─────────────────────┬────────────┬──────────────────────────────┐
│ Document            │ Decision   │ Risk Assessment              │
├─────────────────────┼────────────┼──────────────────────────────┤
│ [Doc name]          │ Attach/Ref │ [Potential adverse content]  │
└─────────────────────┴────────────┴──────────────────────────────┘

7. OVERPLEADING RISKS
• [Unnecessary admission in ¶ X]
• [Theory lock-in concern]
• [Inconsistent position risk]

═══════════════════════════════════════════════════════════════
```

---

## Jurisdiction Overlay

When forum is known, invoke `overlay-jurisdiction-pleadings` to apply:
- Caption block (court name, case number format)
- Required jurisdictional allegations
- Heightened pleading rules (fraud, special damages)
- Verification requirements
- Local formatting rules

---

## Output Checklist

Before delivering:
- [ ] Strategy memo complete
- [ ] Element coverage table for each claim
- [ ] All paragraphs numbered consecutively
- [ ] Defined terms consistent throughout
- [ ] No invented facts or authorities
- [ ] All placeholders clearly bracketed
- [ ] Missing facts listed with priority
- [ ] Full QC report with all 7 sections
- [ ] Prayer matches alleged damages/relief
