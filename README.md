# Domain Knowledge Engineering (DKE)

**Repository purpose:** the reusable methodology, quality gates, and working templates for engineering domain knowledge from source evidence into independently reviewable, maintainable, and—where explicitly admitted—function-ready knowledge.

**Methodology status:** `DKE-METHOD-0.1.0-CANDIDATE`  
**Governance:** draft methodology; not yet frozen as a universal standard. Domain-specific Product authority and source-owner decisions remain controlling.

## What DKE does

DKE is not merely ontology authoring, document summarization, or splitting a domain into small libraries. It is a disciplined process that:

1. starts from a bounded user/product problem and frozen acceptance authority;
2. derives the knowledge demand from real tasks;
3. collects and pins authoritative sources;
4. models claims, concepts, relations, constraints, and unknowns with provenance;
5. recursively decomposes the domain into cohesive, independently verifiable Elements;
6. creates a Domain Blueprint and Element-level Semantic Assurance Profiles (SAP);
7. independently validates source fidelity, semantic correctness, ownership, and composition;
8. tracks source evolution and invalidates affected knowledge;
9. evaluates implementation feasibility and hands only admitted, qualified knowledge to downstream functionization.

The intended trace is:

`Product / User Jobs → Knowledge Demand → Sources → Claims & Graph → Blueprint / Elements → SAP & Independent Review → Feasibility → DIS Function / Pipeline → Runtime Evidence & Functional Closure`

## Start here

- [DKE Methodology 0.1.0](docs/methodology/DKE-METHOD-0.1.0.md) — the end-to-end process, ownership boundaries, qualification gates, AOT/Runtime separation, and functional closure.
- [Demand-to-Function Closure Matrix Template](docs/templates/DEMAND_TO_FUNCTION_CLOSURE_MATRIX.md) — trace real user jobs through knowledge, feasibility, Function/Pipeline, and verified outcomes.
- [Element SAP Profile Template](docs/templates/ELEMENT_SAP_PROFILE_TEMPLATE.md) — record source-backed semantic assurance obligations for each Element.

## Non-negotiable boundaries

- Product owners decide what the product promises and what may be implemented.
- DKE owns knowledge semantics, evidence provenance, decomposition, and semantic assurance—not execution authority.
- DIS owns the downstream functionization contracts (Function, Pipeline, ECP and AOT Package) under its own Product/ABI authority.
- Runtime/Host owns live machine facts, authorization, permits, effects, postcondition observation, and recovery.
- AOT knowledge never contains live machine state and never grants permission.
- Generated, reviewed, validated, qualified, selected, activated, and runtime-verified are distinct states.
- Missing, conflicted, stale, inapplicable, or unverified evidence remains explicit as UNKNOWN / CONFLICT / OUTDATED / EXCLUDED; it is never silently promoted to PASS.

## Reference practice

The current DKE v0.0.1 exploration and Element-decomposition evidence work is tracked in [domain-forge Issue #209](https://github.com/kaicreator-mm/domain-forge/issues/209), under its Product/L1 candidate [Issue #207](https://github.com/kaicreator-mm/domain-forge/issues/207). The methodology repository describes reusable practice; those project issues retain their own scope and qualification authority.

A computer-assistant application of demand → knowledge → feasibility → functional closure is tracked separately in [shun-assistant Issue #411](https://github.com/kaicreator-mm/shun-assistant/issues/411). It is a worked application, not a universal feature mandate.

## Repository structure

```text
docs/
  methodology/
    DKE-METHOD-0.1.0.md
  templates/
    DEMAND_TO_FUNCTION_CLOSURE_MATRIX.md
    ELEMENT_SAP_PROFILE_TEMPLATE.md
```

## Change policy

Methodology changes must be evidence-backed, versioned, and reviewed. A project-specific experiment may inform the method but does not automatically become a universal rule. Preserve unresolved owner decisions and explicit applicability. Do not retroactively change the acceptance criteria of an in-flight project by editing this repository alone.
