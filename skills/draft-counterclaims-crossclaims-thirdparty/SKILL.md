---
name: draft-counterclaims-crossclaims-thirdparty
description: Draft counterclaims/crossclaims/third-party claims with party alignment, element coverage planning, and clean integration with existing pleadings, plus a dependency checklist.
metadata:
  short-description: Counterclaims and related pleadings
---

# Draft Counterclaims / Crossclaims / Third-Party Claims

## Purpose
Produce offensive claims within a defensive pleading, ensuring proper party alignment, element coverage, and consistency with answer positions.

---

## CRITICAL CONSTRAINTS

### Never Invent
- Facts not provided by user
- Elements for claims (use placeholders)
- Joinder/impleader requirements (jurisdiction-dependent)

### Always Ensure
- Consistency with answer positions (no contradictions)
- Clear party alignment (who is claiming what against whom)
- Element coverage for each claim
- Integration instructions with existing pleadings

---

## Input Collection

**STOP if not provided**:
| Input | Why Required |
|-------|--------------|
| Claim type | Counterclaim / crossclaim / third-party claim |
| Parties | Who is asserting against whom |
| Claims to assert | What causes of action |
| Core facts | Basis for claims |

**Strongly Preferred**:
| Input | Default if Missing |
|-------|-------------------|
| Forum | Use placeholders for procedural requirements |
| Answer integration | Ask how to incorporate |
| Remedies sought | Generic prayer |
| Documents | Note what's available |

---

## Claim Type Distinctions

```
┌─────────────────────┬────────────────────────────────────────────────────┐
│ Type                │ Who Against Whom                                   │
├─────────────────────┼────────────────────────────────────────────────────┤
│ COUNTERCLAIM        │ Defendant → Plaintiff                              │
│   - Compulsory      │ Arises from same transaction/occurrence            │
│   - Permissive      │ Different transaction; may require indep. jurisd.  │
├─────────────────────┼────────────────────────────────────────────────────┤
│ CROSSCLAIM          │ Co-party → Co-party (e.g., Defendant A → Def. B)   │
│                     │ Must arise from same transaction/occurrence        │
├─────────────────────┼────────────────────────────────────────────────────┤
│ THIRD-PARTY CLAIM   │ Defendant → New Party (not yet in case)            │
│ (Impleader)         │ New party may be liable for all/part of claim      │
└─────────────────────┴────────────────────────────────────────────────────┘

JURISDICTION FLAGS:
[CHECK: timing requirements for third-party claims]
[CHECK: leave of court required after answer?]
[CHECK: service requirements for new parties]
```

---

## Workflow

### STEP 1 — Party Alignment Analysis

**Output**:
```
═══════════════════════════════════════════════════════════════
PARTY ALIGNMENT ANALYSIS
═══════════════════════════════════════════════════════════════

ORIGINAL ACTION:
Plaintiff(s): [List]
Defendant(s): [List]

THIS CLAIM:
Type: [Counterclaim / Crossclaim / Third-Party Claim]
Asserting Party: [Who]  → Designation: [Counter-Plaintiff / Cross-Claimant / Third-Party Plaintiff]
Target Party: [Who]     → Designation: [Counter-Defendant / Cross-Defendant / Third-Party Defendant]

CLAIMS TO ASSERT:
1. [Claim name] — [Brief basis]
2. [Claim name] — [Brief basis]

RELATIONSHIP TO ORIGINAL CLAIMS:
┌─────────────────────────────────────────────────────────────┐
│ Original Claim        │ Relationship to Counterclaim        │
├─────────────────────────────────────────────────────────────┤
│ Breach of Contract    │ Counter: Plaintiff breached first   │
│ Negligence            │ Counter: Comparative fault          │
└─────────────────────────────────────────────────────────────┘

CONSISTENCY CHECK:
┌─────────────────────────────────────────────────────────────┐
│ Answer Position       │ Counterclaim Position │ Consistent? │
├─────────────────────────────────────────────────────────────┤
│ Deny contract existed │ Claim breach of same  │ ✗ CONFLICT  │
│ Deny performance due  │ Claim offset for work │ ✓ OK        │
└─────────────────────────────────────────────────────────────┘
═══════════════════════════════════════════════════════════════
```

---

### STEP 2 — Element Coverage

**For each claim, produce**:
```
CLAIM: [Name]
ASSERTING: [Party] against [Party]

┌─────────┬────────────────────┬────────────────┬────────────────┬────────┐
│ Element │ Allegation         │ Paragraph(s)   │ Missing Facts  │ Risk   │
├─────────┼────────────────────┼────────────────┼────────────────┼────────┤
│ 1       │ [What we allege]   │ CC ¶¶ X-Y      │ [Gaps]         │ L/M/H  │
│ 2       │ [What we allege]   │ CC ¶¶ X-Y      │ [Gaps]         │ L/M/H  │
└─────────┴────────────────────┴────────────────┴────────────────┴────────┘
```

