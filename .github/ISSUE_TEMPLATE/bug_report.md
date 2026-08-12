<!--
=============================================================================
SAVANT FRAMEWORK — CONSTITUTIONAL ISSUE TEMPLATE
File: .github/ISSUE_TEMPLATE/bug_report.md
SIP Invocation: HARDEN: [S56] Constitutional CI/CD Pipeline
-----------------------------------------------------------------------------
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
=============================================================================
-->
---
name: Bug Report (Constitutional)
about: Report a defect with a falsifiability test and SPOS layer attribution
title: "[L?-?????] bug(<repo>): <concise defect summary>"
labels: ["bug", "constitutional-review"]
assignees: []
---

## SPOS Layer Attribution (required — check exactly one)

- [ ] [L0-KERNEL]
- [ ] [L1-AUDIT]
- [ ] [L2-STRATEGIC]
- [ ] [L3-TACTICAL]
- [ ] [L4-AGENTIC]
- [ ] [L5-EXECUTION]

## Defect Description

<!-- What behavior is observed, and what constitutional claim does it violate? -->

## Reproduction (deterministic, step-by-step)

1.
2.
3.

**Expected behavior:**

**Observed behavior:**

## Falsifiability Test (REQUIRED)

<!--
What concrete, reproducible evidence would PROVE this bug invalidates a
specific claim (e.g., a determinism claim, an S50 checkpoint digest, a test
assertion)? A bug report without a falsifiability test is UNCONSTITUTIONAL
and will be closed without review. Remember the ethos: the failure does not
propagate stochastic uncertainty — reproduction must be deterministic.
-->

**Claim under test:**

**Evidence that would falsify the claim:**

## Regression Detection (REQUIRED)

<!--
Link to the regression record (issue/ADR/test ID) that should have caught
this, or state explicitly: "No regression record exists — new regression
test required."
-->

**Regression record link:** <!-- URL or "none — new regression test required" -->

## Environment

- Repository (savant-core / clai-os / aegis-ng / aegis-global / grants):
- Commit SHA:
- OS / toolchain:

## Constitutional Attestation

- [ ] I have read GOVERNANCE.md and SPOS v1.0 and confirm this report targets the correct layer.
- [ ] My reproduction steps are deterministic (seeded randomness, temperature=0, fixed clocks where applicable).

<!--
=============================================================================
FALSIFIABILITY TEST (this template):
  Claim: "A bug report missing the Falsifiability Test section or the SPOS
  layer checkbox is identifiable as unconstitutional on sight."
  Falsification: submit a report omitting either field; if maintainers can
  accept it without constitutional objection, the template has failed.
  The failure does not propagate stochastic uncertainty.
=============================================================================
-->
