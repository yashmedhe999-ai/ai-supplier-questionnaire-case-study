# Product brief: evidence-backed questionnaire drafting

**Status:** Illustrative portfolio reconstruction. **Audience:** Product, design, engineering, security, supplier operations.

## Opportunity

Suppliers often repeat the same control descriptions across questionnaires. They have evidence documents, but must locate relevant passages, translate them into the questionnaire's wording, and check that the answer remains accurate. Reviewers need to understand whether an answer is supported and current.

## Users and jobs

| User | Job to be done | Failure to avoid |
| --- | --- | --- |
| Supplier respondent | Draft accurate answers from approved evidence quickly | Submitting a convincing but unsupported answer |
| Supplier approver | Confirm the final response represents company practice | Silent submission of unreviewed text |
| Risk reviewer | Verify answer and evidence with minimal back-and-forth | Losing provenance or overlooking a conflict |

## Product goal

Reduce avoidable document lookup and rework while preserving human accountability and an auditable evidence trail.

## Scope for a first useful release

1. Upload approved PDF documents, with clear status if a file cannot be parsed.
2. Propose answers only when a relevant passage is found; display the quoted source location and document name.
3. Show a calibrated uncertainty label (for example, `Review carefully`) rather than implying certainty from a raw score alone.
4. Let suppliers edit, reject, or replace suggestions; require an explicit review action before submission.
5. Record source, final answer, reviewer action, and time of change in the audit trail.
6. Route missing, stale, or contradictory evidence to manual review.

## Outside this illustrative release

Automatic attestation without a supplier review, inventing answers from general knowledge, and treating a model's confidence score as proof of compliance.

## Key edge cases

- Question says `MFA`; policy says `multi-factor authentication`: normalize the acronym, then still verify scope.
- Policy states MFA for administrators only; question asks about all users: flag a scope mismatch.
- Two documents conflict or have different effective dates: present both and require manual review.
- Upload is unreadable or has no relevant passage: leave answer blank and explain why.

## Launch checks

Use a reviewed set of representative, permitted documents and questions. Verify citations resolve to the intended passage, test scope-mismatch examples, and confirm that no unreviewed suggestions can be submitted. See [measurement plan](measurement-plan.md).

## Open questions

- What document freshness threshold should trigger a warning?
- Should approvers see the original suggested text after a supplier edits it?
- What is the escalation path for contradicting evidence?
