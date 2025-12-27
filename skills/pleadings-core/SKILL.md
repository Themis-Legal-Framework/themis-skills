---
name: pleadings-core
description: Draft or revise civil pleadings (complaints, answers, counterclaims, amended pleadings) using element mapping, allegation planning, and numbered-paragraph drafting with a pleading-risk QC pass.
metadata:
  short-description: Pleadings workflow + risk controls
---

# Pleadings Core

## Purpose
Provide a structured workflow for civil pleadings that ensures element coverage, factual precision, and defensive awareness.

---

## CRITICAL CONSTRAINTS

### Never Invent
- Elements of claims/defenses (use placeholders if not provided)
- Case citations or statutory references
- Facts not supplied by the user
- Procedural requirements for unknown jurisdictions

### Always Produce
1. Element coverage table
2. Draft pleading in numbered paragraphs
3. Missing facts question list
4. Pleading-risk QC report

---

## Input Collection

**Required** (STOP if not provided):
| Input | Description |
|-------|-------------|
| Pleading type | Complaint / answer / counterclaim / cross-complaint / amended |
| Parties | Names, entity types, capacities, roles |
| Claims OR defenses | List of causes of action or affirmative defenses |

**Strongly Preferred**:
| Input | Description | If Missing |
|-------|-------------|------------|
| Forum | Jurisdiction + venue + court | Use `[JURISDICTION]` placeholders |
| Fact packet | Chronology, documents, communications | Ask targeted questions |
| Remedies | Damages types, amounts, equitable relief | Use generic prayer |
| Weak points | Limitations, standing, notice, immunity | Flag as unknown risks |
| Exhibits | Contracts, policies, notices to attach | Note in exhibit plan |
| Style | Tone, length, detail level | Use neutral default |

---

## STEP 1 — Element Mapping

**Action**: Build element checklist + coverage table.

### 1.1 Element Checklist
For each claim or defense:
```
CLAIM: [Name]
Authority: [Citation or placeholder]

ELEMENTS:
  1. [Element 1]
  2. [Element 2]
  3. [Element 3]
  ...

If authority not provided:
  [ADD ELEMENTS: jurisdiction-specific for {claim type}]
```

### 1.2 Allegation Coverage Table
```
| Claim | Element | Paragraphs | Supporting Facts | Missing Facts | Risk |
|-------|---------|------------|------------------|---------------|------|
| Breach of Contract | 1. Contract existed | ¶¶ 10-12 | Written agreement dated 1/1/24 | — | Low |
| Breach of Contract | 2. Plaintiff performed | ¶¶ 13-15 | Delivered goods per Ex. B | Delivery confirmation | Med |
| Breach of Contract | 3. Defendant breached | ¶¶ 16-20 | Failed to pay | [CONFIRM: exact breach date] | Low |
| Breach of Contract | 4. Damages | ¶¶ 21-23 | $50,000 unpaid | Interest calculation | Med |
```

**Invoke** `claims-and-elements-builder` for complex multi-claim pleadings.

---

## STEP 2 — Allegation Planning

**Action**: Create section-by-section plan before drafting.

### Standard Pleading Structure
```
SECTION PLAN:

I. PARTIES (¶¶ 1-X)
   - Plaintiff: [name, capacity, residence/principal place]
   - Defendant: [name, capacity, residence/principal place]
   - [Additional parties]

II. JURISDICTION AND VENUE (¶¶ X-Y)
   - Subject matter: [basis or placeholder]
   - Personal: [basis or placeholder]
   - Venue: [basis or placeholder]

III. GENERAL ALLEGATIONS (¶¶ Y-Z)
   - Chronological fact narrative
   - Key documents referenced
   - [Timeline attached as working document]

IV. FIRST CAUSE OF ACTION: [Name] (¶¶ Z-A)
   - Incorporation by reference
   - Element-by-element allegations

V. [ADDITIONAL CAUSES OF ACTION]

VI. DAMAGES / REMEDIES (¶¶ B-C)
   - Compensatory: [types and basis]
   - Special: [if applicable + heightened pleading flag]
   - Punitive: [if applicable + heightened pleading flag]
   - Equitable: [specific relief sought]
   - Fees/costs: [basis]

VII. PRAYER FOR RELIEF

VIII. JURY DEMAND [if applicable]
```

