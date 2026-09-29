# User stories and acceptance criteria

These stories are illustrative and use synthetic evidence.

## 1. Evidence-linked suggestion

**As a supplier respondent**, I want a suggested answer with its source passage so I can verify it before submitting.

**Acceptance criteria**

- Given a question with relevant uploaded evidence, when a suggestion is generated, then the UI displays the proposed answer, document name, passage, and source location.
- Clicking the citation opens the matching document location.
- If the passage does not support the answer's full scope, the system does not label the item ready to accept.
- No suggestion is submitted without an explicit supplier action.

## 2. Missing or conflicting evidence

**As a supplier respondent**, I want an explanation when the system cannot support an answer so I know what to review manually.

**Acceptance criteria**

- Given no relevant passage, the item displays `Evidence not found` and leaves the answer blank.
- Given passages that disagree, the item displays `Conflicting evidence` and shows both passages.
- The user can enter a manual answer and attach the relevant evidence.
- The audit trail distinguishes a manual answer from an AI suggestion.

## 3. Abbreviation mapping

**As a supplier respondent**, I want common acronyms mapped to their full terms so relevant policies are discoverable.

**Acceptance criteria**

- A question using `MFA` can match a passage using `multi-factor authentication`.
- The matched passage must still satisfy the control's population and timeframe; acronym matching alone cannot justify an answer.
- A change to the global abbreviation mapping can be tested against prior evaluated cases before release.

## 4. Reviewer inspection

**As a risk reviewer**, I want to see the final answer and evidence provenance so I can assess the submitted response.

**Acceptance criteria**

- The reviewer can see the final text, original cited evidence, supplier edits, and review status.
- If the supplier changes a suggested answer materially, the reviewer can distinguish the final text from the original suggestion.
- A missing or inaccessible citation is marked as an exception.
