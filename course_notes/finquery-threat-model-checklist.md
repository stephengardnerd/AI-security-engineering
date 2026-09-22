# FinQuery STRIDE-ML Exercise Checklist

Use this checklist while completing **Apply Threat Modeling with STRIDE-ML — Exercise: Threat Model FinQuery**. Check each item only after it has been completed and reviewed.

- [ ] Read the system context and name every component and trust boundary.
- [ ] Complete the Tampering table: identify who can write to S3 and what a replaced document does at the next sync.
- [ ] Complete the Information Disclosure table: analyze retrieval of an unauthorized document.
- [ ] Complete the Elevation of Privilege table: analyze a document carrying model-directed instructions.
- [ ] Rate likelihood and impact for each threat, with one sentence of reasoning for each rating.
- [ ] Choose one mitigation for each threat.
- [ ] Complete the Priority Ranking table and justify each position in one sentence.
- [ ] Answer the single-control question and defend the choice.
- [ ] Save the completed work as `starter/STRIDE_ML_COMPLETED.md` with placeholder text removed.

## Stretch challenges

- [ ] Add Spoofing, Repudiation, and Denial of Service tables for a complete six-category model.
- [ ] Write a one-paragraph launch recommendation for an engineering lead.

## Troubleshooting checks

- [ ] Make every threat concrete: name the actor, component, and outcome rather than repeating a category definition.
- [ ] Prefer one well-defined threat per required category over several vague threats.
- [ ] Justify likelihood by considering whether the attack needs special access or only an ordinary text input.
- [ ] Justify impact by considering whether the result is merely embarrassing or creates a regulatory or material business problem.

## Working priorities

1. Information Disclosure
2. Tampering
3. Elevation of Privilege

## Initial control choice

If only one control can ship first, prioritize identity-aware, document-level authorization at retrieval time.

## Progress log

Update the checkboxes above as each requirement is completed. Add short notes here when a decision needs to be revisited.

## Writing requirements

- Write in clear, human-readable prose that sounds like Stephen D. Gardner wrote it.
- Spell the author name **Stephen**, with “ph.”
- Do not use em dashes.
