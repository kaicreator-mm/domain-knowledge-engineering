# DKE Methodology 0.1.0

**Identifier:** DKE-METHOD-0.1.0-CANDIDATE  
**Status:** Draft candidate; not frozen as a universal standard  
**Purpose:** Define a repeatable, evidence-first method for turning a bounded domain problem into a semantically coherent, independently verifiable, evolution-aware knowledge model, and determine whether/how that knowledge can be safely functionized.

> DKE is successful when a real, authorized domain task is understood with traceable evidence and explicit limits—not when the repository contains the largest number of Claims, Elements, or generated documents.

## 1. Definition and outcome

Domain Knowledge Engineering (DKE) is the engineering discipline for discovering, acquiring, structuring, decomposing, assuring, and maintaining domain knowledge.

DKE must answer, in order:

1. **Demand:** Which real user, business, or product tasks require knowledge?
2. **Knowledge:** What concepts, facts, rules, relations, constraints, procedures, and uncertainty are necessary to perform those tasks correctly?
3. **Authority:** Which sources establish each assertion, for what scope and time/version?
4. **Structure:** How should the domain be represented as a canonical knowledge graph/corpus, Domain Blueprint, and recursively decomposed Elements?
5. **Assurance:** How can each Element and the composed domain be independently checked against original sources and explicit oracles?
6. **Evolution:** What becomes invalid when sources, assumptions, scope, or domain boundaries change?
7. **Feasibility:** Which knowledge can be explained, observed, planned, or implemented, and what evidence proves each level?
8. **Function closure:** If Product admits implementation, how does the knowledge support a Function/Pipeline whose effect and outcome are independently verified?

The default trace is:

```text
Product authority + bounded domain goal
  → user jobs / demand evidence
  → knowledge requirements
  → Stage-0 source and acceptance freeze
  → source-backed claims and canonical graph/corpus
  ↔ Domain Blueprint + recursive Element decomposition (DEDS)
  → Element SAP + cross-Element composition assurance
  → independent source-first review
  → source-change impact and qualification
  → implementation-feasibility assessment
  → Product admission + DIS Function/Pipeline/AOT
  → Runtime authorization, execution, postcondition verification and recovery
  → user-visible functional closure and evidence
```

This is a traceability path, not a promise that every domain must be implemented or that every Element must expose a Function.

## 2. Authority and ownership boundaries

| Concern | Primary owner | DKE rule |
|---|---|---|
| User problem, product promise, supported journey, risk appetite | Product Owner | DKE may analyze and propose; it cannot silently expand Product scope |
| Original source authority and domain truth | Source Owner / domain expert / authoritative publisher | DKE records provenance and unresolved adjudication; it cannot invent authority |
| Claims, vocabulary, relations, constraints, Elements, Blueprint, SAP | DKE | Own semantic model and evidence traceability |
| Function I/O, Pipeline, ECP, AOT Package and compatibility contract | DIS / relevant package authority | DKE supplies qualified knowledge; it does not redefine downstream ABI |
| Live device/application state, permissions, permits, effects, journaling, recovery | Runtime / Host | Never infer live state or execution permission from AOT knowledge |
| Independent semantic review and release/qualification decision | Authorized independent Reviewer / Owner | Builder or Repairer cannot self-issue independent PASS |

Keep the following distinctions explicit:

- **Knowledge truth is not Product admission.**
- **Product admission is not implementation.**
- **Implementation is not native-environment verification.**
- **A Function result is not proof of its postcondition.**
- **Semantic relationships do not grant execution permission.**
- **AOT compilation does not freeze volatile runtime facts or authorization.**

## 3. Phase 0 — Freeze the problem and acceptance authority

Before collecting candidate knowledge:

