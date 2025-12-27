---
name: overlay-style-and-voice
description: Apply a consistent style guide to pleadings (defined terms, headings, tone, paragraph conventions) without changing substance, and output a style compliance checklist.
metadata:
  short-description: Firm voice + formatting consistency layer
---

# Overlay: Style and Voice

## Purpose
Normalize drafting style across pleadings for consistency, readability, and professional presentation while preserving legal substance.

---

## CRITICAL CONSTRAINTS

### Never Change
- Admissions or denials
- Legal positions
- Factual meaning
- Element coverage

### Only Change
- Word choice (within same meaning)
- Sentence structure
- Defined term consistency
- Formatting and organization
- Tone (per style guide)

---

## Input Collection

| Input | Required? | Purpose |
|-------|-----------|---------|
| Draft pleading | YES | What to style |
| Style Pack OR preferences | YES | What style to apply |

**If no Style Pack, request**:
- Tone preference (neutral / assertive / restrained)
- Defined term conventions
- Heading format
- Paragraph length preference
- Any words/phrases to avoid

---

## Style Pack Application

### STEP 1 — Tone Calibration

**Analyze current draft tone**:
```
═══════════════════════════════════════════════════════════════
TONE ANALYSIS
═══════════════════════════════════════════════════════════════

CURRENT DRAFT ASSESSMENT:
• Overall tone: [Neutral / Assertive / Aggressive / Restrained]
• Inflammatory language: [None / Some / Significant]
• Conclusory statements: [Few / Moderate / Many]

STYLE PACK SPECIFICATION:
• Target tone: [From pack]
• Words to avoid: [From pack]
• Preferred verbs: [From pack]

ADJUSTMENTS NEEDED:
┌─────────────────────────────┬─────────────────────────────────────────────┐
│ Current Language            │ Styled Version                              │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ "Defendant recklessly..."   │ "Defendant failed to exercise..."          │
│ "blatantly lied"            │ "made statements that were false"          │
│ "outrageous conduct"        │ "conduct described herein"                 │
└─────────────────────────────┴─────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Defined Terms Normalization

**Audit and standardize**:
```
═══════════════════════════════════════════════════════════════
DEFINED TERMS NORMALIZATION
═══════════════════════════════════════════════════════════════

STYLE PACK CONVENTIONS:
• Party naming: [Full name then short form / Role labels / etc.]
• Document naming: ["the Agreement" / "Agreement" / etc.]
• Date references: [Month DD, YYYY / MM/DD/YYYY / etc.]

CURRENT DRAFT ISSUES:
┌─────────────────────────────┬───────────────┬─────────────────────────────┐
│ Term                        │ Defined At    │ Issues                      │
├─────────────────────────────┼───────────────┼─────────────────────────────┤
│ ACME Corporation            │ ¶ 1 ("ACME")  │ Called "Plaintiff" at ¶ 12 │
│ Services Agreement          │ ¶ 8           │ Called "the Contract" at ¶ 15│
│ John Smith                  │ ¶ 3 ("Smith") │ ✓ Consistent                │
└─────────────────────────────┴───────────────┴─────────────────────────────┘

STANDARDIZATION:
• Use "ACME" consistently (not "Plaintiff" after definition)
• Use "Agreement" consistently (not "Contract")
• Add defined term for recurring documents
═══════════════════════════════════════════════════════════════
```

---

### STEP 3 — Structure Normalization

**Apply structural conventions**:
```
═══════════════════════════════════════════════════════════════
STRUCTURE NORMALIZATION
═══════════════════════════════════════════════════════════════

STYLE PACK SPECIFICATIONS:
• Section headings: [ALL CAPS / Title Case / Bold]
• Subsection format: [A., B., C. / 1., 2., 3. / Roman numerals]
• Intro paragraph: [Include / Omit]
• Allegation organization: [Chronological / Topical]

CURRENT DRAFT VS. STYLE:
┌─────────────────────────────┬─────────────────────────────────────────────┐
│ Element                     │ Adjustment                                  │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ Section headings            │ Change from Title Case to ALL CAPS         │
│ Cause of action headers     │ Add underline per style                     │
│ Intro paragraph             │ Add per style convention                    │
│ Prayer format               │ Adjust spacing per style                    │
└─────────────────────────────┴─────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 4 — Paragraph Rules

**Apply paragraph conventions**:
```
═══════════════════════════════════════════════════════════════
PARAGRAPH STYLING
═══════════════════════════════════════════════════════════════

STYLE PACK SPECIFICATIONS:
• Ideal length: [X sentences / X lines]
• One idea per paragraph: [Strict / Flexible]
• Date format: [Month DD, YYYY]
• Money format: [$X,XXX.XX / $X,XXX / words]
• Time references: [a.m./p.m. / AM/PM / 24-hour]

PARAGRAPHS TO REVISE:
┌────────────┬────────────────────────────────────────────────────────────┐
│ Paragraph  │ Issue / Fix                                                │
├────────────┼────────────────────────────────────────────────────────────┤
│ ¶ 10       │ Too long (8 sentences) — split into ¶¶ 10-11              │
│ ¶ 14       │ Date format "1/15/24" → "January 15, 2024"                │
│ ¶ 22       │ Money format "$50000" → "$50,000.00"                      │
│ ¶ 18       │ Multiple ideas — split by topic                           │
└────────────┴────────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Boilerplate Standardization

**Apply firm-standard language**:
```
═══════════════════════════════════════════════════════════════
BOILERPLATE STANDARDIZATION
═══════════════════════════════════════════════════════════════

