---
name: litigation-drafting-core
description: Run the litigation drafting workflow (intake→strategy→outline→modular draft→QC) and produce a filing-ready draft package without inventing facts or legal authority.
metadata:
  short-description: Universal litigation drafting assembly line
---

# Litigation Drafting Core

## Purpose
Provide a repeatable, high-quality drafting workflow for litigation documents. This skill is jurisdiction-agnostic and defers to overlays for local requirements.

---

## CRITICAL CONSTRAINTS (enforce always)

### Never Invent
- **Facts**: Only use facts explicitly provided by the user
- **Authorities**: Only cite cases/statutes/rules provided by the user
- **Quotes**: Never fabricate quotations from any source
- **Procedural requirements**: Treat as jurisdiction-dependent unless specified

### Always Placeholder
When required information is missing, use explicit placeholders:
```
[ADD AUTHORITY: description of what's needed]
[CONFIRM FACT: specific question]
[LOCAL RULE: what requirement applies]
[CITE: record reference needed]
[DATE: approximate or unknown]
[AMOUNT: to be determined]
```

### User Responsibility
The user is responsible for: legal accuracy, filing compliance, local rules, ethical obligations, and final review.

---

## STEP 0 — Intake Gate

**Action**: Collect these inputs before drafting. If user says "proceed with assumptions," continue but track gaps.

| Category | What to Collect | If Missing |
|----------|-----------------|------------|
| Document type | Pleading / motion / discovery / trial paper | STOP - must clarify |
| Forum | Jurisdiction + venue + court level | Use placeholders |
| Role | Moving/responding/amending; plaintiff/defendant | STOP - must clarify |
| Deadlines | Filing deadline, page/word limits | Flag in compliance checklist |
| Posture | What's pending, procedural stage | Note assumptions |
| Materials | Pleadings, exhibits, correspondence provided | List what's available |
| Goal | What document must accomplish | STOP - must clarify |
| Risks | Bad facts, privilege concerns, sensitive issues | Create risk register |

**Output**: Intake summary table + Missing Inputs list (if any)

---

## STEP 1 — Strategy Memo

**Action**: Produce a focused strategy memo (1-2 pages max).

### Required Sections

#### 1.1 Issues
List each issue to be decided or pleaded:
```
ISSUE 1: [Plain language statement]
  - Burden: [Party] must show [standard]
  - Elements: [List or placeholder]
  - Our position: [1-2 sentences]
```

#### 1.2 Theme
State 1-2 unifying themes that tie the case together:
```
PRIMARY THEME: [One sentence the factfinder should remember]
SECONDARY THEME: [Optional supporting narrative]
```

#### 1.3 Top Arguments (rank ordered)
```
1. [Strongest argument] — supported by [fact/evidence]
2. [Second argument] — supported by [fact/evidence]
3. [Third argument] — supported by [fact/evidence]
```

#### 1.4 Anticipated Counterarguments
```
| Their Argument | Our Response | Strength |
|----------------|--------------|----------|
| [Argument 1]   | [Response]   | High/Med/Low |
```

#### 1.5 Evidence Map
```
| Point to Prove | Supporting Evidence | Gap? |
|----------------|---------------------|------|
| [Point 1]      | [Doc/testimony]     | Y/N  |
```

#### 1.6 Relief Sought
Specific, practical remedies with legal basis.

---

## STEP 2 — Outline

**Action**: Produce a detailed section-by-section outline.

### Format
```
I. [SECTION HEADING]
   A. [Subsection]
      - Required facts: [list]
      - Source: [where facts come from]
      - Authority: [cite or placeholder]
      - Attachments: [if any]
   B. [Subsection]
      ...

II. [NEXT SECTION]
   ...
```

### Required Elements
- Every section must identify its factual foundation
- Every legal assertion must have authority or `[ADD AUTHORITY]`
- Every exhibit/attachment must be listed with purpose

---

## STEP 3 — Modular Drafting

**Action**: Draft in discrete modules. After each module, include inline QC.

### Module Structure
```
=== MODULE: [Section Name] ===

[Draft content]

--- MODULE QC ---
Assumptions made: [list]
Missing facts: [list with specific questions]
Missing authority: [list]
Internal consistency: [OK / issues noted]
=================
```

### Drafting Rules
1. **One idea per paragraph** (for pleadings with numbered paragraphs)
2. **Define before using**: Full name → defined term → consistent use
3. **Facts before conclusions**: Lead with conduct, follow with legal significance
4. **Anchor in time**: Include dates or temporal markers
5. **Cite sources**: Exhibit references, record cites, or `[CITE]` placeholders

---

## STEP 4 — QC Pass

**Action**: Produce a comprehensive QC report with four audits.

### 4.1 Factual Integrity Audit
```
| Factual Claim | Paragraph | Source | Confirmed? |
|---------------|-----------|--------|------------|
| [Claim 1]     | ¶ 12      | Ex. A  | Yes        |
| [Claim 2]     | ¶ 15      | None   | [CONFIRM]  |
```

### 4.2 Authority Audit
```
| Legal Proposition | Paragraph | Authority | Status |
|-------------------|-----------|-----------|--------|
| [Proposition 1]   | ¶ 20      | Smith v. Jones | Cited |
| [Proposition 2]   | ¶ 25      | [ADD AUTHORITY] | Missing |
```

### 4.3 Compliance Checklist
```
| Requirement | Status | Notes |
|-------------|--------|-------|
| Deadline    | [date] | [days remaining] |
| Page limit  | [X/Y]  | [OK / over] |
| Formatting  | [spec] | [compliant?] |
| Signature   | —      | [placeholder] |
| Service     | —      | [requirements] |
| Exhibits    | [list] | [attached?] |
| Proposed order | —   | [required?] |
```

### 4.4 Risk Audit
```
| Risk Category | Specific Risk | Severity | Mitigation |
|---------------|---------------|----------|------------|
| Overstatement | ¶ 14 claims "knew" without evidence | High | Soften to "was aware or should have been aware" |
| Admission     | ¶ 8 concedes timing | Medium | Evaluate strategic value |
| Sanctions     | — | — | — |
| Privilege     | — | — | — |
```

---

## Overlay Invocation

When jurisdiction/venue requirements apply, invoke:

| Condition | Invoke | Purpose |
|-----------|--------|---------|
| Caption/format needed | `overlay-jurisdiction-pleadings` | Local formatting, required sections |
| Firm style applies | `overlay-style-and-voice` | Consistent voice, defined terms |

---

## Output Checklist

Before delivering, confirm:
- [ ] All four QC audits completed
- [ ] All placeholders clearly marked with brackets
- [ ] No invented facts, authorities, or quotes
- [ ] Missing Inputs list provided (if gaps exist)
- [ ] Deliverables labeled (Strategy Memo, Outline, Draft, QC Report)
