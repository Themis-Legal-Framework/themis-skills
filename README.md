# Themis Skills: Litigation Pleadings

A skill stack for drafting civil litigation pleadings with AI. Built for the [Themis Legal Framework](https://github.com/Themis-Legal-Framework/themis-framework).

## Design Philosophy

These skills are built on four core truths:

### 1. Expertise Transfer, Not Instructions

Each skill embodies how an expert litigator thinks—not a checklist of steps to follow. When you invoke `draft-complaint`, you get a senior litigation partner who knows what matters: elements, gaps, defenses, and how to tell the story.

### 2. Flow, Not Friction

Skills produce output. A complaint. An answer. A prioritized fix list. Not memos about what they might produce, not tables asking for approval, not intermediate documents that slow you down.

### 3. Voice Matches Domain

These skills sound like litigators, not documentation. Direct. Practical. Every sentence earns its place.

### 4. Focused Beats Comprehensive

Constraints are explicit and minimal. No 50-item checklists. No verbose procedures. The skills do what matters and skip what doesn't.

## The Skills

```
Core Workflow
├── litigation-drafting-core     # Universal drafting workflow
└── pleadings-core               # Foundation for all pleadings

Drafting Skills
├── draft-complaint              # Complaints that survive dismissal
├── draft-answer-and-defenses    # Answers that protect your client
├── draft-counterclaims-...      # Offensive claims in defensive pleadings
└── draft-amended-pleading       # Amendments that cure defects

Support Skills
├── claims-and-elements-builder  # Element mapping before you draft
├── convert-facts-to-...         # Raw facts → numbered paragraphs
├── exhibit-and-attachment-plan  # What to attach, what to leave out
└── pleading-qc-and-risk-audit   # Find weaknesses before they do

Overlays
├── overlay-jurisdiction-...     # Apply local court requirements
└── overlay-style-and-voice      # Apply consistent style
```

## Quick Start

### Draft a Complaint

```
Invoke: draft-complaint

Provide:
- Parties (names, roles, entity types)
- Facts (what happened, when)
- Claims (what causes of action)
- What you want (damages, injunction, etc.)

Get:
- The complaint, ready to file
- Flags for gaps and missing facts
- Element coverage built in
```

### Draft an Answer

```
Invoke: draft-answer-and-defenses

Provide:
- The complaint
- What's true, what's false, what's unknown
- Defenses to preserve

Get:
- Paragraph-by-paragraph responses
- Affirmative defenses (actually pleaded, not just labeled)
- No inadvertent admissions
```

### QC Before Filing

```
Invoke: pleading-qc-and-risk-audit

Provide:
- The draft pleading

Get:
- Prioritized fix list (must fix / should fix / polish)
- Attack surface analysis
- Client questions to resolve
```

## How the Skills Think

Each skill starts with a mental model. For example, `draft-answer-and-defenses`:

> **Read the complaint like opposing counsel will read your answer.**
>
> For each paragraph, ask:
> - Is this actually true?
> - Do I have the information to know?
> - Does admitting this hurt me later?
> - Is this a legal conclusion?

This isn't a checklist—it's how defense lawyers actually think.

## Constraints

Every skill enforces:

**Never invent:**
- Facts not provided
- Case citations (use `[CITE]` placeholders)
- Elements you're not sure about

**Always produce:**
- The actual document, not a memo about it
- Inline flags for problems: `[FLAG: description]`
- Specific questions for what's missing

## Jurisdiction + Style

Skills produce jurisdiction-agnostic output by default. Apply local requirements with overlays:

**Jurisdiction Pack** → Caption format, required sections, terminology, heightened pleading rules

**Style Pack** → Tone, defined terms, formatting conventions, boilerplate language

Templates in `overlay-jurisdiction-pleadings/references/` and `overlay-style-and-voice/references/`.

## File Structure

```
skills/
├── litigation-drafting-core/
│   └── SKILL.md
├── pleadings-core/
│   └── SKILL.md
├── claims-and-elements-builder/
│   └── SKILL.md
├── convert-facts-to-numbered-allegations/
│   └── SKILL.md
├── draft-complaint/
│   └── SKILL.md
├── draft-answer-and-defenses/
│   └── SKILL.md
├── draft-counterclaims-crossclaims-thirdparty/
│   └── SKILL.md
├── draft-amended-pleading/
│   └── SKILL.md
├── exhibit-and-attachment-plan/
│   └── SKILL.md
├── pleading-qc-and-risk-audit/
│   └── SKILL.md
├── overlay-jurisdiction-pleadings/
│   ├── SKILL.md
│   └── references/
│       └── JURISDICTION_PACK_TEMPLATE.md
└── overlay-style-and-voice/
    ├── SKILL.md
    └── references/
        └── STYLE_PACK_TEMPLATE.md
```

## Contributing

1. Fork the repository
2. Create jurisdiction packs for your courts
3. Submit style packs for common firm conventions
4. Open issues for workflow improvements

Jurisdiction pack contributions especially welcome.

## License

MIT License - see LICENSE file.

---

Built for the [Themis Legal Framework](https://github.com/Themis-Legal-Framework)