### Heightened Pleading Flags
Mark where jurisdiction may require specificity:
```
[CHECK HEIGHTENED PLEADING: fraud — who/what/when/where/how]
[CHECK HEIGHTENED PLEADING: special damages — itemization required?]
[CHECK HEIGHTENED PLEADING: punitive damages — specific allegations?]
```

---

## STEP 3 — Drafting

**Action**: Draft in numbered paragraphs following these rules.

### Drafting Rules

| Rule | Implementation |
|------|----------------|
| One idea per paragraph | Each ¶ = one fact, one act, or one legal point |
| Define before use | "Plaintiff ACME CORP. ("ACME")" then use "ACME" |
| Facts over conclusions | Lead with conduct; legal labels follow |
| Temporal anchoring | Include date/timeframe for every event |
| Source references | "As set forth in Exhibit A..." or `[CITE]` |
| No overstatement | "Defendant knew" only if evidence supports actual knowledge |
| Minimize admissions | Avoid unnecessary concessions |

### Paragraph Template
```
¶ X. On [DATE], [ACTOR] [ACTION] [to/with/against] [OBJECT/RECIPIENT].
     [CONSEQUENCE or SIGNIFICANCE]. [DOCUMENT REFERENCE if applicable].
```

### Example
```
¶ 15. On January 15, 2024, Defendant sent Plaintiff an email stating that
      Defendant would not fulfill its remaining obligations under the
      Agreement. A true and correct copy of this email is attached hereto
      as Exhibit C and incorporated by reference.
```

---

## STEP 4 — QC Pass

**Action**: Complete all sections of the Pleading-Risk QC Report.

### 4.1 Element Coverage Gaps
```
| Claim/Defense | Element | Status | Fix |
|---------------|---------|--------|-----|
| Negligence | Duty | THIN | Add ¶ re: special relationship |
| Negligence | Breach | OK | — |
| Negligence | Causation | MISSING | [NEED FACTS: how breach caused harm] |
```

### 4.2 Timeline Integrity
```
| Event | Alleged Date | Paragraph | Consistent? |
|-------|--------------|-----------|-------------|
| Contract signed | 1/1/24 | ¶ 10 | ✓ |
| Breach occurred | 3/15/24 | ¶ 16 | ✓ |
| Breach discovered | 2/1/24 | ¶ 18 | ✗ CONFLICT — discovery before breach |
```

### 4.3 Identity Clarity
```
| Actor | First Defined | Used Consistently? |
|-------|---------------|-------------------|
| ACME Corp. | ¶ 1 ("ACME") | ✓ |
| John Smith | ¶ 3 ("Smith") | ✗ — called "Defendant" in ¶ 15 |
```

### 4.4 Remedy Alignment
```
| Remedy Sought | Factual Support | Paragraph | Gap? |
|---------------|-----------------|-----------|------|
| Lost profits | Sales projections | ¶¶ 22-23 | Need causation link |
| Specific performance | Unique goods | ¶ 24 | [CONFIRM: why unique] |
```

### 4.5 Defensive Risk Assessment
```
| Defense | Exposure | Paragraphs at Risk | Mitigation |
|---------|----------|-------------------|------------|
| Statute of limitations | Medium | ¶ 5 (discovery date) | Add discovery rule allegations |
| Standing | Low | ¶¶ 1-2 | — |
| Failure to mitigate | Medium | None | Add mitigation efforts |
| Preemption | Unknown | — | [CHECK: federal preemption?] |
```

### 4.6 Exhibit/Attachment Risks
```
| Document | Attached? | Risk | Recommendation |
|----------|-----------|------|----------------|
| Contract | Yes (Ex. A) | Adverse terms in ¶ 12 | Prepare response to MTD |
| Emails | No | Authenticity | Attach or describe precisely |
```

---

## Jurisdiction Customization

When forum is known, invoke `overlay-jurisdiction-pleadings` to apply:
- Caption block format
- Required sections (cover sheet, verification)
- Signature block requirements
- Local pleading standards
- Terminology (e.g., "petition" vs. "complaint")

---

## Output Checklist

Before delivering:
- [ ] Element coverage table complete
- [ ] All numbered paragraphs follow drafting rules
- [ ] No invented facts or authorities
- [ ] All placeholders clearly bracketed
- [ ] QC report includes all six sections
- [ ] Missing facts compiled as specific questions