1. Identify the authoritative Product/L1 or equivalent requirement, its revision, status, and owner.
2. Record the bounded domain goal, intended consumers, supported tasks, exclusions, operating context, and known risk.
3. Identify the acceptance criteria already authorized by the owner. Separate them from proposed criteria and implementation ideas.
4. Pin the exact revision/SHA of relevant Product, standard, source manifest, original source files, code, and tests.
5. Establish a Stage-0 raw-source manifest: source identity, publisher/owner, immutable locator, revision/date, hash or Git Blob, retrieval method, scope, and known limitations.
6. Freeze the independent reviewer's initial source set and criteria before showing candidate output, Builder conclusions, historical review findings, or repair narratives.

### Stage-0 rules

- Start with original Product and original evidence, not the candidate model.
- Distinguish authoritative sources, secondary interpretations, implementation observations, test fixtures, and generated material.
- A test written by the Builder is evidence that the code behaves as tested, not evidence that the domain rule is true.
- Historical review and repair records are useful only after the independent baseline is frozen.
- A missing source, unavailable original, ambiguous version, or unsupported interpretation is recorded as UNKNOWN / NOT_AVAILABLE; never fill it with plausible prose.
- Do not broaden the task because a source or API happens to be available.

**Required outputs:** scope/authority record, acceptance matrix, Stage-0 raw-source manifest, exact revision pins, and unresolved-owner-decision list.

## 4. Phase 1 — Derive knowledge demand from real tasks

Do not begin with a list of technologies, APIs, documents, or ontology classes. Begin with user jobs and work backwards.

For each task, record:

- Job ID, actor, desired outcome, triggering situation, and observable success.
- Evidence that the task exists: frozen Product journey, owner request, observed workflow, support case, domain process, or other identified source.
- Product status: admitted, candidate, explicitly excluded, or unknown.
- Frequency/value/impact only when supported by evidence; otherwise UNKNOWN.
- Harm if knowledge is wrong, reversibility, affected assets, and required authority.
- Preconditions, environment, dependencies, exception paths, and user decisions.
- Required diagnosis, decision, operation, and postcondition verification.
- Knowledge gaps and unanswered owner questions.

### Demand classes

Use classes as a prioritization aid, not as an automatic admission mechanism:

- **D0 — Frozen Product-critical:** knowledge required for an already authorized Product journey.
- **D1 — High-value candidate:** plausible recurring/high-impact tasks proposed for future Product admission.
- **D2 — Specialist/low-frequency:** advanced, environment-specific, or expert tasks.
- **D3 — Boundary/excluded:** unsupported, unsafe, out-of-scope, non-applicable, or not worth implementing. Retain safety/refusal knowledge when needed.

Prioritize using evidence-backed user value, Product alignment, recurrence, harm if wrong, dependency leverage, verification feasibility, source maturity, and lifecycle cost. Do not prioritize merely because an API exists or an LLM can describe the topic.

### Knowledge requirement derivation

For every job, derive the minimum required:

1. Concepts and identities.
2. Facts and properties.
3. Preconditions and applicability.
4. Rules, decisions, and domain procedures.
5. Relations and cross-cutting constraints.
6. Positive, negative, boundary, conflict, UNKNOWN, and outdated-evidence cases.
7. Required evidence and independent verification oracle.
8. Runtime-only observations and authority requirements, if the task can cause effects.

**Required output:** a demand-to-knowledge matrix with explicit coverage gaps. See the matrix template in this repository.

## 5. Phase 2 — Acquire and model source-backed knowledge

### 5.1 Source selection and authority

For every source, record:

- Stable source ID and exact locator (URL, Git repository/path/commit/blob, document ID, standard section, dataset release, etc.).
- Issuer/publisher, authority type, jurisdiction/domain, publication/release date, effective interval, and revision.
- Retrieval date/method, content hash, and immutable snapshot when possible.
- What the source can establish and what it cannot establish.
- Applicability, exclusions, known conflicts, and whether it is normative, informative, observational, or merely a test fixture.

Do not treat a search result snippet, an LLM summary, an implementation comment, or a third-party mirror as equivalent to the original authoritative source.

### 5.2 Claim model

