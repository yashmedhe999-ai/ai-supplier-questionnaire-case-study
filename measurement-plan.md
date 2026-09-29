# Measurement plan

This is a proposed plan, not a report of actual company data.

## Primary outcome

**Median supplier time to complete a questionnaire**, measured from first open to supplier submission, excluding periods when the questionnaire is paused for an external dependency. Segment by questionnaire length and supplier type; compare to a comparable prelaunch baseline.

## Supporting measures

| Metric | Definition | Why it matters |
| --- | --- | --- |
| Suggestion coverage | Questions with a draft / eligible questions | Indicates where the workflow can help. |
| Evidence-supported acceptance | Accepted drafts with a valid cited passage / accepted drafts | Guards against plausible but ungrounded text. |
| Supplier edit rate | Suggested answers materially edited / suggested answers reviewed | Highlights quality or wording problems. |
| Reviewer clarification rate | Submitted answers sent back for clarification / submitted answers | Checks downstream quality. |
| Median reviewer time per item | Time spent in review / items reviewed | Tests whether provenance saves effort. |

## Guardrails and diagnostics

- **Critical unsupported answer rate:** A sampled review panel labels answers whose text is not supported by the displayed evidence. Investigate any critical instance before expanding use.
- **Citation accuracy:** Percentage of sampled citations that open the correct document and passage.
- **Scope mismatch rate:** How often a suggestion overgeneralizes a limited control (for example, administrators versus all users).
- **Evidence freshness:** Percentage of drafts referencing expired or superseded documents.

## Review method

1. Establish the baseline using comparable questionnaire cohorts and document volumes.
2. Sample accepted, edited, rejected, and manually answered questions; do not measure quality only on accepted suggestions.
3. Use independent reviewer labels for support, scope, and actionability; resolve disagreements before reporting.
4. Review outcomes weekly by question type and evidence document, then improve prompts, retrieval, or UX according to the failure mode.

**Interpretation:** A shorter turnaround is a win only when evidence quality and reviewer clarification do not deteriorate.
