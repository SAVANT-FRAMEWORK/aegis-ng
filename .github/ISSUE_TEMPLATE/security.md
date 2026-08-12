<!--
=============================================================================
SAVANT FRAMEWORK — CONSTITUTIONAL ISSUE TEMPLATE
File: .github/ISSUE_TEMPLATE/security.md
SIP Invocation: HARDEN: [S56] Constitutional CI/CD Pipeline
-----------------------------------------------------------------------------
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
=============================================================================
-->
---
name: Security Disclosure (Constitutional — Private Channel Preferred)
about: Threat-model-referenced security report. DO NOT publish exploit details here.
title: "[L1-AUDIT] security(<repo>): <non-sensitive summary only>"
labels: ["security", "constitutional-review", "private-disclosure"]
assignees: []
---

> **STOP — READ BEFORE FILING.**
> If this report contains a reproducible exploit, proof-of-concept code, or
> details enabling harm, DO NOT file it publicly. Report privately:
> **security@savant-framework.dev** (GPG-encrypted preferred; key fingerprint
> published in SECURITY.md). Public issues with exploit detail are locked,
> scrubbed, and re-routed. This template collects only NON-SENSITIVE metadata.

## Threat Model Reference (REQUIRED — check all that apply)

Per GOVERNANCE.md threat model, classify the finding:

- [ ] **S-01 — OPSEC** (operational security / key handling / personnel process)
- [ ] **S-02 — PERSEC** (personnel security / identity exposure)
- [ ] **S-03 — INFOSEC** (data confidentiality, integrity, availability)
- [ ] **S-04 — PHYSEC** (physical security of devices / deployment sites)
- [ ] **S-05 — RF Security** (radio-frequency emission / interception / jamming)
- [ ] **S-06 — Supply Chain** (dependencies, build provenance, SBOM integrity)
- [ ] **S-07 — Firmware Security** (embedded/edge firmware, signed boot, TFLite Micro targets)
- [ ] **S-08 — Civilian Privacy** (non-combatant data protection, lawful-use constraints)

## SPOS Layer Attribution (required — check exactly one)

- [ ] [L0-KERNEL]
- [ ] [L1-AUDIT]
- [ ] [L2-STRATEGIC]
- [ ] [L3-TACTICAL]
- [ ] [L4-AGENTIC]
- [ ] [L5-EXECUTION]

## Non-Sensitive Summary

<!-- Classification-level description ONLY. No payloads, no PoC, no target data. -->

## Private Disclosure Checklist (REQUIRED)

- [ ] I have NOT included exploit code, payloads, or step-by-step reproduction in this public issue.
- [ ] I have sent (or am sending) full details to **security@savant-framework.dev** with GPG encryption.
- [ ] I understand coordinated disclosure per SECURITY.md and will observe the embargo window.

## Severity Self-Assessment (advisory)

- [ ] Critical (constitutional breach — checkpoint/anchor integrity at risk)
- [ ] High
- [ ] Medium
- [ ] Low / informational

## Constitutional Attestation

- [ ] I have read GOVERNANCE.md and the S-01…S-08 threat model.
- [ ] To my knowledge this finding does not endanger civilian privacy (S-08) if disclosed per this process.

<!--
=============================================================================
FALSIFIABILITY TEST (this template):
  Claim: "No public security issue filed via this template can contain
  exploit detail, and every filed issue carries at least one S-01…S-08
  threat-model reference."
  Falsification: file a test issue with no threat-model checkbox ticked and
  no private-disclosure checklist completed; if it can be triaged as valid,
  the template has failed.
=============================================================================
-->
