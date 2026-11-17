# Failure analysis and guardrails

This case study describes observed issues and the controls introduced in response. A written policy is not automatically proof that every portal honours it; implementation evidence and remaining limits are identified below.

| Observed failure | Change | Local evidence | Remaining limit |
| --- | --- | --- | --- |
| Work experience or field of study missing after resume upload | Review structured answers explicitly before submission | Workday and SuccessFactors review-blocker functions; corresponding tests | Custom portal layouts can require a new adapter |
| Normal browser opened instead of the dedicated session | Validate the exact user-data directory and ownership of the CDP endpoint | Dedicated Chrome launcher and browser-attachment checks | External manually opened links are outside this launcher |
| Manual completion reported as agent work | Store submission actor and require confirmation in the submitting run | Log fields for actor and same-run confirmation; provenance tests | Legacy logs require reconciliation before publishing totals |
| A retry encounters an existing application | Deduplicate by requisition/URL and confirmed history | Intake normalisation and confirmed-submission filtering | Cross-platform duplicates may have different identifiers |
| Job looks relevant but excludes sponsorship | Explicit eligibility checks before form entry | Sponsorship eligibility tests and package policy | Silence about sponsorship is not a promise of sponsorship |
| Alert messages read without all extracted roles being processed | Queue each lead or record a disposition; preserve incomplete checkpoint | Operating skill and intake workflow specification | Connector availability and audit completeness require live verification |
| Portal blocks on CAPTCHA or authentication | Save a precise blocker and retain the dedicated tab for human continuation | Browser blocker detection and outcome logging | No automated bypass; some applications remain incomplete |

## Engineering lesson

Separate intent, execution and evidence. A target such as ten daily applications describes intent. A browser interaction records an attempt. A confirmed, correctly attributed outcome is evidence. Conflating those states caused misleading reports and made recovery harder.

The next architectural improvement would be a single explicit state model with durable transitions, idempotency keys and a consistent evidence requirement across every portal adapter.
