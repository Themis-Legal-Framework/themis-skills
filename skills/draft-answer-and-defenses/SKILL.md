---
name: draft-answer-and-defenses
description: Draft an answer responding paragraph-by-paragraph with admissions/denials/insufficient knowledge, plus affirmative defenses and preservation language, and a risk audit for inadvertent admissions.
metadata:
  short-description: Answer + defenses with admission-risk controls
---

# Draft Answer and Defenses

## Purpose
Produce a defensive pleading that responds precisely to each allegation, asserts applicable defenses, and avoids inadvertent admissions.

---

## CRITICAL CONSTRAINTS

### Never
- Admit facts without client confirmation
- Deny indisputably true facts (creates credibility issues)
- Plead privileged or work-product content
- Invent affirmative defense elements

### Always
- Respond to every numbered paragraph
- Use "lacks sufficient knowledge" when genuinely uncertain
- Include admission-risk audit before finalizing
- Preserve defenses even if not fully developed

---

## Input Collection

**STOP if not provided**:
| Input | Why Required |
|-------|--------------|
| Complaint text | Cannot respond to allegations |
| Client position | Cannot determine admit/deny without guidance |

**Strongly Preferred**:
| Input | Default if Missing |
|-------|-------------------|
| Affirmative defenses | List common categories; ask user to select |
| Counterclaim intent | Assume no; note if facts suggest claims |
| Jurisdiction | Use generic format; placeholder for local rules |
| Sensitive facts | Flag potential privilege issues |

---

## Workflow

### STEP 1 — Complaint Analysis

**Output**: Allegation-by-allegation analysis table

```
═══════════════════════════════════════════════════════════════
COMPLAINT ANALYSIS
═══════════════════════════════════════════════════════════════

PARAGRAPH-BY-PARAGRAPH ASSESSMENT:

┌──────┬─────────────────────────────────┬────────────┬─────────────────────────┐
│ ¶    │ Allegation Summary              │ Response   │ Notes/Risks             │
├──────┼─────────────────────────────────┼────────────┼─────────────────────────┤
│ 1    │ Plaintiff is a DE corp          │ ADMIT      │ Public record           │
│ 2    │ Defendant resides in LA         │ ADMIT      │ Undisputed              │
│ 3    │ Parties entered contract 1/1/24 │ ADMIT      │ Have signed copy        │
│ 4    │ Contract required X services    │ ADMIT/DENY │ Admit contract; deny scope │
│ 5    │ Plaintiff performed             │ DENY       │ [CONFIRM: nonperformance?] │
│ 6    │ Defendant breached              │ DENY       │ Legal conclusion        │
│ 7    │ Plaintiff suffered $X damages   │ DENY       │ Lack knowledge of amount │
└──────┴─────────────────────────────────┴────────────┴─────────────────────────┘

ISSUES REQUIRING CLIENT INPUT:
• ¶ 5: Did Plaintiff actually perform? Need docs to verify
• ¶ 4: Exact scope of services — review contract language

POTENTIAL ADMISSIONS TO AVOID:
• ¶ 4: Don't admit "required" if scope is disputed
• ¶ 7: Don't admit any damages amount
```

---

### STEP 2 — Draft Answer

**Structure**:

```
[CAPTION BLOCK — match complaint format]

              ANSWER TO COMPLAINT
              [AND AFFIRMATIVE DEFENSES]

     Defendant [NAME] answers the Complaint as follows:

              RESPONSES TO ALLEGATIONS

                    I. PARTIES

¶ 1.  [ADMIT/DENY/INSUFFICIENT KNOWLEDGE — match complaint ¶ 1]

¶ 2.  [Response to complaint ¶ 2]

[Continue for all paragraphs in complaint]

              II. JURISDICTION AND VENUE

¶ X.  [Response — typically admit or insufficient knowledge]

                III. GENERAL ALLEGATIONS

[Respond to each numbered paragraph]

        IV. RESPONSES TO FIRST CAUSE OF ACTION

[Respond to each paragraph in the cause of action]

[Continue for all causes of action]

              AFFIRMATIVE DEFENSES

                 FIRST AFFIRMATIVE DEFENSE
                   (Statute of Limitations)

     The Complaint, and each cause of action therein, is barred in
whole or in part by the applicable statute of limitations.
[ADD ELEMENTS: jurisdiction-specific limitations periods]

                SECOND AFFIRMATIVE DEFENSE
                      (Failure of Consideration)

     Plaintiff's claims are barred because [factual basis for defense].

[Continue for each affirmative defense]

              RESERVATION OF DEFENSES

     Defendant reserves the right to assert additional affirmative
defenses as discovery proceeds and additional facts become known.

              PRAYER FOR RELIEF

     WHEREFORE, Defendant prays for judgment as follows:

     1. That Plaintiff take nothing by way of the Complaint;

     2. That the Complaint be dismissed with prejudice;

     3. For costs of suit incurred herein;

     4. For attorneys' fees [if contractual/statutory basis];

     5. For such other and further relief as the Court deems just
        and proper.


DATED: [DATE]                    Respectfully submitted,

                                 [SIGNATURE BLOCK]
                                 Attorneys for Defendant
```

---

### STEP 3 — Response Formulations

**Use precise language**:

