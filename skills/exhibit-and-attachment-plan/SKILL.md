---
name: exhibit-and-attachment-plan
description: Create an exhibit/attachment plan for pleadings: what to attach vs reference only, how to cite documents safely, and risks of incorporation/admissions, with jurisdiction-dependent placeholders.
metadata:
  short-description: Pleading exhibits strategy + risk flags
---

# Exhibit and Attachment Plan (Pleadings)

## Purpose
Develop a strategic plan for document attachments that strengthens pleading credibility while minimizing risks from adverse content, incorporation by reference, and authentication issues.

---

## CRITICAL CONSTRAINTS

### Never Assume
- Local rules on attachments (vary by jurisdiction)
- What opposing party will do with attached documents
- Authentication will be stipulated

### Always Consider
- Does attachment help or hurt?
- What adverse content might opponent cite?
- Is document final or draft?
- Confidentiality/privilege concerns

---

## Input Collection

| Input | Required? | Purpose |
|-------|-----------|---------|
| Draft pleading or outline | YES | What documents are referenced |
| Document list | YES | What's available to attach |
| User goals | Preferred | Credibility, motion resistance, etc. |
| Jurisdiction | Preferred | Local attachment rules |

---

## Workflow

### STEP 1 — Document Inventory

**Output**:
```
═══════════════════════════════════════════════════════════════
DOCUMENT INVENTORY
═══════════════════════════════════════════════════════════════

┌─────┬─────────────────────┬──────────────┬──────────────────────────────┐
│ #   │ Document            │ Type         │ Role in Pleading             │
├─────┼─────────────────────┼──────────────┼──────────────────────────────┤
│ 1   │ Services Agreement  │ Contract     │ Basis for breach claim       │
│ 2   │ March 15 Email      │ Communication│ Evidence of repudiation      │
│ 3   │ Invoices (12 docs)  │ Financial    │ Damages calculation          │
│ 4   │ Board Minutes       │ Internal     │ Knowledge/authorization      │
│ 5   │ Demand Letter       │ Communication│ Pre-suit notice              │
└─────┴─────────────────────┴──────────────┴──────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Decision Framework

**For each document, analyze**:

```
DOCUMENT: [Name]
═══════════════════════════════════════════════════════════════

ATTACHMENT ANALYSIS:

1. CENTRALITY
   ☐ Central to claim (contract sued upon, key communication)
   ☐ Supporting evidence (corroborates allegations)
   ☐ Peripheral (context only)

2. FAVORABLE/ADVERSE CONTENT
   Favorable provisions:
   • [List favorable terms/content]

   Adverse provisions:
   • [List adverse terms/content]

   Net assessment: [Favorable / Neutral / Mixed / Adverse]

3. AUTHENTICATION
   ☐ Self-authenticating (notarized, certified, etc.)
   ☐ Easily authenticated (signatures, letterhead)
   ☐ May face challenge (unsigned, draft, screenshot)
   ☐ Authentication complex (requires foundation witness)

4. INCORPORATION RISK
   If attached, opponent can cite:
   • [Provision/content that could be used against us]
   • [Provision/content that could be used against us]

5. CONFIDENTIALITY
   ☐ No confidentiality concerns
   ☐ Contains confidential business info
   ☐ May contain privileged content
   ☐ Third-party privacy concerns
   ☐ Trade secrets / proprietary

