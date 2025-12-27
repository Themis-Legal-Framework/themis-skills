---
name: draft-complaint
description: Draft a civil complaint from a fact packet: parties/capacities, jurisdiction/venue placeholders, general allegations, claim counts with element coverage, and remedies/prayer, with a pleading-risk QC report.
metadata:
  short-description: Complaint drafting with element coverage + QC
---

# Draft Complaint

## Inputs (must ask)
1) Parties (names, entity types, roles, capacities)
2) Forum (if known): jurisdiction + venue + court level
3) Claims to plead (list)
4) Core facts (chronology + key docs)
5) Damages/remedies sought (types + rough amounts if known)
6) Any pre-suit steps taken (demands/notices/exhaustion), if applicable
7) Known vulnerabilities (limitations, contract terms, disclaimers, reliance issues, immunities)
8) Tone preference (neutral vs assertive) + length preference

## Workflow
### Step 1 — Strategy memo (short)
- Theme and theory of the case
- Claim list + element coverage risks
- Defensive risks and how we plead around them (without over-pleading)

### Step 2 — Element coverage table
- Invoke `claims-and-elements-builder` logic:
  - element → allegations → missing facts

### Step 3 — Draft structure (default)
A) Caption block (placeholder)
B) Parties and capacities
C) Jurisdiction/venue (placeholders if unknown)
D) General allegations (chronological)
E) Claim counts (each: incorporate → factual allegations → elements as ultimate facts)
F) Damages and remedies
G) Prayer for relief
H) Jury demand (if requested/appropriate as a placeholder)

### Step 4 — Produce deliverables
Deliver:
1) Draft complaint
2) Missing facts list (grouped by claim/element)
3) Pleading-risk QC report (see below)

## Pleading-risk QC report (required)
Include:
- Thin elements / conclusory allegations (list paragraphs)
- Timeline gaps
- Party/agency/alter ego (if implicated) needs
- Causation/damages linkage gaps
- Limitations/notice/exhaustion flags (placeholders)
- Exhibit/attachment decision risks
- "Overpleading" risks (unnecessary admissions; locking into a theory)

## Jurisdiction overlay instruction
If jurisdiction is known or user provides local rules/templates, invoke `overlay-jurisdiction-pleadings` to:
- apply caption/format requirements
- add required jurisdictional statements
- enforce heightened pleading rules (if any)
- add verification/statement requirements (if any)
