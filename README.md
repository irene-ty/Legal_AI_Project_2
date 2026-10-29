# Legal_AI_Project_2

# Bankruptcy Inheritance Issue Mapper

# URL: https://legalaiproject2-aztmb8iait9pixhx3kyget.streamlit.app/

A Streamlit prototype for **Australian legal practitioners** reviewing one inheritance interest in a personal bankruptcy matter. It extracts source-linked facts, builds a timeline, identifies preliminary issues and retrieves curated law to prepare an **internal working draft**.

The scope covers bankruptcy timing, inheritance interests and potential vesting in the trustee. It excludes final client advice and complex estate litigation.

## Four-step workflow

1. **Client Communications:** Enter your own OpenAI API key and select a model. Paste each email or SMS separately, with its date where known. **Create matter map** runs Calls 1–5: extraction, timeline construction, issue spotting, consistency review and consolidation.
2. **AI Matter Map:** Inspect the facts, original quotations, chronological timeline, preliminary issues and AI findings. Viewing results makes no additional AI call.
3. **Lawyer Review:** Verify sources, correct errors and supplement missing facts. Review affected timeline entries and outstanding items, enter initials and a review note, then approve the map.
4. **Legal Research & Working Notes:** Click **Run legal research**. RAG retrieves local law; Call 6 attempts preliminary analysis and Call 7 organises a draft. Download TXT notes and JSON source/review records.

Outputs are **Material Facts**, **Potential Legal Issues with Suggested Law Application**, and **Outstanding Information**. All require lawyer verification.

A complete run uses seven generative calls plus embedding requests; API charges apply. **New matter map** clears case inputs and results, retaining key/model settings.

## Test cases and expected performance

All cases are fictional. Click **New matter map** before each test, enter your own API key and select a model.

Copy only the message, clarification and review-note text into the matching fields. Do not paste table labels or test instructions. Communication dates use **YYYY-MM-DD**.

Step 2 is for inspection; no additional input is required. In Step 3, use **Edit facts, timeline, issues and information gaps** where corrections are needed. Keep client-reported information attributed: these fictional statements do not establish independent verification of documents.

### Case 1 — Simple inheritance

The father dies after reported discharge, and a single $8,000 gift is paid. The main facts are complete; the Step 3 confirmation is optional.

| Step / field | What to enter or do |
|---|---|
| **Step 1 · Communication 1** — Source type | Email |
| **Communication date** | 2025-06-23 |
| **Original text** | My debtor's petition was lodged and accepted on 12 February 2021. My statement of affairs was filed on the same day. My bankruptcy record lists 12 February 2021 as the commencement date and 13 February 2024 as the discharge date. No objection to discharge or extension is recorded.<br><br>My father died on 10 March 2025. His Will, signed on 2 July 2024, leaves me a fixed cash gift of $8,000 under clause 4. The gift has no stated condition, trust or life interest. There was no earlier contract, lifetime gift, transfer or trust arrangement relating to this $8,000. |
| **Step 1 · Communication 2** — Source type | Email |
| **Communication date** | 2025-06-24 |
| **Original text** | The estate was administered in Victoria. Probate was granted on 5 May 2025. The executor paid the full $8,000 into my bank account on 20 June 2025 and confirmed that estate administration was completed on that date.<br><br>This was the full and only payment under the gift, not an interim payment. No further inheritance payments are due. The dates and gift terms above are taken from my bankruptcy record, the Will, grant of probate, executor's final statement and bank statement. |
| **Step 1 · Action** | Click **Create matter map** and wait for Calls 1–5 to finish. |
| **Step 2 · Inspect** | Check the quotations and chronology: petition/statement of affairs → discharge → Will signing → death → probate → payment/administration completion. Dates, gift terms and payment status are already supplied. |
| **Step 3 · Additional lawyer-entered factual clarification** — Optional | For this fictional exercise, the client confirms that the recorded discharge date is 13 February 2024 and the probate grant date is 5 May 2025. The $8,000 was the full and only gift payment, credited on 20 June 2025. There is no earlier gift, transfer, contract or trust arrangement relating to this amount, and no further payment is due. |
| **Step 3 · Update affected entries** | No planned factual correction is needed. Compare the map with the communications, correct any extraction errors and mark answered questions accordingly. Retain genuine unresolved matters. |
| **Step 3 · Reviewer name or initials** | Enter your own name or initials, for example: TY |
| **Step 3 · Review note** | Fictional test only. All material factual dates, gift terms and payment status are supplied consistently. This note records the client's clarification; it does not claim independent verification of real documents. No legal conclusion about entitlement or vesting is approved. |
| **Step 3 · Approval** | After reviewing the map, tick **I have reviewed the sources, corrections and outstanding issues, and approve this map for research**, then click **Approve reviewed Matter Map**. |
| **Step 4 · Generate draft** | Click **Run legal research**. Inspect the working notes and download the TXT draft or JSON records if needed. |
| **Expected performance** | Produce a straightforward factual draft with no unanswered major factual question and minimal outstanding information, usually 0–1 consolidated record check. A source-supported **no apparent issue on supplied facts** result, or a specific legal-source limitation, is acceptable. Do not infer vesting merely because death or payment followed discharge, or treat Will signing alone as acquisition of an inheritance interest. Do not repeatedly request facts already supplied. |