A semantic Claim should minimally carry:

- Stable Claim ID and normalized assertion.
- Subject, predicate, object/value, and typed qualifiers.
- Source references down to the smallest practical section/line/record/span.
- Source revision/hash and retrieval snapshot.
- Scope, preconditions, applicability, exclusions, jurisdiction/platform/version.
- Epistemic status (for example: asserted by source, observed, inferred, disputed, unknown, outdated); define the exact vocabulary per schema.
- Polarity and modality (required, permitted, prohibited, possible, conditional).
- Effective time / observed time when relevant.
- Confidence or evidence strength only when its semantics are defined; do not use an ungrounded numeric confidence as a substitute for provenance.
- Known counterevidence, conflicting Claims, and validation obligations.

Keep **source statement**, **DKE interpretation**, **derived inference**, and **runtime observation** distinguishable. Derived Claims must link to their premises and inference rule. A Claim without sufficient source authority remains candidate or UNKNOWN.

### 5.3 Relations and global constraints

- Define relation meaning, direction, domain/range, cardinality, scope, and whether it is normative or descriptive.
- Record inverse, transitive, symmetric, or other logical properties only when the source/ontology actually supports them.
- Avoid importing semantics from a similarly named relation in another domain.
- Every global invariant or cross-Element policy has an explicit owning Element, applicability, referenced Elements, evidence, violation cases, UNKNOWN behavior, and validation obligations.
- Unresolved ownership is a visible gap; it must not be hidden in free-text notes.

### 5.4 Knowledge graph / corpus

The canonical graph/corpus is the semantic source of truth. Blueprints, Element views, consumer selections, and AOT projections should be versioned and traceable projections/decision records—not independent, silently divergent copies.

Pin each graph revision to its source snapshot and generation/curation provenance. Preserve stable identities and change lineage.

## 6. Phase 3 — Build Domain Blueprint and decompose Elements (DEDS)

Blueprint and Element decomposition are created **during canonical knowledge-graph construction**, not postponed until a consumer asks for an AOT Package.

### 6.1 Three separate structures

Maintain three different structures:

1. **Decomposition/ownership hierarchy:** recursive Root → child Elements and explicit semantic/global Elements.
2. **Semantic graph:** concepts, Claims, relations, constraints, and cross-cutting relationships. Cycles may be semantically valid.
3. **Static executable dependency DAG:** only declared build-time/function dependencies. It must be acyclic when required by the downstream contract. A semantic edge does not become a Function dependency or permission.

Never collapse these structures into one tree or one DAG.

### 6.2 Element responsibilities

- **Root Element:** domain scope, goals, vocabulary, validity/coverage obligations, and composition boundary.
- **Child Elements:** cohesive bounded responsibilities, knowledge capabilities, processes, policies, or domain areas.
- **Global semantic Elements:** cross-cutting relations, invariants, policies, collaboration/coordination contracts, compatibility semantics, and composition obligations. They are first-class Elements, even when they expose zero Functions.
- A declarative Element with zero Functions still has verifiable semantic assertions and validation obligations.
- A Claim/fact does not automatically require one Element; a Function does not automatically require one Element.

### 6.3 Complementary decomposition heuristics

Use and reconcile, rather than mechanically equate:

1. Minimum cohesive, self-consistent, independently verifiable responsibility (primary).
2. DDD subdomain / Bounded Context / ubiquitous-language boundaries; Aggregates for consistency/invariant boundaries.
3. Information hiding, cohesion/coupling, and change-together analysis.
4. Business capability, process scenarios, and event discovery to expose missing responsibilities and collaboration paths.
5. Ontology/KG modularization to test semantic closure, ownership, overlapping terms, relation scopes, and global constraints.

A Bounded Context, microservice, Package, file, or API is not automatically an Element.

### 6.4 Split/merge decision record

For every consequential split or merge, record:

