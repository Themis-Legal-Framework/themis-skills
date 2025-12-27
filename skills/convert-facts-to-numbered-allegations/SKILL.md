---
name: convert-facts-to-numbered-allegations
description: Turn a fact chronology into litigation-ready numbered allegations with defined actors, dates, and document references, minimizing legal conclusions and flagging missing details.
metadata:
  short-description: Fact packet → numbered paragraphs
---

# Convert Facts to Numbered Allegations

## Purpose
Transform raw facts into litigation-ready numbered paragraphs that can be incorporated into any pleading.

---

## CRITICAL CONSTRAINTS

### Never Invent
- Dates not provided → use `[DATE]` or `[APPROXIMATE: timeframe]`
- Amounts not provided → use `[AMOUNT]`
- Actors unclear → use `[CONFIRM IDENTITY: who?]`
- Documents not provided → reference by description only

### Always Prefer
- **Facts over conclusions**: Describe conduct, not legal labels
- **Specificity over generality**: Names, dates, places, amounts
- **Documents over memory**: Tie allegations to exhibits where possible

---

## Input Collection

| Input | Required? | Format |
|-------|-----------|--------|
| Chronology/narrative | YES | Bullets, prose, or timeline |
| Parties list | YES | Names + roles |
| Key documents | Preferred | Titles, dates, excerpts |
| Amounts/dates | Preferred | For damages allegations |
| "Do not include" items | If any | Privacy, privilege, strategy |

---

## Output Deliverables

### 1. Defined Terms List

```
PARTIES:
• ACME Corporation → "ACME" (Plaintiff)
• John Smith → "Smith" (Defendant, CEO of XYZ)
• XYZ Inc. → "XYZ" (Defendant)

ENTITIES:
• Board of Directors of ACME → "the Board"

DOCUMENTS:
• Services Agreement dated January 1, 2024 → "the Agreement" (Exhibit A)
• Email from Smith dated March 15, 2024 → "the March 15 Email" (Exhibit B)
```

### 2. Numbered Allegations

**Format**: Chronological unless user requests topical organization.

**Paragraph Structure**:
```
¶ [#]. On [DATE], [ACTOR] [VERB] [OBJECT/ACTION]. [CONSEQUENCE]. [DOCUMENT REFERENCE].
```

**Example Output**:
```
GENERAL ALLEGATIONS

¶ 1.  Plaintiff ACME Corporation ("ACME") is a Delaware corporation with its
      principal place of business in San Francisco, California.

¶ 2.  Defendant John Smith ("Smith") is an individual residing in Los Angeles,
      California. At all relevant times, Smith served as Chief Executive
      Officer of Defendant XYZ Inc.

¶ 3.  Defendant XYZ Inc. ("XYZ") is a California corporation with its
      principal place of business in Los Angeles, California.

¶ 4.  On January 1, 2024, ACME and XYZ entered into a written Services
      Agreement (the "Agreement"). A true and correct copy of the Agreement
      is attached hereto as Exhibit A and incorporated by reference.

¶ 5.  Under the Agreement, XYZ agreed to provide software development
      services to ACME in exchange for monthly payments of $25,000.

¶ 6.  Paragraph 5.2 of the Agreement required XYZ to deliver a functional
      prototype by March 1, 2024.

¶ 7.  ACME performed all conditions precedent under the Agreement, including
      timely payment of all amounts due through February 2024.

¶ 8.  XYZ failed to deliver the prototype by March 1, 2024, or at any time
      thereafter.

¶ 9.  On March 15, 2024, Smith sent an email to ACME's CEO stating that XYZ
      "ichever" would not complete the project. A true and correct copy of the
      March 15 Email is attached hereto as Exhibit B.

¶ 10. As a direct result of XYZ's breach, ACME has suffered damages in an
      amount to be proven at trial, but not less than $150,000.
```

### 3. Document Reference Map

```
| Document | Exhibit | Referenced In | Purpose |
|----------|---------|---------------|---------|
| Services Agreement | A | ¶¶ 4-7 | Establishes contract terms |
| March 15 Email | B | ¶ 9 | Evidence of repudiation |
| Payment records | C | ¶ 7 | Proves performance |
| [Prototype specs] | — | ¶ 6 | [NOT YET OBTAINED] |
```

### 4. Missing Details List

```
QUESTIONS FOR CLIENT:

DATES:
• ¶ 7: Exact dates of payments in January and February 2024?
• ¶ 10: When did ACME first incur damages (mitigation timeline)?

AMOUNTS:
• ¶ 10: Breakdown of $150,000 damages figure?
• ¶ 10: Any consequential damages beyond direct payments?

IDENTITIES:
• ¶ 9: Who at ACME received the March 15 Email?
• ¶ 2: Smith's exact title — CEO or President?

DOCUMENTS:
• ¶ 6: Do we have the prototype specifications referenced in the Agreement?
• ¶ 7: Bank records or wire confirmations for payments?

EVENTS:
• Any communications between March 1-15, 2024?
• Did ACME send a cure notice? If so, when?
```

---

## Drafting Rules

### Rule 1: One Paragraph = One Idea
```
BAD:  ¶ 5. The parties entered into a contract on January 1, 2024, which
           required defendant to provide services, and defendant breached
           the contract by failing to perform, causing damages.

GOOD: ¶ 5. On January 1, 2024, the parties entered into the Agreement.
      ¶ 6. Under the Agreement, Defendant agreed to provide consulting services.
      ¶ 7. Defendant failed to provide the required services.
      ¶ 8. As a result, Plaintiff suffered damages.
```

### Rule 2: Anchor in Time
```
BAD:  ¶ 10. Defendant made false statements.

GOOD: ¶ 10. On March 15, 2024, Defendant stated in writing that the
            product was "fully tested and ready for deployment."
```

### Rule 3: Identify Actors Precisely
```
BAD:  ¶ 12. They failed to respond.

GOOD: ¶ 12. XYZ, through its CEO Smith, failed to respond to ACME's
            March 20, 2024 demand letter.
```

### Rule 4: Facts Before Conclusions
```
BAD:  ¶ 15. Defendant fraudulently induced Plaintiff to enter the contract.

GOOD: ¶ 15. Prior to executing the Agreement, Smith represented to ACME
            that XYZ had completed similar projects for three Fortune 500
            companies.
      ¶ 16. Smith knew this representation was false because XYZ had never
            performed work for any Fortune 500 company.
      ¶ 17. ACME relied on Smith's representation in deciding to execute
            the Agreement.
```

### Rule 5: Bracket Uncertainties
```
¶ 20. On [DATE: approximately late March 2024], ACME discovered that
      XYZ had [CONFIRM: abandoned the project / ceased work /
      reassigned personnel].
```

---

## QC Checklist

Before delivering:

| Check | Status |
|-------|--------|
| Defined terms used consistently throughout | ☐ |
| Dates in chronological order | ☐ |
| No "floating pronouns" (unclear "they/it/them") | ☐ |
| Every factual claim tied to source or bracketed | ☐ |
| Damages traceable to specific events | ☐ |
| No legal conclusions without factual foundation | ☐ |
| All missing details listed as specific questions | ☐ |
