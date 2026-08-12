<!--
=============================================================================
SAVANT FRAMEWORK — CONSTITUTIONAL ISSUE TEMPLATE
File: .github/ISSUE_TEMPLATE/feature_request.md
SIP Invocation: HARDEN: [S56] Constitutional CI/CD Pipeline
-----------------------------------------------------------------------------
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
=============================================================================
-->
---
name: Feature Request (Constitutional)
about: Propose a capability with a Constitutional Impact Assessment
title: "[L?-?????] feat(<repo>): <concise capability summary>"
labels: ["enhancement", "constitutional-review"]
assignees: []
---

## SPOS Layer Attribution (required — check exactly one)

- [ ] [L0-KERNEL]
- [ ] [L1-AUDIT]
- [ ] [L2-STRATEGIC]
- [ ] [L3-TACTICAL]
- [ ] [L4-AGENTIC]
- [ ] [L5-EXECUTION]

## Constitutional Impact Assessment (REQUIRED)

<!--
Every feature touches the constitution. State precisely:
  1. Which SPOS layer owns this capability (must match the checkbox above).
  2. Which existing ADR (ADR-001 … ADR-007) is amended, superseded, or
     constrained by this feature.
  3. Which patent claim (if any) is implicated — cite the claim number or
     state "no patent claim implicated".
An assessment of "none" in all three fields is UNCONSTITUTIONAL and the
request will be closed without review.
-->

**Owning SPOS layer:**

**ADR affected:** <!-- ADR-001 … ADR-007, or "new ADR required" -->

**Patent claim implicated:** <!-- claim number, or "no patent claim implicated" -->

## ADR Reference (REQUIRED)

<!--
If this feature cannot be mapped to an existing ADR, it requires a new ADR
BEFORE implementation. State the ADR disposition explicitly.
-->

- [ ] Maps to existing ADR: <!-- ADR-00X -->
- [ ] New ADR required (must be merged before any implementation PR)

## Capability Description

<!-- What does this enable, for which sovereign actor, and why now? -->

## Determinism & Falsifiability

<!--
If this feature introduces reasoning chains or model invocations, state how
deterministic output is guaranteed (seeded RNG, temperature=0, injected
clocks) and which deterministic/ paths it will occupy.
-->

**Determinism guarantee:**

**Falsification condition (what observable outcome would prove this feature fails its claim):**

## Constitutional Attestation

- [ ] I have read GOVERNANCE.md, SPOS v1.0, and the referenced ADR(s).
- [ ] This request does not circumvent any S50 checkpoint or SIP trigger.

<!--
=============================================================================
FALSIFIABILITY TEST (this template):
  Claim: "A feature request without a Constitutional Impact Assessment
  (layer + ADR + patent-claim disposition) cannot proceed to implementation."
  Falsification: merge any implementation PR whose originating request left
  all three assessment fields empty; if possible, the template has failed.
=============================================================================
-->
