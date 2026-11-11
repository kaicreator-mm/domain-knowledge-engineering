# Demand-to-Function Closure Matrix Template

**Status:** template; fill only with source-backed facts.  
**Domain / Product:**  
**Product authority + exact revision:**  
**Domain / KG revision:**  
**Target platform / version scope:**  
**Owner / Reviewer:**  

Use one row per user job or bounded task. Split a row only when the tasks have materially different knowledge, authority, risk, or verification boundaries. Do not infer Product admission from demand priority.

## 1. Matrix

| Field | Required content |
|---|---|
| Job ID / title | Stable identifier and user-visible goal |
| Demand evidence | Product journey, owner request, observed case, source locator; otherwise UNKNOWN |
| Demand class | D0 Product-critical / D1 candidate / D2 specialist / D3 boundary |
| Product status | ADMITTED / CANDIDATE / EXCLUDED / UNKNOWN; include exact Product revision |
| Actor / trigger / success | Who asks, under what condition, and observable success |
| Knowledge requirements | Concepts, facts, rules, relations, invariants, preconditions, exceptions |
| Source pins | Source IDs, revisions, hashes/Git Blobs, exact sections/records |
| Claim / Element mapping | Claim IDs, owning Element IDs, global semantic Element references |
| CQ / SAP mapping | Positive, negative, boundary, conflict, UNKNOWN, outdated cases and SAP revision |
| AOT-eligible knowledge | Stable source-backed semantics, applicability, rules, risk, verification logic |
| Runtime-only facts | Live state, exact target identity, permissions, current approval, permits, receipts |
| Feasibility level | I0 explanation / I1 observation / I2 plan-preview / I3 authorized bounded effect / I4 high-risk effect |
| Maturity evidence | Separate statuses: documented, qualified, API/provider available, implemented, tested, native verified, integrated, recovery verified |
| Candidate Function/Pipeline | Function ID/version, typed I/O, typed outcomes, dependencies; or NOT_PROPOSED |
| Preconditions / authority | Applicability, target identity, privileges, approvals, permits, refusal conditions |
| Effect / risk | Read/write set, protected assets, reversibility, idempotency, risk class |
| Postconditions / oracle | Independently observable expected state and authoritative verification method |
| Failure / recovery | FAILED, BLOCKED, UNKNOWN, PARTIAL handling; reconciliation and safe recovery |
| User-visible closure | What can be truthfully reported, with evidence/history |
| Dependencies / cost | Technical/domain dependencies, implementation and maintenance cost |
| Owner decisions | Unresolved scope, semantics, source authority, risk, or product-admission questions |
| Final state | GAP / UNKNOWN / EXCLUDED / RESEARCH / QUALIFIED / IMPLEMENTED / VERIFIED |

## 2. Example (illustrative only; not Product admission)

| Field | Example |
|---|---|
| Job ID / title | STORAGE-CLEAN-01 — safely free space under a user-selected folder |
| Demand evidence | Must cite the actual Product journey or Owner request; otherwise mark UNKNOWN |
| Demand class / Product status | D1 / CANDIDATE until explicitly admitted |
| Knowledge requirements | File/asset classes, protected assets, path identity, ACL/locks, deletion semantics, OS applicability, free-space measurement |
| AOT-eligible | Stable file classification rules, protected-asset policy, applicability, preview and postcondition criteria |
| Runtime-only | Current volume, selected root, exact files, ACLs, locks, free space, user approval, permit, journal |
| Feasibility | I1 inventory → I2 exact preview → I3 approved bounded cleanup; partition/format is separate I4 scope |
| Function/Pipeline | Candidate only after Product admission and DIS contract approval |
| Preconditions | Exact selected scope, target identity stable, protected assets excluded, permissions and approval valid |
| Postconditions | Independently re-observe free space; verify protected canaries and intended scope |
| UNKNOWN handling | Target changed, access denied, effect uncertain, or postcondition unavailable → reconcile; never claim success |
| Final state | Keep CANDIDATE / NOT_IMPLEMENTED until actual evidence exists |

## 3. Status vocabulary

Use the project-defined canonical vocabulary if one exists. At minimum, keep these dimensions separate:

- Demand: EVIDENCED / UNKNOWN.
- Product: ADMITTED / CANDIDATE / EXCLUDED / UNKNOWN.
- Knowledge: NOT_STARTED / CANDIDATE / SOURCE_TRACEABLE / SAP_REVIEWED / QUALIFIED / STALE.
- Implementation: NOT_PROPOSED / PLANNED / IMPLEMENTED / TESTED / NATIVE_VERIFIED.
- Integration: NOT_INTEGRATED / USER_JOURNEY_INTEGRATED.
- Runtime closure: NOT_RUN / PASS / FAIL / BLOCKED / UNKNOWN / PARTIAL.

Never derive a later status automatically from an earlier one.