| Situation | Formulation |
|-----------|-------------|
| Undisputed fact | "Admits." |
| False allegation | "Denies." |
| Partially true | "Admits [specific portion]; denies the remainder." |
| Legal conclusion | "Paragraph X states a legal conclusion to which no response is required. To the extent a response is required, Defendant denies." |
| Unknown fact | "Lacks sufficient knowledge or information to admit or deny the allegations in Paragraph X and on that basis denies." |
| Document speaks | "The document referenced in Paragraph X speaks for itself. Defendant denies any allegations inconsistent with the document's terms." |

---

### STEP 4 — Affirmative Defenses

**If jurisdiction-specific elements not provided**:

```
AFFIRMATIVE DEFENSES MENU
[Select applicable defenses; provide supporting facts]

CONTRACT DEFENSES:
☐ Statute of limitations
☐ Failure of consideration
☐ Breach by plaintiff (unclean hands)
☐ Waiver
☐ Estoppel
☐ Modification
☐ Accord and satisfaction
☐ Impossibility/impracticability
☐ Frustration of purpose

TORT DEFENSES:
☐ Comparative/contributory negligence
☐ Assumption of risk
☐ Statute of limitations
☐ Statute of repose
☐ Immunity (specify type)
☐ Privilege (specify type)

PROCEDURAL DEFENSES:
☐ Lack of standing
☐ Failure to join necessary party
☐ Failure to exhaust administrative remedies
☐ Failure to comply with notice requirements
☐ Forum non conveniens

REMEDIAL DEFENSES:
☐ Failure to mitigate
☐ No damages / speculative damages
☐ Offset/setoff
```

**For each selected defense, request**:
- Key facts supporting the defense
- Relevant dates
- Documents that support it

---

### STEP 5 — Admission-Risk Audit

**Required output**:

```
═══════════════════════════════════════════════════════════════
ADMISSION-RISK AUDIT
═══════════════════════════════════════════════════════════════

1. RESPONSES REQUIRING CLIENT CONFIRMATION
┌──────┬─────────────────────────────────┬─────────────────────────┐
│ ¶    │ Proposed Response               │ What to Confirm         │
├──────┼─────────────────────────────────┼─────────────────────────┤
│ 5    │ Deny performance                │ Review delivery records │
│ 8    │ Admit contract execution        │ Verify signature        │
└──────┴─────────────────────────────────┴─────────────────────────┘

2. POTENTIAL DUTY/AGENCY ADMISSIONS
┌──────┬─────────────────────────────────┬─────────────────────────┐
│ ¶    │ Concern                         │ Recommendation          │
├──────┼─────────────────────────────────┼─────────────────────────┤
│ 3    │ Admitting agency relationship   │ Confirm scope of agency │
│ 12   │ Admitting duty of care          │ Use "denies" if disputed│
└──────┴─────────────────────────────────┴─────────────────────────┘

3. CONTRACT FORMATION ADMISSIONS
┌──────┬─────────────────────────────────┬─────────────────────────┐
│ ¶    │ What's Being Admitted           │ Impact                  │
├──────┼─────────────────────────────────┼─────────────────────────┤
│ 4    │ Contract existed                │ OK if undisputed        │
│ 6    │ Contract required X             │ RISK: locks in scope    │
└──────┴─────────────────────────────────┴─────────────────────────┘

4. NOTICE/KNOWLEDGE ADMISSIONS
┌──────┬─────────────────────────────────┬─────────────────────────┐
│ ¶    │ What's Alleged                  │ Response Risk           │
├──────┼─────────────────────────────────┼─────────────────────────┤
│ 15   │ "Defendant knew" X              │ Don't admit knowledge   │
│ 18   │ "Defendant was notified"        │ Verify notice receipt   │
└──────┴─────────────────────────────────┴─────────────────────────┘

5. DEFENSE-FACT INCONSISTENCIES
┌─────────────────────────────────┬─────────────────────────────────┐
│ Defense                         │ Conflicting Response            │
├─────────────────────────────────┼─────────────────────────────────┤
│ SOL (claims arose 2020)         │ ¶ 10: Admitting conduct in 2023│
│ No contract (defense)           │ ¶ 4: Admitting contract exists │
└─────────────────────────────────┴─────────────────────────────────┘

6. AFFIRMATIVE DEFENSES NEEDING FACTUAL SUPPORT
┌─────────────────────────────────┬─────────────────────────────────┐
│ Defense                         │ Facts Needed                    │
├─────────────────────────────────┼─────────────────────────────────┤
│ Failure to mitigate             │ What mitigation was available?  │
│ Waiver                          │ Specific waiver conduct/date    │
└─────────────────────────────────┴─────────────────────────────────┘

═══════════════════════════════════════════════════════════════
```

---

## Jurisdiction Overlay

When forum is known, invoke `overlay-jurisdiction-pleadings` to apply:
- General denial availability (some jurisdictions allow)
- Verification requirements
- Affirmative defense pleading standards
- Caption and formatting conventions

---

## Output Checklist

Before delivering:
- [ ] Every complaint paragraph addressed
- [ ] Response language precise (no ambiguous denials)
- [ ] Legal conclusions labeled as such
- [ ] Affirmative defenses listed with factual basis or placeholder
- [ ] Reservation of defenses included
- [ ] Admission-risk audit complete (all 6 sections)
- [ ] No privileged content pleaded
- [ ] Defense-response consistency verified