---

### STEP 3 — Draft Pleading

**Structure for Counterclaim**:
```
              COUNTERCLAIM

     Counter-Plaintiff [NAME] alleges against Counter-Defendant
[NAME] as follows:

                    I. PARTIES

CC ¶ 1.  Counter-Plaintiff [identification — may incorporate from Answer]

CC ¶ 2.  Counter-Defendant [identification]

              II. JURISDICTION AND VENUE

CC ¶ 3.  [If compulsory: This Court has jurisdiction over this
          counterclaim as it arises from the same transaction or
          occurrence as Plaintiff's claims.]

         [If permissive: This Court has jurisdiction because...]

              III. GENERAL ALLEGATIONS

[Numbered paragraphs with facts supporting counterclaim]
[May incorporate by reference from Answer where appropriate]

         IV. FIRST CAUSE OF ACTION FOR COUNTERCLAIM
                   [Claim Name]

CC ¶ X.  Counter-Plaintiff incorporates the foregoing paragraphs
         as though fully set forth herein.

[Element-by-element allegations]

CC ¶ Y.  As a direct and proximate result, Counter-Plaintiff has
         suffered damages in an amount to be proven at trial.

              V. PRAYER FOR RELIEF

     WHEREFORE, Counter-Plaintiff prays for judgment against
Counter-Defendant as follows:

     1. For compensatory damages according to proof;
     2. For [offset against any judgment for Plaintiff];
     3. For costs of suit;
     4. For such other relief as the Court deems just.
```

**For Crossclaims and Third-Party Claims**: Adapt structure with appropriate designations and jurisdictional allegations.

---

### STEP 4 — Dependency Checklist

**Required output**:
```
═══════════════════════════════════════════════════════════════
DEPENDENCY CHECKLIST
═══════════════════════════════════════════════════════════════

REQUIRED PARTIES:
☐ [Party name] — Status: [In case / Must add / Must serve]
☐ [Party name] — Status: [In case / Must add / Must serve]

REQUIRED ALLEGATIONS:
☐ [Allegation type] — Present in CC ¶ [X]
☐ Notice requirements — [Addressed / CHECK jurisdiction]
☐ Contract terms — [Incorporated / Need to attach]
☐ Agency allegations — [Present if needed]

EXHIBITS/DOCUMENTS:
┌─────────────────────┬────────────────────┬─────────────────────┐
│ Document            │ Status             │ Action Required     │
├─────────────────────┼────────────────────┼─────────────────────┤
│ [Contract]          │ Attached to Answer │ Reference           │
│ [Invoices]          │ Not attached       │ Obtain and attach   │
└─────────────────────┴────────────────────┴─────────────────────┘

TIMING CONSTRAINTS:
☐ [CHECK: deadline to file third-party claim]
☐ [CHECK: leave of court required?]
☐ [CHECK: service requirements for new parties]

PROCEDURAL REQUIREMENTS:
☐ [CHECK: separate summons needed?]
☐ [CHECK: filing fee for added parties?]
☐ [CHECK: removal implications?]
═══════════════════════════════════════════════════════════════
```

---

### STEP 5 — Integration Instructions

**Output**:
```
INTEGRATION WITH ANSWER

OPTION A: Combined Pleading
- File as "ANSWER, AFFIRMATIVE DEFENSES, AND COUNTERCLAIM"
- Counterclaim follows after affirmative defenses
- Use separate numbering: CC ¶ 1, CC ¶ 2, etc.

OPTION B: Separate Filing
- File counterclaim separately
- Reference answer: "As alleged in Defendant's Answer filed [date]..."

INCORPORATION BY REFERENCE:
- CC ¶ 1 may incorporate Answer ¶¶ 1-5 (party allegations)
- Avoid incorporating denied facts

PARAGRAPH NUMBERING SCHEME:
- Answer paragraphs: ¶ 1, ¶ 2...
- Counterclaim paragraphs: CC ¶ 1, CC ¶ 2...
- [Or: continuous numbering if required by local rules]
```

---

## QC Checks

```
┌────────────────────────────────────┬──────────────────────────────────┐
│ Check                              │ Status                           │
├────────────────────────────────────┼──────────────────────────────────┤
│ Party alignment clear              │ ☐                                │
│ No contradictions with answer      │ ☐                                │
│ Element coverage complete          │ ☐                                │
│ Damages tied to conduct            │ ☐                                │
│ Procedural requirements flagged    │ ☐                                │
│ Integration instructions provided  │ ☐                                │
│ Dependency checklist complete      │ ☐                                │
└────────────────────────────────────┴──────────────────────────────────┘
```

---

## Output Checklist

Before delivering:
- [ ] Party alignment analysis complete
- [ ] Element coverage for each claim
- [ ] No contradictions with answer positions
- [ ] Proper party designations used
- [ ] Dependency checklist with all items
- [ ] Integration instructions provided
- [ ] Procedural requirements flagged as jurisdiction-dependent