### Case 2 — More complex timing

The mother dies during bankruptcy, and a single $12,000 gift is paid after discharge. Step 3 supplies the precise payment and administration-completion date.

| Step / field | What to enter or do |
|---|---|
| **Step 1 · Communication 1** — Source type | Email |
| **Communication date** | 2026-04-20 |
| **Original text** | My debtor's petition was lodged and accepted on 6 March 2023. My statement of affairs was filed on the same day. My bankruptcy record lists 6 March 2023 as the commencement date and 7 March 2026 as the discharge date. No objection to discharge or extension is recorded.<br><br>My mother died on 10 November 2024. Her Will leaves me a fixed cash gift of $12,000, with no stated condition, trust or life interest. Probate was granted on 20 February 2025, and the estate was administered in Victoria. |
| **Step 1 · Communication 2** — Source type | Email |
| **Communication date** | 2026-04-21 |
| **Original text** | The executor paid the full $12,000 in April 2026, after my discharge. I need to check my bank statement for the exact payment day. The executor confirmed that administration was completed when this payment was made. It was the full and only payment, and no further inheritance payments are due.<br><br>I thought payment after discharge meant I could keep the money. There is no reported estate dispute or creditor claim, and there was no earlier lifetime gift, transfer or trust arrangement for me. |
| **Step 1 · Action** | Click **Create matter map** and wait for Calls 1–5 to finish. |
| **Step 2 · Inspect** | Check that death precedes reported discharge and payment follows it. The exact April 2026 payment day is initially unknown. The client's belief about keeping the money must remain a belief, not an established legal rule. |
| **Step 3 · Additional lawyer-entered factual clarification** | I checked my bank statement: the full $12,000 was credited on 15 April 2026. The executor's final statement also records 15 April 2026 as the date of the final and only payment and completion of estate administration. No further payment is due. My bankruptcy record confirms the reported discharge date of 7 March 2026, with no extension recorded. |
| **Step 3 · Add the clarification** | Paste the supplied follow-up response into **Additional lawyer-entered factual clarification (optional)**. Then expand **Edit facts, timeline, issues and information gaps** to check the existing records. |
| **Step 3 · Update facts and timeline** | In **Facts**, update the payment and administration-completion dates to **15 April 2026**, where applicable. In **Timeline events and dates**, update the corresponding events: `date_text` = `15 April 2026`, `date_iso` = `2026-04-15`, `date_precision` = `exact`, and `status` = `reported`. Preserve existing IDs and source references. Click outside each edited cell to finish the edit. |
| **Step 3 · Review outstanding items** | Scroll the **Issues** table horizontally to inspect `unknown_facts` and `research_questions`. Then check **both** text boxes below the table: **Conflicts and their resolution/status** and **Missing information / questions**. After adding the clarification confirming **15 April 2026**, remove any outdated statement that the exact payment or administration-completion date is unknown **from every field in which it appears, including both text boxes**. Updating the facts and timeline does not necessarily remove these older statements automatically. If an entry also contains an unresolved legal question, retain that question in `research_questions` while removing the resolved date-gap wording. Leave empty fields empty, and preserve unrelated outstanding items, including any check of the statutory bankruptcy commencement date. |
| **Step 3 · Reviewer name or initials** | Enter your own name or initials, for example: TY |
| **Step 3 · Review note** | Fictional test only. The precise payment and administration-completion date has been supplied by the client. Keep that attribution and update the previously approximate April 2026 entries. The client's belief about keeping the money is not adopted as a legal conclusion. |
| **Step 3 · Approval** | After reviewing the map, tick **I have reviewed the sources, corrections and outstanding issues, and approve this map for research**, then click **Approve reviewed Matter Map**. |
| **Step 4 · Generate draft** | Click **Run legal research**. Inspect the working notes and download the TXT draft or JSON records if needed. |
| **Expected performance** | Incorporate **15 April 2026** in the approved map and draft; no longer describe the payment day as unknown. Examine a **potential after-acquired-property issue**, subject to the supplied law and factual characterisation. Payment after discharge alone must not exclude it. Usually 1–2 targeted checks or research tasks may remain. Do not assume probate or receipt alone establishes when the interest arose, or give a definitive vesting conclusion. |

### Case 3 — Unrelated matter

An employment dispute concerns unpaid wages and dismissal, with no inheritance-related bankruptcy issue.

