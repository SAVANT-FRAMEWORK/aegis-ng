<!--
=============================================================================
SAVANT FRAMEWORK — CONSTITUTIONAL PULL REQUEST TEMPLATE
File: .github/PULL_REQUEST_TEMPLATE.md
SIP Invocation: HARDEN: [S56] Constitutional CI/CD Pipeline
-----------------------------------------------------------------------------
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
-----------------------------------------------------------------------------
NOTE: This template is a constitutional instrument, not a courtesy form.
The constitutional-check workflow enforces the SPOS layer tag on this PR's
title and every commit message automatically, with zero manual review.
=============================================================================
-->

## SPOS Layer Tag Confirmation (REQUIRED — blocking)

<!--
This PR title and EVERY commit message must begin with exactly one:
  [L0-KERNEL] [L1-AUDIT] [L2-STRATEGIC] [L3-TACTICAL] [L4-AGENTIC] [L5-EXECUTION]
Example: [L3-TACTICAL] feat(aegis-ng): add F-04 TFLite Micro model M-03
Untagged work is UNCONSTITUTIONAL (GOVERNANCE.md, SPOS v1.0) and is
rejected automatically.
-->

- [ ] I confirm the PR title and every commit message carry a valid SPOS layer tag: **<!-- tag here, e.g. [L3-TACTICAL] -->**

## Summary

<!-- What does this change do, at which layer, and under which SIP trigger? -->

## Constitutional Compliance (REQUIRED — all boxes must be checked)

- [ ] **DCO sign-off**: every commit carries `Signed-off-by: Real Name <email>` (Developer Certificate of Origin).
- [ ] **CLA signed**: I have signed the Contributor License Agreement via the CLA Assistant (see CLA_ASSISTANT_CONFIG.yml; PRs are blocked until signed).
- [ ] **Regression check**: I have run the repository test suite locally and state the result below.
- [ ] **Determinism**: changes under `deterministic/` contain no unseeded randomness, no `temperature>0` invocations, and no timestamp-dependent logic.

**Regression check statement (REQUIRED):**
<!-- e.g., "pytest -q: 42 passed, 0 failed on <commit-sha>" or "no test suite present — falsifiability-test workflow suite step is a no-op" -->

## Falsifiability Test (REQUIRED)

<!--
State the claim this PR makes and the concrete, deterministic evidence that
would falsify it. A PR advancing an unfalsifiable claim is UNCONSTITUTIONAL.
Ethos: the failure does not propagate stochastic uncertainty.
-->

**Claim:**

**Falsification condition:**

## ADR / Governance Reference

- ADR affected: <!-- ADR-001 … ADR-007, or "new ADR required" -->
- Threat model relevance (if any): <!-- S-01 … S-08, or "none" -->
- S50 checkpoint impact: <!-- does this change alter release artifacts? yes/no -->

## Constitutional Attestation

- [ ] I have read GOVERNANCE.md, SPOS v1.0, and SIP v1.0.
- [ ] I accept that violations of this template are constitutional violations, not style issues, and are rejected without manual override.

<!--
=============================================================================
FALSIFIABILITY TEST (this template):
  Claim: "A PR missing SPOS tag confirmation, DCO sign-off, regression
  statement, falsifiability section, or CLA checkbox is identifiable as
  unconstitutional and blocked before merge."
  Falsification: attempt to merge a PR with every section blank; the
  constitutional-check and CLA Assistant gates must both block it. If the
  merge succeeds, the constitution has failed.
=============================================================================
-->