- Parent/child Element IDs, roles, ownership, and revision.
- Criterion and source/task evidence supporting the boundary.
- Alternatives considered and why they were rejected.
- Semantic content and invariants owned by each side.
- Cross-Element relations and global constraints.
- Candidate Functions (0..N), but no assumed execution permission.
- Independent verification boundary and composition tests.
- Coupling/change impact and expected maintenance cost.
- Assumptions, unknowns, conflicts, and owner decisions.
- Reversible decision lineage.

### 6.5 Stop conditions

There is no universal numeric threshold for Element size or recursion depth.

Split when responsibilities have independently changing semantics, distinct authority/applicability, separate verification oracles, or materially different consumers.

Merge when the proposed children cannot be independently understood or verified without extensive cross-coordination, share one inseparable invariant/authority boundary, or the split creates artificial indirection.

Stop when another split decreases cohesion or independent verifiability, or increases coordination/coupling more than it improves change isolation. Always test for both over-fragmentation and overloaded Elements.

### 6.6 Blueprint minimum inventory

A Blueprint candidate should identify:

- Domain ID/revision, scope, outcomes, consumers, and exclusions.
- Source snapshot and canonical graph revision.
- Vocabulary and scoped meanings.
- Root Element and recursive Element hierarchy.
- Each Element's responsibility, ownership, claims, relations, and constraints.
- First-class global semantic Elements and their cross-Element references.
- Separately derived static dependency DAG, if any.
- Task/capability/problem-class coverage and gaps.
- Split/merge rationale and alternatives.
- Element validation/SAP references.
- Independent critique and composition validation status.
- Conflicts, UNKNOWNs, stale evidence, and unresolved owner decisions.

## 7. Phase 4 — Semantic Assurance Profile (SAP) for every Element

Every Element candidate has its own first-class Semantic Assurance Profile. A global test bundle may supplement SAP but cannot replace per-Element ownership and obligations.

An SAP should bind to the exact Element revision and include:

1. Owned semantic Claims and source provenance.
2. Scope, applicability, exclusions, and preconditions.
3. Owned and referenced relations/global constraints.
4. CQ set and explicit expected answer/UNKNOWN semantics.
5. Verification oracle type and its authority/limitations.
6. Positive, negative, boundary, conflict, UNKNOWN, and outdated-evidence cases.
7. Schema/contract checks where applicable.
8. Cross-Element dependency/composition obligations.
9. Access, disclosure, and handling restrictions when relevant.
10. Exact fixture/source revisions and test digests.
11. Independent review and execution state.
12. Open findings and requalification triggers.

### CQ and test design

A CQ must not be only a positive happy-path question. Include:

- **POSITIVE:** supported by authoritative evidence.
- **NEGATIVE:** contradicted or explicitly prohibited by evidence.
- **BOUNDARY:** just inside/outside scope or applicability.
- **CONFLICT:** credible sources or Claims disagree.
- **UNKNOWN:** available evidence cannot decide.
- **OUTDATED:** formerly supported evidence is no longer current/applicable.

Add adversarial cases: missing source, wrong source version, fabricated citation, scope substitution, cross-Element ownership leak, invalid relation, stale SAP, changed assumptions, and misleading PASS receipts.

A test oracle must be appropriate to the claim. Structural schema checks cannot prove domain truth; LLM agreement cannot replace a domain expert or authoritative source; a source parser cannot adjudicate a disputed policy decision.

## 8. Phase 5 — Independent Source-First review and qualification

Use a genuinely independent Reviewer context, separate from Builder and Repairer.

### Required order

1. Reviewer reads frozen Product, Stage-0 manifest, original sources, and original acceptance authority.
2. Reviewer independently derives criteria and freezes Stage-0.
3. Only then Reviewer reads candidate Blueprint, graph, Elements, Claims, SAPs, generated tests, prior reviews, and repair records.
4. Reviewer traces candidate assertions back to original source bytes/records and independently challenges their meaning and scope.
5. Reviewer checks decomposition, ownership, relations, global invariants, CQ positive/negative/UNKNOWN coverage, SAP sufficiency, and composition.
6. Reviewer records exact candidate HEAD/tree/blob pins, findings, severity, evidence, UNKNOWN/EXCLUDED, and G1–G5 or project-defined gates.
7. Repairer fixes only confirmed findings; independent Reviewer reviews the new exact SHA. Repairer does not self-sign PASS.

