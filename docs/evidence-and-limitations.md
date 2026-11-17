# Evidence and limitations

## Evidence reviewed for this showcase

- Python entry point, daily pipeline, intake and matching modules.
- Resume tailoring and cover-letter generation modules.
- Browser submission policy, form-answer engine and final-review functions.
- Dedicated browser launcher and operating instructions.
- Local test source covering eligibility, matching, intake, tailoring and browser policy.
- Private audit-log structure, including blocker statuses, actor and confirmation fields.

The files above remain private. This document describes their responsibilities without reproducing source or personal records.

## Illustrative tracker

**Synthetic examples only. These rows are not applications or results.**

| Example role | Match score | Package | State | Next action |
| --- | --- | --- | --- | --- |
| Data Analyst at Example A | 74/100 | Resume and cover letter prepared | Ready for review | Verify the final employer form |
| AI Engineer at Example B | 68/100 | Prepared | CAPTCHA blocked | Human verification |
| ML Engineer at Example C | 81/100 | Prepared | Agent submitted with same-run confirmation | Retain evidence and deduplicate |
| BI Analyst at Example D | 65/100 | Prepared | User submitted | Attribute completion to the user |

## Measures suitable for a future evaluation

- Unique qualifying roles retained after deduplication.
- Package completion rate among eligible roles.
- Structured-field completeness at final review.
- Confirmed submissions separated by actor.
- Blocker distribution by portal and stage.
- Duplicate prevention and retry behaviour.
- Document factuality checks against the verified profile.
- Time and cost per completed application against a recorded manual baseline.

No performance values are asserted for these measures in this showcase. Historical audit entries cannot be treated as a validated benchmark without cleaning and evidence reconciliation.

## Validation record

On 17 November 2026, the existing local suite was executed using `python -m unittest discover -s tests -v` from the private project environment. **All 54 tests passed.**

These tests cover local policy and transformation behaviour, including sponsorship conflicts, duplicate intake, freshness tiers, role matching, truthful tailoring, structured-field review and submission attribution. They do not measure live portal completion rates or the reliability of an unattended daily run. No live applications were submitted during this validation.