6. PRACTICAL FACTORS
   ☐ Length: [# pages] — [Manageable / Voluminous]
   ☐ Format: [PDF / Native / Other]
   ☐ Completeness: [Full document / Excerpt / Redacted]

RECOMMENDATION:
☐ ATTACH — [Reason]
☐ REFERENCE ONLY — [Reason]
☐ OMIT FOR NOW — [Reason]
☐ ATTACH EXCERPT — [What to include/exclude]
═══════════════════════════════════════════════════════════════
```

---

### STEP 3 — Exhibit Plan

**Output**:
```
═══════════════════════════════════════════════════════════════
EXHIBIT PLAN
═══════════════════════════════════════════════════════════════

DOCUMENTS TO ATTACH:
┌─────────┬─────────────────────┬────────────────┬──────────────────────────┐
│ Exhibit │ Document            │ Referenced In  │ Purpose                  │
├─────────┼─────────────────────┼────────────────┼──────────────────────────┤
│ A       │ Services Agreement  │ ¶¶ 8-12, 25   │ Contract at issue        │
│ B       │ March 15 Email      │ ¶ 18          │ Anticipatory repudiation │
│ C       │ Demand Letter       │ ¶ 22          │ Pre-suit notice          │
└─────────┴─────────────────────┴────────────────┴──────────────────────────┘

DOCUMENTS TO REFERENCE ONLY (not attach):
┌─────────────────────────────┬────────────────┬──────────────────────────────┐
│ Document                    │ Referenced In  │ Reason Not Attached          │
├─────────────────────────────┼────────────────┼──────────────────────────────┤
│ Invoices (12 docs)          │ ¶¶ 14-15      │ Voluminous; describe in text │
│ Board Minutes               │ ¶ 10          │ Contains other confidential  │
└─────────────────────────────┴────────────────┴──────────────────────────────┘

DOCUMENTS TO OMIT:
┌─────────────────────────────┬────────────────────────────────────────────────┐
│ Document                    │ Reason                                         │
├─────────────────────────────┼────────────────────────────────────────────────┤
│ Draft Agreement (v2)        │ Not final; invites confusion                   │
│ Internal Strategy Memo      │ Privileged; not relevant to pleading           │
└─────────────────────────────┴────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 4 — Citation Language

**Provide draft language for each exhibit**:

```
EXHIBIT CITATION LANGUAGE
═══════════════════════════════════════════════════════════════

EXHIBIT A (Services Agreement):
"A true and correct copy of the Agreement is attached hereto as
Exhibit A and incorporated herein by reference."

EXHIBIT B (March 15 Email):
"A true and correct copy of this email is attached hereto as
Exhibit B and incorporated herein by reference."

REFERENCED-ONLY DOCUMENTS:

Invoices:
"Plaintiff issued twelve invoices to Defendant between January
and December 2024, totaling $300,000."
[No incorporation by reference — avoids making all 12 part of pleading]

Board Minutes:
"As reflected in the minutes of XYZ's Board of Directors meeting
on February 1, 2024, the Board authorized [specific action]."
[Describes relevant content without attaching full document]
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Risk Assessment

**Output**:
```
═══════════════════════════════════════════════════════════════
EXHIBIT RISK ASSESSMENT
═══════════════════════════════════════════════════════════════

1. INCORPORATION BY REFERENCE RISKS
┌───────────┬──────────────────────────────────────────────────────────┐
│ Exhibit   │ Adverse Content Opponent May Cite                        │
├───────────┼──────────────────────────────────────────────────────────┤
│ A (Agmt)  │ § 12.3: Limitation of liability clause                   │
│           │ § 15.1: Notice requirements (did we comply?)             │
│           │ § 8.2: Conditions precedent                              │
├───────────┼──────────────────────────────────────────────────────────┤
│ B (Email) │ Paragraph 2: Client's prior complaints                   │
└───────────┴──────────────────────────────────────────────────────────┘

2. AUTHENTICATION RISKS
┌───────────┬───────────────┬──────────────────────────────────────────┐
│ Exhibit   │ Risk Level    │ Issue                                    │
├───────────┼───────────────┼──────────────────────────────────────────┤
│ A         │ Low           │ Signed by both parties                   │
│ B         │ Medium        │ Email — may need custodian declaration   │
│ C         │ Low           │ Our letter with signature                │
└───────────┴───────────────┴──────────────────────────────────────────┘

3. UNINTENDED ADMISSION RISKS
┌───────────────────────────────────────────────────────────────────────┐
│ Risk                              │ Mitigation                        │
├───────────────────────────────────────────────────────────────────────┤
│ Attaching contract admits         │ OK if contract existence not      │
│ contract existed                  │ disputed                          │
├───────────────────────────────────────────────────────────────────────┤
│ Email shows our client knew X     │ Evaluate if knowledge admission   │
│                                   │ is problematic for claims         │
└───────────────────────────────────────────────────────────────────────┘

4. CONFIDENTIALITY RISKS
┌───────────┬───────────────────────────────────────────────────────────┐
│ Exhibit   │ Concern                                                   │
├───────────┼───────────────────────────────────────────────────────────┤
│ A         │ Contains pricing terms — consider redaction or seal       │
│ None      │ No third-party PII concerns                               │
└───────────┴───────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 6 — Jurisdiction Considerations

**Output**:
```
JURISDICTION-DEPENDENT ISSUES
[CHECK LOCAL PRACTICE]

☐ Are exhibits required for contract claims?
☐ Are exhibits permitted at pleading stage?
☐ Page limits — do exhibits count?
☐ E-filing format requirements?
☐ Confidential filing procedures available?
☐ Requirement to attach written instruments?

PLACEHOLDER: [CHECK LOCAL RULE: attachment requirements for {jurisdiction}]
```

---

## Decision Heuristics

```
WHEN TO ATTACH:
✓ Central to claim (contract sued upon)
✓ Short and favorable
✓ Strengthens plausibility (specific, concrete)
✓ Preempts authentication disputes
✓ Required by local rule

WHEN TO REFERENCE ONLY:
○ Voluminous (describe key terms in text)
○ Mixed favorable/adverse content
○ Contains confidential/sensitive material
○ Not central to claim

WHEN TO OMIT:
✗ Primarily adverse content
✗ Authentication uncertain
✗ Creates more questions than answers
✗ Privileged or work product
✗ Contains irrelevant sensitive information
```

---

## Output Checklist

Before delivering:
- [ ] Document inventory complete
- [ ] Each document analyzed with decision framework
- [ ] Exhibit plan with clear attach/reference/omit decisions
- [ ] Citation language provided for each exhibit
- [ ] Risk assessment (incorporation, authentication, admissions)
- [ ] Jurisdiction-dependent issues flagged
- [ ] Confidentiality concerns identified