### Qualification distinctions

Do not collapse these states:

- GENERATED
- STRUCTURALLY_VALID
- SOURCE_TRACEABLE
- SOURCE_REVIEWED
- SEMANTICALLY_REVIEWED
- SAP_COMPLETE
- INDEPENDENTLY_VALIDATED
- OWNER/DOMAIN_ORACLE_ATTESTED
- QUALIFIED_FOR_DECLARED_SCOPE
- SELECTED_BY_CONSUMER
- FUNCTIONIZED
- RUNTIME_VERIFIED

The exact state vocabulary and transition authority must be defined by the governing Product/standard. A checker PASS, test count, or two agreeing LLMs cannot skip a gate.

## 9. Phase 6 — Knowledge evolution and impact invalidation

Knowledge is versioned and evidence-dependent. A source update, scope change, new counterexample, changed domain boundary, or altered global invariant can invalidate downstream Claims, SAPs, Elements, Blueprint decisions, and consumer packages.

Required approach:

1. Detect changed source identity/revision/hash or changed interpretation.
2. Identify directly dependent Claims and Elements from explicit provenance edges.
3. Derive transitive impact through the actual versioned dependency/Blueprint graph—not a separately hard-coded downstream map.
4. Include cross-cutting/global constraints and their referenced Elements; unchanged local bytes do not prove the full semantic closure remains valid.
5. Distinguish source change from hypothetical change, metadata-only change, parser change, and consumer contract change.
6. Mark affected assertions/SAPs/Blueprint/consumer projections stale or review-required before requalification.
7. Revalidate affected Elements and parent/composition obligations; preserve unrelated source pins only when dependency analysis proves they are unaffected.
8. Record before/after revisions, impact set, tests, reviewer decisions, and unresolved owner decisions.

A hypothetical mutation test demonstrates behavior under a simulated change; it is not evidence that a real upstream release occurred.

## 10. Phase 7 — Evaluate implementation feasibility

DKE must analyze what is useful and knowable, but Product and implementation owners decide what becomes a feature.

### Feasibility levels

| Level | Meaning | Evidence expectation |
|---|---|---|
| I0 | Explain / recommend | qualified knowledge and explicit limits |
| I1 | Real read-only observation | actual provider/OS data, identity and freshness evidence |
| I2 | Evidence-backed plan / preview | exact target, predicted scope/effect, no mutation |
| I3 | Bounded effect after explicit authorization | controlled execution, journal, typed outcome and independent postcondition |
| I4 | Destructive, privileged, or hard-to-reverse effect | stronger Product admission, exact identity, risk controls, recovery proof, independent review and native environment evidence |

These levels are not a claim that every task should reach I4. Some tasks should remain I0–I2 or be excluded.

### Keep maturity dimensions separate

For every candidate capability, record independently:

- PRODUCT_ADMITTED
- SOURCE_DOCUMENTED
- KNOWLEDGE_QUALIFIED
- API/PROVIDER_AVAILABLE
- IMPLEMENTED
- TESTED (identify exact test type and environment)
- NATIVE_ENVIRONMENT_VERIFIED
- USER_JOURNEY_INTEGRATED
- RECOVERY_VERIFIED

An OS API being documented does not prove the application uses it. Source code does not prove it ran. Hosted logic tests do not prove native Windows behavior. A successful command does not prove the intended postcondition.

### Candidate ranking

Evaluate user value, frequency, impact, harm if wrong, reversibility, prerequisites, platform/version coverage, permission model, trusted provider availability, testability, independent oracle availability, recovery, cost, and maintenance burden.

