---
name: litigation-drafting-core
description: Run the litigation drafting workflow (intake→strategy→outline→modular draft→QC) and produce a filing-ready draft package without inventing facts or legal authority.
metadata:
  short-description: Universal litigation drafting assembly line
---

# Litigation Drafting Core

## Purpose
Provide a repeatable drafting workflow for litigation documents. This skill is jurisdiction-agnostic and must defer to jurisdiction/venue-specific overlays when needed.

## Non-negotiables
- **Do not invent**: facts, record citations, case names, statutes, rules, quotes, or procedural requirements.
- If authority is not provided, use **placeholders** like: `[ADD AUTHORITY: jurisdiction-specific rule/case]`.
- If a fact is uncertain, label it: `[CONFIRM FACT]` or ask for clarification in a **Missing Inputs** list.
- The user is responsible for legal accuracy, filing compliance, and local rules.

## Step 0 — Intake Gate (ask first; proceed with assumptions only if the user explicitly says to)
Collect:
1) Document type (pleading, motion, discovery, trial paper, etc.)
2) Jurisdiction/venue (if known) + court level (trial/appellate) + case type
3) Role: moving/responding/amending (or plaintiff/defendant)
4) Deadlines + page/word limits + formatting constraints (if any)
5) Procedural posture (what's pending; what stage)
6) Source materials provided (pleadings, exhibits, correspondence, transcripts)
7) Goal (what the document must accomplish) + what "win" means
8) Risks/constraints (bad facts, sensitive facts, privilege concerns)

If key items are missing, continue but create a **Missing Inputs** list and mark any dependent sections with placeholders.

## Step 1 — Strategy Memo (deliverable #1)
Output a short memo with:
- Issues to be decided (or pleaded) in plain language
- Elements/burdens/standards **as placeholders** if not supplied
- Best themes (1–2) and top arguments (2–4)
- Anticipated counterarguments and responses
- What evidence/record/facts support each point (or what is missing)
- Practical remedies/relief (what to ask the court for, or what the pleading seeks)

## Step 2 — Outline (deliverable #2)
Provide a detailed outline:
- Section headings (and subheadings)
- For each section: required facts + where they come from + placeholders for authority
- Any required attachments/verification sections as placeholders if jurisdiction unknown

## Step 3 — Modular Drafting (deliverable #3)
Draft in modules; after each module, include a brief **QC note** identifying:
- Any assumptions made
- Any missing facts or authority
- Any internal inconsistencies detected

## Step 4 — QC Pass (deliverable #4)
Provide:
- **Factual integrity audit**: list every factual claim that needs confirmation
- **Authority audit**: list every authority used or placeholder needed
- **Compliance checklist** (jurisdiction-agnostic): deadlines, formatting, service, signatures, exhibits, proposed order (as applicable)
- **Risk audit**: overstatements, conclusory language, admissions, sanctions exposure, privilege concerns

## When to invoke overlays
If jurisdiction/venue requirements matter, invoke:
- `overlay-jurisdiction-pleadings` (for pleadings requirements, captions, required sections)
- `overlay-style-and-voice` (for firm voice/format conventions)