STYLE PACK BOILERPLATE:

1. INCORPORATION BY REFERENCE:
   Standard: "Plaintiff incorporates by reference the allegations
             set forth in paragraphs 1 through [X] as though fully
             set forth herein."

2. WHEREFORE CLAUSE:
   Standard: "WHEREFORE, Plaintiff respectfully requests that this
             Court enter judgment in Plaintiff's favor and against
             Defendant(s) as follows:..."

3. PRAYER ITEMS:
   Standard format: [Per style pack]

4. JURY DEMAND:
   Standard: "Plaintiff hereby demands a trial by jury on all
             claims so triable."

5. VERIFICATION (if used):
   Standard language: [Per style pack]

6. RESERVATION LANGUAGE:
   Standard: "Plaintiff reserves the right to amend this Complaint
             to add parties, claims, or remedies as discovery
             proceeds and additional facts become known."

CURRENT DRAFT ADJUSTMENTS:
• Incorporation: [Matches / Needs revision]
• Wherefore: [Matches / Needs revision]
• Jury demand: [Matches / Needs revision]
═══════════════════════════════════════════════════════════════
```

---

### STEP 6 — Word Choice Refinement

**Apply preferred language**:
```
═══════════════════════════════════════════════════════════════
WORD CHOICE REFINEMENT
═══════════════════════════════════════════════════════════════

WORDS TO AVOID → PREFERRED ALTERNATIVES:
┌─────────────────────────────┬─────────────────────────────────────────────┐
│ Avoid                       │ Use Instead                                 │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ "clearly"                   │ [omit or use facts]                         │
│ "obviously"                 │ [omit or use facts]                         │
│ "never"                     │ "did not" (unless literally never)          │
│ "always"                    │ "consistently" (unless literally always)    │
│ "bad faith"                 │ [specific conduct description]              │
│ "scheme"                    │ "course of conduct" or "actions"            │
└─────────────────────────────┴─────────────────────────────────────────────┘

INSTANCES IN DRAFT:
┌────────────┬────────────────────────────────┬────────────────────────────┐
│ Paragraph  │ Current                        │ Revised                    │
├────────────┼────────────────────────────────┼────────────────────────────┤
│ ¶ 15       │ "clearly knew"                 │ "knew"                     │
│ ¶ 18       │ "fraudulent scheme"            │ "course of conduct"        │
│ ¶ 22       │ "obviously false"              │ "false"                    │
└────────────┴────────────────────────────────┴────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

## Output Deliverables

### 1. Styled Pleading
Full text with all style adjustments applied.

### 2. Style Compliance Checklist
```
═══════════════════════════════════════════════════════════════
STYLE COMPLIANCE CHECKLIST
═══════════════════════════════════════════════════════════════

STYLE PACK: [Name or "User preferences"]

TONE:
☐ Matches target tone: [Neutral / Assertive / Restrained]
☐ No inflammatory language
☐ No words from "avoid" list

DEFINED TERMS:
☐ All parties defined on first use
☐ All documents defined on first use
☐ Consistent use throughout

STRUCTURE:
☐ Section headings match style
☐ Subsection format matches style
☐ Intro paragraph [included / omitted per style]

PARAGRAPH RULES:
☐ Length within guidelines
☐ One idea per paragraph
☐ Date format consistent
☐ Money format consistent

BOILERPLATE:
☐ Incorporation language matches
☐ Prayer format matches
☐ Jury demand format matches
☐ Signature block format matches
═══════════════════════════════════════════════════════════════
```

### 3. Style-Substance Conflicts
```
STYLE-SUBSTANCE CONFLICTS FLAGGED:

If any style change would alter meaning:

┌─────────────────────────────┬─────────────────────────────────────────────┐
│ Location                    │ Conflict                                    │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ ¶ 15                        │ Softening "knew" to "should have known"     │
│                             │ changes scienter allegation — NOT CHANGED   │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ ¶ 22                        │ Style prefers "approximately" but specific  │
│                             │ amount is alleged — KEPT SPECIFIC           │
└─────────────────────────────┴─────────────────────────────────────────────┘

RESOLUTION: Substance preserved; style not applied where conflict exists.
```

---

## Output Checklist

Before delivering:
- [ ] Draft restyled per pack/preferences
- [ ] Tone calibrated (no inflammatory language)
- [ ] Defined terms normalized and consistent
- [ ] Structure matches style guide
- [ ] Paragraph rules applied
- [ ] Boilerplate standardized
- [ ] Word choice refined
- [ ] Style compliance checklist complete
- [ ] Style-substance conflicts flagged (substance preserved)
- [ ] No change to legal meaning or positions