Keep Product-critical tasks separate from future candidates. DKE may research a candidate without granting implementation authorization.

## 11. Phase 8 — AOT / Runtime separation

AOT means compiling stable, reviewed, version-pinned knowledge and contracts ahead of execution. It does not mean guessing the current machine state.

### Suitable AOT material

- Stable concepts, vocabulary, domain rules, and source-backed facts.
- Platform/version applicability matrices and compatibility rules.
- Qualified decision trees and precondition logic.
- Risk classes, protected-asset semantics, refusal conditions.
- Function schemas, typed outcomes, and static dependency contracts.
- Verification oracles, expected postconditions, and recovery policies.
- Provenance, source revision, SAP status, expiry/requalification triggers.

### Runtime-only material

- Current machine, OS build, device and package inventory.
- Exact disk/volume/file/process/service/device identity.
- Current ACLs, permissions, privileges, locks, free space, and connectivity.
- Current user intent, approval, session, permit, and authorization decision.
- Current provider availability, trust/revocation state, and downloaded artifact identity.
- Live execution result, journal, observed postcondition, and recovery receipt.

**AOT must never contain or imply live user/device state, current approval, a reusable permit, or authority to perform an effect.** Runtime must re-check volatile facts and authority at the point of use.

## 12. Phase 9 — Knowledge-to-Function functional closure (DKE → DIS → Runtime)

Only a Product-admitted task with sufficiently qualified knowledge may proceed to implementation. DKE supplies semantics and assurance; DIS defines functionization contracts; Runtime/Host supplies live authority and effects.

### End-to-end closure chain

```text
User goal
  → intent normalization / clarification
  → Product-admitted capability selection
  → Runtime observation of current state and exact target identity
  → AOT knowledge: applicability, rules, risk, preconditions and verification
  → bounded plan / preview
  → explicit user approval where required
  → independent Runtime/Kernel/Host authorization and permit checks
  → journaled, bounded effect
  → typed outcome (including BLOCKED / REJECTED / UNKNOWN / PARTIAL)
  → independent observation of postconditions
  → reconciliation / safe recovery; never blind retry an uncertain effect
  → truthful user-visible result, evidence and history
```

### Function closure contract

Every Function/Pipeline candidate must define:

- Purpose and Product journey linkage.
- Exact Function identity/version, typed input/output, and typed outcomes.
- Required AOT knowledge package and SAP qualification pins.
- Preconditions, applicability, dependencies, and target identity semantics.
- Read/write effects, protected assets, risk class, and idempotency behavior.
- User approval and independent authorization requirements.
- Runtime observations and evidence schema.
- Journal/lease/recovery/reconciliation behavior.
- Independent postcondition oracle and success criteria.
- UNKNOWN/PARTIAL/FAILED behavior and safe continuation rules.
- User-visible explanation, history, and evidence retention.

**A Function cannot self-certify success.** Exit code 0 or a returned `SUCCESS` field is only execution evidence. The system must independently observe the intended postcondition and check protected invariants. If the postcondition cannot be established, return UNKNOWN or PARTIAL rather than inventing success.

### Example: free space on a system drive

- DKE models file/asset categories, protected assets, deletion semantics, scope, and safe-cleanup rules; it records sources and SAP cases.
- Feasibility distinguishes read-only disk inventory (I1), a file-by-file preview (I2), bounded cleanup with approval and verification (I3), and partition/format operations (I4, separate high-risk scope).
- AOT contains stable classification rules, protected-asset policy, OS applicability, and verification criteria.
- Runtime observes current volumes, exact selected root/files, ACLs, locks, and free space; builds the preview; obtains approval and permits; executes only the approved scope; then re-observes free space and protected canaries.
- If the target changes, protected state cannot be checked, or execution outcome is uncertain, block/reconcile and report UNKNOWN/PARTIAL. Do not treat a successful delete command as proof of safe cleanup.

