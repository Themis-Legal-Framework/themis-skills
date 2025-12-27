---
name: overlay-jurisdiction-pleadings
description: Apply jurisdiction/venue-specific pleading requirements (caption blocks, required sections, terminology, verifications, formatting, and pleading standards) to an existing pleading draft using a user-provided jurisdiction pack.
metadata:
  short-description: Jurisdiction customization layer for pleadings
---

# Overlay: Jurisdiction Pleadings

## Purpose
Transform a jurisdiction-agnostic pleading into a jurisdiction-compliant document based on user-supplied local rules and templates.

---

## CRITICAL CONSTRAINTS

### Never Guess Local Rules
- If requirement is unknown, use explicit placeholder:
  ```
  [LOCAL RULE REQUIRED: {specific requirement}]
  ```
- Do not assume any jurisdiction's requirements apply to another

### Always Require
- Jurisdiction identification
- Either a Jurisdiction Pack OR user-provided specifics
- Explicit confirmation of compliance items

---

## Input Collection

**STOP if not provided**:
| Input | Why Required |
|-------|--------------|
| Draft pleading | What to transform |
| Jurisdiction/venue | Which rules apply |

**Required (one of)**:
| Input | Description |
|-------|-------------|
| Jurisdiction Pack | Structured local requirements file |
| User-provided rules | Ad hoc caption, sections, standards |

---

## Jurisdiction Pack Usage

### If Pack Provided

**Read and apply each section**:

```
═══════════════════════════════════════════════════════════════
JURISDICTION PACK APPLICATION
═══════════════════════════════════════════════════════════════

PACK: [Name/jurisdiction]
COURT: [Specific court]
CASE TYPE: [Civil/limited/unlimited/federal/etc.]

1. CAPTION BLOCK
   ☐ Court name format: [Apply from pack]
   ☐ Case number format: [Apply from pack]
   ☐ Party designation format: [Apply from pack]
   ☐ Document title format: [Apply from pack]

2. REQUIRED SECTIONS
   ☐ Civil cover sheet: [Required? / Attached?]
   ☐ Summons: [Required? / Attached?]
   ☐ Verification: [Required? / When? / Language?]
   ☐ Certificate of service: [Format?]

3. SIGNATURE BLOCK
   ☐ Attorney info requirements: [Bar number, address, etc.]
   ☐ E-signature permitted: [Yes/No]
   ☐ Firm name required: [Yes/No]

4. PLEADING STANDARDS
   ☐ General standard: [Notice / fact / code]
   ☐ Heightened pleading: [Fraud? Special damages? Punitive?]
   ☐ Required jurisdictional allegations: [List]

5. FORMATTING
   ☐ Page size: [Letter/A4]
   ☐ Margins: [Specific requirements]
   ☐ Font: [Required font/size]
   ☐ Line spacing: [Single/double]
   ☐ Line numbering: [Required?]
   ☐ Page limits: [Any?]
═══════════════════════════════════════════════════════════════
```

### If No Pack Provided

**Request minimum information**:

```
MINIMUM REQUIRED FROM USER:

1. Caption example (from a recent filing in this court)

2. Required sections checklist:
   ☐ Civil cover sheet required?
   ☐ Verification required? (for what document types?)
   ☐ Summons form required?
   ☐ Other required attachments?

3. Heightened pleading requirements:
   ☐ Fraud claims — specificity required?
   ☐ Special damages — itemization required?
   ☐ Punitive damages — specific allegations?

4. Formatting constraints:
   ☐ Page/word limits?
   ☐ Line numbering required?
   ☐ Specific font/spacing requirements?

5. Any local practice notes:
   ☐ Common clerk rejections?
   ☐ Preferred organization?
```

---

## Transformation Workflow

### STEP 1 — Caption Transformation

**From generic**:
```
[COURT NAME]

PLAINTIFF NAME,
     Plaintiff,
v.
DEFENDANT NAME,
     Defendant.

                              COMPLAINT
```

**To jurisdiction-specific** (example: California Superior):
```
                                                    Case No. [TO BE ASSIGNED]
SUPERIOR COURT OF THE STATE OF CALIFORNIA
COUNTY OF LOS ANGELES
CENTRAL DISTRICT

ACME CORPORATION, a Delaware     )
corporation,                     )
                                )
          Plaintiff,            )     COMPLAINT FOR:
                                )
     v.                         )     1. Breach of Contract
                                )     2. Fraud
XYZ INC., a California          )     3. Negligent Misrepresentation
corporation; and DOES 1-10,     )
                                )     DEMAND FOR JURY TRIAL
          Defendants.           )
________________________________)
```

---

### STEP 2 — Section Additions

**Add required sections based on jurisdiction**:

```
SECTIONS TO ADD:
┌─────────────────────────────┬────────────────────────────────────────────┐
│ Section                     │ Status                                     │
├─────────────────────────────┼────────────────────────────────────────────┤
│ Doe defendants              │ [Added if required / N/A for federal]     │
│ Jurisdictional allegations  │ [Verify against local requirements]        │
│ Venue allegations           │ [Verify against local requirements]        │
│ Verification                │ [Added / Not required]                     │
│ Certificate of interested   │ [Added if required / N/A]                  │
│ parties                     │                                            │
└─────────────────────────────┴────────────────────────────────────────────┘
```