| Step / field | What to enter or do |
|---|---|
| **Step 1 · Communication 1** — Source type | Email |
| **Communication date** | 2026-09-21 |
| **Original text** | I work part-time at a cafe in Melbourne. My employer has not paid me for six hours of overtime worked last week. I asked for the payment and was then removed from next week's roster. I would like to know whether I can recover the unpaid wages. |
| **Step 1 · Communication 2** — Source type | SMS |
| **Communication date** | 2026-09-22 |
| **Original text** | The manager has now said that my employment has ended. I have my payslips, roster and the messages about the dismissal. Can a lawyer advise me about unpaid wages and dismissal? |
| **Step 1 · Action** | Click **Create matter map**. Expect the scope decision here. |
| **Step 2** | Not applicable. The workflow should already have stopped in Step 1. |
| **Step 3 · Clarification, reviewer and review note** | Not applicable. Leave these fields empty; no approval is needed. |
| **Step 4** | Not applicable. Do not run legal research or generate working notes. |
| **Expected performance** | Display **Not applicable / out of scope** in Step 1 after Call 1, with a brief explanation of the application's scope. Do not run Calls 2–7, legal retrieval or embeddings, or provide employment-law advice. Do not present the scope decision as an API/validation failure or request repeated retries. |

Outstanding-item counts are indicative, not pass/fail quotas. Genuine factual or source gaps must remain visible. Assess source fidelity, chronology, incorporation of clarification and support for legal applications, rather than expecting identical wording.

**Observed limitations:** Cases 1–2 generally demonstrated factual organisation and incorporation of clarification. Some legal applications remained unsupported or were withheld. The expectations above are test criteria, not claims that every task passed. Outputs vary; citation checks do not certify legal correctness.

## Legal knowledge base

`legal_sources/`, beside `home.py`, contains selected **Bankruptcy Act 1966 (Cth)** provisions and **AFSA guidance**, grouped into legislation, professional guidance and client guidance.

Guidance is not equivalent to legislation. Retrieval uses this collection; the app does not search the internet.

To update the collection, add or replace authoritative `.md` or `.txt` files containing exact legal text and section headings. Include this metadata at the beginning:

```yaml
---
source_id: LAW010
title: "Actual source title"
source_type: legislation
provision_or_pinpoint: "Exact section or pinpoint"
version_date: ""
---
```

Paste the legal text below the header. Use a unique `source_id`, the actual title and pinpoint, and the version date where known.

`source_type` accepts `legislation`, `case` or `guidance`. Files named `README.md` are excluded.

Commit the updated files to the repository, deploy and rebuild the index through Step 4's **Legal file format and index controls**. Embeddings use `text-embedding-3-large`. Source currency requires human checking.

## Confidentiality and responsible use

This prototype is intended for **internal practitioner use**, not direct client advice. That purpose does not make the hosted demonstration private or authenticated.

**Client names are not required.** Use labels such as Client A and Deceased B. Remove unnecessary identifiers, signatures, contact details and account details while preserving relevant dates and relationships. Omitting names does not guarantee anonymity.

Communications, derived facts and retrieval queries are sent to OpenAI when relevant functions run. `store=False` does not guarantee zero retention: see [OpenAI's API data controls](https://developers.openai.com/api/docs/guides/your-data).

Use fictional or appropriately de-identified data for demonstrations. Follow firm approval and confidentiality procedures before submitting real material.

Keep client data out of `legal_sources/` and public repositories. Protect downloaded TXT/JSON records. Clearing a matter does not delete downloads or provider records.

## Technologies Used

- **Python and Streamlit:** application logic, interactive forms and session state; deployed on Streamlit Community Cloud.
- **OpenAI Python SDK:** AI calls for factual extraction, review, legal analysis and working notes. Available model options are `gpt-4o-mini`, `gpt-4o` and `gpt-5-pro`, subject to API access.
- **OpenAI `text-embedding-3-large` and ChromaDB:** embeddings, vector storage and semantic retrieval of curated legal passages for RAG.
- **Pydantic and PyYAML:** checking structured data and reading legal-source metadata.
- **pytest (development):** automated tests of application logic and workflows using simulated API responses.

## Acknowledgements / References

The project author supplied the application requirements and legal task prompts. ChatGPT and Codex assisted with coding, debugging, test-case preparation and documentation. All test cases are fictional, and generated outputs require human review.

The curated legal collection draws on:

- [Bankruptcy Act 1966 (Cth)](https://www.legislation.gov.au/C1966A00033/latest/text), including s 5 (definition of property), ss 58, 115, 116, 149 and 149A.
- AFSA, [Treatment of property in bankruptcy](https://www.afsa.gov.au/professionals/resource-hub/practice-guidance/treatment-property-bankruptcy), including interests in deceased estates.
- AFSA, [Choses in action](https://www.afsa.gov.au/professionals/resource-hub/practice-guidance/choses-action).
- AFSA, [What happens to my money?](https://www.afsa.gov.au/i-cant-pay-my-debts/bankruptcy/consequences-bankruptcy/what-happens-my-money), including inheritance guidance.

AFSA materials are administrative guidance, not legislation or binding judicial authority. The application retrieves locally stored excerpts rather than live webpages; their version and currency require separate checking.