The same reasoning applies to software lifecycle and hardware/driver management: identity, provenance, compatibility, privilege, effect, reboot/recovery, and independent postcondition must be explicit. Researching those domains does not admit them as Product features.

## 13. Safety, uncertainty, and refusal

- UNKNOWN is a valid result, not a failure to write enough prose.
- CONFLICT remains unresolved until an authorized oracle adjudicates it.
- OUTDATED evidence cannot silently support a current assertion.
- EXCLUDED means explicitly outside scope; it is not equivalent to UNKNOWN.
- If target identity, applicability, authorization, or expected effect is ambiguous, do not mutate.
- Fail closed on missing provenance, invalid signatures, source mismatch, expired qualification, stale policy, untrusted provider, unexpected scope expansion, or unverified protected invariants.
- Do not retry a non-idempotent or uncertain effect blindly. Reconcile against the journal and live state.
- Keep advice separate from authority: an LLM proposal, generated plan, or knowledge Claim is never a permit.
- High-risk/destructive tasks require explicit Product admission and stronger domain, source, native-environment, and recovery evidence.

## 14. Evidence and validation discipline

Every result must identify what was actually checked.

| Evidence type | What it can establish | What it cannot establish alone |
|---|---|---|
| Source/document review | what the pinned source says | implementation or runtime behavior |
| Structural checker | schema, IDs, references, declared invariants | semantic truth or source authority |
| Unit/logic test | behavior of tested code under fixtures | native OS/provider behavior |
| Hosted execution | behavior in the named hosted runtime | local Node, Windows, device, or production behavior |
| Native environment test | behavior on the exact recorded OS/build/provider/device | untested versions or all environments |
| Independent semantic review | reasoned source-grounded assessment | owner decision where owner authority is required |
| Runtime receipt | recorded execution/observation for one run | universal capability or future machine state |

Record exact commit/tree/blob, tool/runtime versions, command, exit status, environment, fixture/source pins, output digest, and reviewer identity/role. Never state that native tests ran if only hosted checks ran.

## 15. Required deliverables and repository artifacts

A DKE workstream should produce only the artifacts needed for its scope, but must keep them versioned and traceable:

1. Product/domain scope and acceptance authority.
2. Stage-0 raw-source manifest.
3. Demand-to-knowledge matrix.
4. Source/Claim register and canonical KG/corpus.
5. Domain Blueprint and DEDS decision ledger.
6. Element profiles and global semantic Element ownership.
7. Per-Element SAP and CQ/validation bundles.
8. Independent review packet and exact-SHA findings.
9. Source-change/impact receipts and qualification state.
10. Demand-to-function feasibility/closure matrix.
11. DIS handoff contract for admitted capabilities.
12. Runtime/native verification and functional-closure receipts, if implemented.

Suggested project layout (adapt to an existing repository rather than moving files mechanically):

```text
docs/
  product/                 # Product authority and scope
  sources/                 # manifests, provenance, immutable source references
  knowledge/               # vocabulary, claims, relations, invariants
  blueprint/               # canonical graph revision, DEDS, Element ownership
  elements/<element-id>/   # Element profile, SAP, CQ, verification bundle
  review/                  # Stage-0, independent reviews, findings, repairs
  evolution/               # source changes, impact analysis, requalification
  feasibility/             # demand-to-function matrix and implementation evidence
  functionization/         # DIS handoff references (not duplicate ABI authority)
  runtime-evidence/        # actual host/native execution receipts
```

Use the existing project's conventions and canonical data format. Avoid duplicating the same authoritative content in multiple files; prefer stable IDs and references.

## 16. Quality gates

A project may tailor gate names, but it must answer all of these questions:

