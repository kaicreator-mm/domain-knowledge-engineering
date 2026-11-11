# Element Semantic Assurance Profile (SAP) Template

**Purpose:** define source-backed semantic assurance obligations owned by one exact Element revision.  
**Status:** candidate until the authorized independent review / domain oracle completes.  
**Do not use this template as evidence that the Element is qualified.**

## 1. Identity and ownership

- Domain ID / revision:
- Canonical KG revision:
- Blueprint revision:
- Element ID / revision:
- Element name:
- Parent Element:
- Element type: ROOT / DOMAIN / GLOBAL_SEMANTIC / OTHER
- Semantic owner:
- Product/task coverage:
- Profile revision:
- Status: CANDIDATE_NOT_QUALIFIED / REVIEW_REQUIRED / QUALIFIED_FOR_DECLARED_SCOPE / STALE / BLOCKED
- Exact Git commit / tree / relevant blob pins:

## 2. Responsibility and boundary

- Responsibility:
- Owned concepts / vocabulary:
- Owned Claims:
- Owned relations:
- Owned invariants / constraints:
- Referenced Elements:
- Applicable scope:
- Preconditions:
- Explicit exclusions:
- Out-of-scope neighboring concepts:
- Known ambiguity / unresolved owner decisions:

## 3. Source and Claim provenance

For each Claim, record:

| Claim ID | Normalized assertion | Source ID + exact locator | Source revision/hash | Scope/applicability | Epistemic state | Counterevidence / conflict |
|---|---|---|---|---|---|---|
| CLAIM-... | ... | ... | ... | ... | ... | ... |

Separate source statements, DKE interpretations, derived inferences, implementation observations, and runtime observations. Derived Claims must identify premises and inference rules.

## 4. Relations and global constraints

| Relation / invariant ID | Meaning and direction | Owner Element | Referenced Elements | Source/evidence | Scope | Violation / UNKNOWN behavior |
|---|---|---|---|---|---|---|
| REL-... | ... | ... | ... | ... | ... | ... |

Explicitly state whether the relation belongs to the semantic graph, decomposition hierarchy, or static executable dependency DAG. Do not infer executable dependency or permission from semantic relationships.

## 5. Competency Questions (CQ)

| CQ ID | Question | Expected POSITIVE | Expected NEGATIVE | Boundary | Conflict | UNKNOWN | Outdated evidence |
|---|---|---|---|---|---|---|---|
| CQ-... | ... | ... | ... | ... | ... | ... | ... |

For each answer, cite source and oracle. If evidence cannot decide, expected result must be UNKNOWN rather than a guessed answer.

## 6. Verification obligations

| Obligation ID | Property / invariant | Oracle type and authority | Fixture/source pins | Positive cases | Negative/adversarial cases | Result |
|---|---|---|---|---|---|---|
| SAP-... | ... | ... | ... | ... | ... | NOT_RUN |

Include as relevant:

- schema and reference integrity;
- source provenance and source-version applicability;
- semantic interpretation and scope;
- ownership and cross-Element closure;
- relation constraints and graph invariants;
- positive, negative, boundary, conflict, UNKNOWN, and outdated evidence;
- fabricated source/citation, source substitution, stale profile, and invalid relation attacks;
- parent/global composition (child PASS does not imply parent PASS);
- changed-source and changed-assumption invalidation.

Structural validation, source parsing, hosted logic execution, native tests, and independent semantic review are distinct evidence types.

## 7. AOT / Runtime boundary

**AOT-eligible stable knowledge:**
- source-backed semantics and rules:
- platform/version applicability:
- preconditions / refusal conditions:
- risk classification:
- verification and recovery policy:
- source revision and qualification pins:

**Runtime-only facts (must be re-observed at point of use):**
- live state:
- exact target identity:
- current permissions / ACL / privilege:
- user intent / approval:
- current permit / policy / provider trust:
- execution journal / receipt / postcondition:

Confirm explicitly: AOT does not contain live machine state, reusable approval, permit, or execution authority.

## 8. Cross-Element and parent composition

- Required neighboring Elements:
- Cross-Element relations:
- Global semantic Element dependencies:
- Static dependency DAG edges (if any):
- Composition invariants:
- Parent-level negative cases:
- Parent-level UNKNOWN cases:
- Change-impact edges and invalidation triggers:

## 9. Independent review and qualification

- Stage-0 source manifest revision:
- Independent Reviewer:
- Reviewer independence statement:
- Exact candidate HEAD/tree:
- Review date:
- Findings by severity:
- UNKNOWN / EXCLUDED:
- Required Source Owner / domain-expert decisions:
- Repair revision(s):
- Exact-SHA re-review:
- Final decision and declared scope:
- Qualification expiry / requalification triggers:

Builder and Repairer cannot sign the independent PASS. If an owner/domain oracle is required and absent, preserve the qualification gap.

## 10. Change and invalidation history

| Change ID | Source / assumption / scope changed | Before → after revision | Directly affected Claims/Elements | Transitive/global impact | Revalidation performed | Qualification result |
|---|---|---|---|---|---|---|
| CHANGE-... | ... | ... | ... | ... | ... | ... |

Impact must be derived from the actual versioned graph/Blueprint dependencies. Hypothetical mutation tests must be labeled hypothetical and must not be represented as actual upstream source releases.

## 11. Final state

- [ ] Candidate only; no qualification claimed.
- [ ] Source traceability checked.
- [ ] Semantic ownership checked.
- [ ] CQ and verification obligations complete.
- [ ] Independent source-first review complete.
- [ ] Required Owner/domain-oracle decisions complete.
- [ ] Parent/global composition complete.
- [ ] Source evolution / invalidation checked.
- [ ] Qualified only for the explicitly declared scope and revision.

**Final status:**  
**Scope covered:**  
**Remaining UNKNOWN / CONFLICT / EXCLUDED:**  
**Evidence links:**