---

### STEP 3 — Terminology Normalization

**Apply jurisdiction-specific terms**:
```
TERMINOLOGY ADJUSTMENTS:
┌─────────────────────────────┬─────────────────────────────────────────────┐
│ Generic Term                │ Jurisdiction-Specific Term                  │
├─────────────────────────────┼─────────────────────────────────────────────┤
│ Complaint                   │ [Complaint / Petition / Statement of Claim] │
│ Defendant                   │ [Defendant / Respondent]                    │
│ Answer                      │ [Answer / Response / Defence]               │
│ Motion to Dismiss           │ [MTD / Demurrer / Motion to Strike]        │
│ Discovery                   │ [Discovery / Disclosure]                    │
└─────────────────────────────┴─────────────────────────────────────────────┘
```

---

### STEP 4 — Heightened Pleading Check

**If fraud or similar claims**:
```
HEIGHTENED PLEADING REQUIREMENTS:
═══════════════════════════════════════════════════════════════

CLAIM: [Fraud / Other heightened claim]
STANDARD: [Jurisdiction-specific standard]

CHECKLIST (verify allegations include):
┌─────────────────────────────┬───────────────┬────────────────────────────┐
│ Requirement                 │ Present?      │ Location                   │
├─────────────────────────────┼───────────────┼────────────────────────────┤
│ WHO made representation     │ ☐ Yes ☐ No   │ ¶ ___                      │
│ WHAT was stated             │ ☐ Yes ☐ No   │ ¶ ___                      │
│ WHEN statement made         │ ☐ Yes ☐ No   │ ¶ ___                      │
│ WHERE statement made        │ ☐ Yes ☐ No   │ ¶ ___                      │
│ HOW statement was false     │ ☐ Yes ☐ No   │ ¶ ___                      │
│ WHY speaker knew false      │ ☐ Yes ☐ No   │ ¶ ___                      │
└─────────────────────────────┴───────────────┴────────────────────────────┘

DEFICIENCIES TO CURE:
• [List any missing heightened pleading elements]
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Format Compliance

**Apply formatting requirements**:
```
FORMAT COMPLIANCE:
┌─────────────────────────────┬────────────────────┬────────────────────────┐
│ Requirement                 │ Jurisdiction Spec  │ Current Draft          │
├─────────────────────────────┼────────────────────┼────────────────────────┤
│ Page size                   │ [Requirement]      │ [Compliant? / Fix]     │
│ Margins                     │ [Requirement]      │ [Compliant? / Fix]     │
│ Font                        │ [Requirement]      │ [Compliant? / Fix]     │
│ Line spacing                │ [Requirement]      │ [Compliant? / Fix]     │
│ Line numbers                │ [Requirement]      │ [Compliant? / Fix]     │
│ Page limit                  │ [Requirement]      │ [X pages / compliant?] │
│ Footer/header               │ [Requirement]      │ [Compliant? / Fix]     │
└─────────────────────────────┴────────────────────┴────────────────────────┘
```

---

## Output Deliverables

### 1. Transformed Pleading
Full text with jurisdiction-specific formatting applied.

### 2. Compliance Checklist
```
═══════════════════════════════════════════════════════════════
JURISDICTION COMPLIANCE CHECKLIST
═══════════════════════════════════════════════════════════════

JURISDICTION: [Name]
COURT: [Specific court]
DOCUMENT: [Complaint / Answer / etc.]

CAPTION:
☐ Court name correct
☐ Case number format correct (or placeholder)
☐ Party designations correct
☐ Document title correct

REQUIRED SECTIONS:
☐ Civil cover sheet [Required: Y/N] [Included: Y/N]
☐ Summons [Required: Y/N] [Included: Y/N]
☐ Verification [Required: Y/N] [Included: Y/N]
☐ Certificate of service [Required: Y/N] [Included: Y/N]

SUBSTANTIVE REQUIREMENTS:
☐ Jurisdictional allegations present
☐ Venue allegations present
☐ Heightened pleading satisfied (if applicable)

FORMATTING:
☐ All formatting requirements met

SIGNATURE BLOCK:
☐ Attorney information complete
☐ Bar number included
☐ Contact information included
═══════════════════════════════════════════════════════════════
```

### 3. Open Questions
```
OPEN QUESTIONS — LOCAL REQUIREMENTS UNKNOWN:

1. [Specific requirement not addressed in pack]
2. [Specific requirement not addressed in pack]

ACTION: Verify with local rules or clerk's office before filing.
```

---

## Output Checklist

Before delivering:
- [ ] Draft transformed with jurisdiction formatting
- [ ] Caption matches local format
- [ ] All required sections included or noted
- [ ] Terminology normalized
- [ ] Heightened pleading verified (if applicable)
- [ ] Format requirements applied
- [ ] Compliance checklist complete
- [ ] Unknown requirements flagged with placeholders