- **G0 Scope/authority:** Is the task authorized and bounded?
- **G1 Demand:** Is there evidence that the task matters, and are required knowledge needs explicit?
- **G2 Sources/claims:** Are source identity, version, scope, claim meaning, and uncertainty traceable?
- **G3 Structure/ownership:** Are Root, child, global semantic Elements, relations, invariants, and the three graph structures coherent?
- **G4 Assurance:** Does every Element have adequate SAP/CQs/oracles and independent source-first review? Are parent/composition obligations checked?
- **G5 Evolution:** Can changed evidence invalidate exactly the affected semantic closure without trusting a separate hard-coded map?
- **G6 Feasibility/admission:** Is each maturity dimension evidenced and Product authority explicit?
- **G7 Function closure:** Does the real user journey complete with authorization, bounded effects, typed outcomes, independent postcondition, recovery, and truthful history?

A gate can be NOT_RUN, PASS, FAIL, BLOCKED, UNKNOWN, or NOT_APPLICABLE only under a defined rule. A global PASS cannot be inferred from a percentage of tests or from children passing independently.

## 17. Common failure modes to prevent

- Starting from APIs or technology inventory instead of user/product demand.
- Collecting large volumes of sources without authority, version, scope, or task relevance.
- Treating LLM-generated Claims, citations, tests, or confidence as authoritative.
- One Element per fact, one Element per Function, or arbitrary fixed-size decomposition.
- Omitting global semantic Elements or leaving invariant ownership implicit.
- Collapsing semantic graph cycles into an executable DAG.
- Treating child PASS as parent/composition PASS.
- Using one global test bundle as a substitute for per-Element SAP.
- Treating structural validation or test count as semantic qualification.
- Reusing historical review as if it were a fresh independent Stage-0.
- Hard-coding source-impact maps separately from the actual Blueprint/dependency model.
- Confusing hypothetical source mutation with a real upstream release.
- Promoting knowledge to Function without Product admission and DIS contract authority.
- Treating AOT knowledge as current device state, approval, or permission.
- Treating command exit status as independently verified functional success.
- Reporting UNKNOWN or partial execution as PASS.

## 18. Completion criteria

A DKE workstream is complete for a declared scope only when:

1. The user/domain tasks and Product authority are explicit.
2. Required knowledge is traced to original, version-pinned evidence or clearly marked UNKNOWN.
3. The canonical graph, Blueprint, Element ownership, and DEDS decisions are coherent and reproducible.
4. Each Element has a sufficient SAP and validation bundle; global and parent composition obligations are covered.
5. An independent source-first reviewer has assessed the exact candidate revision, and required Owner/domain-oracle decisions are present or explicitly unresolved.
6. Source evolution and impact invalidation are demonstrated to the level required by scope.
7. Implementation feasibility and Product admission are separately recorded.
8. If Functionization is in scope, at least one real authorized journey is traced through DIS and Runtime to independently verified postconditions, recovery behavior, evidence, and truthful user-visible closure.

**Do not define completion as “all knowledge documented.”** The correct completion statement is always scoped: what tasks are covered, on which sources/versions/platforms, at what qualification and implementation level, with which UNKNOWNs and exclusions still open.

---

## 19. Current reference applications

- **DomainForge DKE v0.0.1:** [main exploration/evidence Issue #209](https://github.com/kaicreator-mm/domain-forge/issues/209), [Product/L1 candidate #207](https://github.com/kaicreator-mm/domain-forge/issues/207), and [Draft PR #208](https://github.com/kaicreator-mm/domain-forge/pull/208). The Product/L1 candidate specifically requires Blueprint/DEDS to be produced alongside canonical KG construction and makes global semantic Elements and Element self-verification first-class. Its own L1/L2/qualification status remains governed by those project records.
- **Shun Assistant computer-assistant application:** [Issue #411](https://github.com/kaicreator-mm/shun-assistant/issues/411). It applies the demand → knowledge → feasibility → functional-closure analysis to an assistant product. The candidate expansion of general disk, software, driver, service, or network management remains subject to explicit Product admission.

This document is a methodology candidate. It does not modify any referenced project's Product scope, grant implementation permission, or replace a domain-specific standard/Owner decision.
