# Themis Skills: Litigation Pleadings

A jurisdiction-agnostic skill stack for drafting civil litigation pleadings with AI assistance. Built for the [Themis Legal Framework](https://github.com/Themis-Legal-Framework/themis-framework).

## Overview

This skill stack provides structured workflows for drafting complaints, answers, counterclaims, amended pleadings, and related documents. Each skill enforces:

- **No hallucination**: Facts and authorities are never invented
- **Explicit placeholders**: Missing information is clearly marked
- **Element coverage**: Claims map to elements map to allegations
- **Risk awareness**: QC passes identify vulnerabilities before filing

## Quick Start

```
skills/
├── litigation-drafting-core/      # Master workflow (start here)
├── pleadings-core/                # Pleading-specific workflow
├── claims-and-elements-builder/   # Element mapping
├── convert-facts-to-numbered-allegations/
├── draft-complaint/
├── draft-answer-and-defenses/
├── draft-counterclaims-crossclaims-thirdparty/
├── draft-amended-pleading/
├── exhibit-and-attachment-plan/
├── pleading-qc-and-risk-audit/
├── overlay-jurisdiction-pleadings/  # + Jurisdiction Pack template
└── overlay-style-and-voice/         # + Style Pack template
```

## Skill Hierarchy

```
┌─────────────────────────────────┐
│   litigation-drafting-core      │  ← Universal workflow
└───────────────┬─────────────────┘
                │
┌───────────────▼─────────────────┐
│       pleadings-core            │  ← Pleading-specific workflow
└───────────────┬─────────────────┘
                │
    ┌───────────┼───────────┬───────────┬───────────┐
    ▼           ▼           ▼           ▼           ▼
┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐
│Complaint│ │Answer  │ │Counter-│ │Amended │ │QC/Audit│
│        │ │+Defense│ │claims  │ │Pleading│ │        │
└────────┘ └────────┘ └────────┘ └────────┘ └────────┘
                │
    ┌───────────┴───────────┐
    ▼                       ▼
┌────────────────┐  ┌────────────────┐
│ claims-and-    │  │ convert-facts- │
│ elements-      │  │ to-numbered-   │
│ builder        │  │ allegations    │
└────────────────┘  └────────────────┘

Overlays (apply to any output):
┌────────────────────────┐  ┌────────────────────────┐
│ overlay-jurisdiction-  │  │ overlay-style-and-     │
│ pleadings              │  │ voice                  │
└────────────────────────┘  └────────────────────────┘
```

## Usage

### 1. Starting a New Complaint

Invoke `draft-complaint` with:
- Party names and roles
- Core facts (chronology)
- Claims to assert
- Damages/remedies sought

The skill will produce:
1. Strategy memo
2. Element coverage table
3. Draft complaint (numbered paragraphs)
4. Missing facts list
5. Pleading-risk QC report

### 2. Drafting an Answer

Invoke `draft-answer-and-defenses` with:
- The complaint text
- Client's position (what's true/false/unknown)
- Affirmative defenses to assert

The skill will produce:
1. Paragraph-by-paragraph responses
2. Affirmative defenses
3. Admission-risk audit

### 3. Applying Jurisdiction Rules

Create a Jurisdiction Pack using the template at:
```
skills/overlay-jurisdiction-pleadings/references/JURISDICTION_PACK_TEMPLATE.md
```

Then invoke `overlay-jurisdiction-pleadings` to apply:
- Caption formatting
- Required sections
- Local terminology
- Verification requirements

### 4. QC Before Filing

Invoke `pleading-qc-and-risk-audit` on any draft to get:
- Top 10 fixes (ranked by impact)
- Element coverage gaps
- Attack points (limitations, standing, notice, etc.)
- Client questions to resolve

## Creating Jurisdiction Packs

Copy `JURISDICTION_PACK_TEMPLATE.md` and fill in:

1. **Identification**: Court, level, case types
2. **Caption Templates**: Complaint, answer, amended formats
3. **Required Components**: Cover sheets, verifications, signature blocks
4. **Pleading Standards**: General standard, heightened pleading triggers
5. **Formatting Defaults**: Margins, fonts, line spacing, page limits
6. **Local Practice Notes**: Common clerk rejections, pitfalls

Example packs (community contributions welcome):
- `jurisdiction-pack-california-superior.md`
- `jurisdiction-pack-federal-ndcal.md`
- `jurisdiction-pack-texas-state.md`

## Creating Style Packs

Copy `STYLE_PACK_TEMPLATE.md` and fill in:

1. **Tone**: Default voice, words to avoid
2. **Defined Terms**: Party naming conventions
3. **Structure**: Section headings, intro paragraphs
4. **Paragraph Rules**: Length, date/money formats
5. **Boilerplate**: Prayer format, jury demand, reservations

## Design Principles

### No Hallucination
Every skill enforces:
- Facts come from user input only
- Authorities come from user input or are marked `[ADD AUTHORITY]`
- Procedural requirements are jurisdiction-dependent placeholders

### Structured Output
Every skill produces:
- Clearly labeled deliverables
- Tabular formats for coverage/mapping
- Ranked/prioritized lists for action items

### Defense-Aware Drafting
Offensive pleadings anticipate:
- Motion to dismiss attack points
- Limitations/standing/notice defenses
- Element-by-element scrutiny

Defensive pleadings anticipate:
- Inadvertent admissions
- Waiver of defenses
- Inconsistent positions

## License

MIT License - see LICENSE file.

## Contributing

1. Fork the repository
2. Create jurisdiction packs for your courts
3. Submit style packs for common firm conventions
4. Open issues for workflow improvements

---

Built for the [Themis Legal Framework](https://github.com/Themis-Legal-Framework)
