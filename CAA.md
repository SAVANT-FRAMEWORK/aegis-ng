---
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
---

# SAVANT FRAMEWORK — COMMERCIAL ACCESS AGREEMENT (CAA) v1.0

Licensor: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL.
This document is the master Commercial Access Agreement template for the
Savant-Commercial-1.0 license path declared in LICENSE. Individual deals are
executed by appending a signed Order Form to this master text.

---

## 1. PURPOSE

This agreement grants a commercial licensee the right to use specified
SAVANT FRAMEWORK components without triggering the copyleft obligations of
AGPL-3.0, within a precisely defined open-core boundary. This document exists
so that the boundary between open and proprietary is a matter of contract
text, not marketing narrative.

## 2. LICENSED COMPONENTS — PROPRIETARY SIDE OF THE BOUNDARY

The following components are proprietary and are licensed commercially only
under this CAA:

  2.1 The DETERMINISTIC ENGINE LAYER of CLAI-OS: the deterministic-first
      clinical reasoning core that executes rule-bounded inference before any
      probabilistic model output is permitted to reach a decision path
      (subject matter of PPA-001).

  2.2 The offline CRDT synchronization engine as embodied in the production
      sync service: conflict-free replicated data type merge logic operating
      natively over FHIR R4 resources without a central coordinator
      (subject matter of PPA-002).

  2.3 The AEGIS-NG / AEGIS-GLOBAL 433MHz LoRa mesh safety infrastructure
      control plane: mesh routing, store-and-forward alerting, and per-unit
      cost-optimized firmware logic (reference per-unit cost withheld — program documentation)
      (subject matter of PPA-003).

  2.4 The federated edge learning coordinator with differential privacy:
      gradient aggregation, privacy-budget accounting, and edge-node
      orchestration (subject matter of PPA-004).

  2.5 The metric-gated blockchain grant tranching engine: milestone-attested
      release of grant capital via Hyperledger audit anchoring, as deployed in
      the `grants` repository (subject matter of PPA-005).

## 3. THE BOUNDARY — WHAT REMAINS OPEN, PERMANENTLY

  3.1 THE FHIR R4 RESOURCE LAYER IS OPEN. All FHIR R4 resource definitions,
      profiles, mappings, serializers, validators, and conformance tooling in
      every SAVANT FRAMEWORK repository are and remain licensed under
      AGPL-3.0 in perpetuity, in every distribution model, for every licensee.

  3.2 The proprietary boundary is drawn at the DETERMINISTIC ENGINE LAYER —
      the reasoning and control logic — NOT at the data-interchange layer.
      Rationale: interoperability infrastructure (FHIR R4) is a public good;
      the clinical reasoning engine that acts on interoperable data is the
      commercial asset. No Order Form, amendment, side letter, or course of
      dealing may move the boundary into the FHIR R4 resource layer. Any
      purported term doing so is void.

  3.3 The SIP v1.0 invocation protocol surface (trigger prefixes and one-letter
      shortcuts) and the SHA-256 checkpoint verification interface of the S50
      governance engine are open, so that auditors, grant officers, and
      sovereign partners can verify governance integrity without a commercial
      license.

## 4. PATENT POSITION

  4.1 This CAA conveys a limited, non-exclusive, non-transferable patent
      license to PPA-001 through PPA-005, strictly as embodied in the Licensed
      Components of Section 2, for the term of this agreement.

  4.2 The patent retaliation clause of LICENSE Section 4 applies in full to
      commercial licensees and survives termination of this agreement with
      respect to rights already revoked.

  4.3 PPA-006 (Jurisdiction Compiler) is planned but not yet filed at the date
      of this document (see PATENTS.md, defensive publication v3.1
      reconciliation). No rights to PPA-006 are granted, implied, or
      promissory under this CAA. Licensees receive no expectation of
      Jurisdiction Compiler coverage until a supplemental Order Form is
      executed after filing.

## 5. LICENSE GRANT AND RESTRICTIONS

  5.1 Grant. Subject to payment of fees in the Order Form, Licensor grants
      Licensee a non-exclusive, non-sublicensable (except to affiliates named
      in the Order Form), non-transferable license to use the Licensed
      Components in object-code and, where specified, source-code form, for
      Licensee's internal operations and for products identified in the Order
      Form.

  5.2 Restrictions. Licensee shall not: (a) re-close, relicense, or restrict
      the FHIR R4 resource layer; (b) remove attribution to Dr. Christabel
      Odeta; (c) use the Singularity Mark except as permitted by TRADEMARK.md;
      (d) tamper with, bypass, or falsify S50 SHA-256 go/no-go checkpoints;
      (e) export Licensed Components in violation of applicable export
      control or sanctions law.

  5.3 Audit. Licensor may, on 30 days' notice, audit deployment scope against
      the Order Form once per calendar year. Discrepancies beyond 5 percent of
      licensed scope are billed retroactively at list price plus interest.

## 6. SOVEREIGN LICENSEES

Sovereign entities qualifying under LICENSE Section 5 (Sovereign Technology
Transfer carve-out) sign this CAA at no fee for non-commercial
humanitarian deployment, recorded explicitly in the Order Form. All other
clauses — including audit, attribution, checkpoint integrity, and trademark —
apply without modification.

## 7. COMPLIANCE AND DATA PROTECTION

Licensee deployments processing personal data must engage the applicable
compliance adapters P61–P70 for their operating jurisdictions (24 supported
jurisdictions at v1.0), including NDPR (Nigeria) and GDPR (EU). Licensor's
provision of adapters does not transfer regulatory responsibility; Licensee
remains the data controller of record.

## 8. TERM, TERMINATION, SURVIVAL

  8.1 Term: as stated in the Order Form; absent a stated term, 12 months,
      non-renewing without written extension.

  8.2 Termination for breach is effective 30 days after written notice if
      uncured; breach of Sections 3.2, 5.2(b), 5.2(c), or 5.2(d) is incurable
      and terminates immediately.

  8.3 Survival: Sections 3, 4.2, 6, 7, and 9 survive termination.

## 9. LIABILITY

Aggregate liability under this CAA is capped at fees paid in the 12 months
preceding the claim. The deterministic-first safety architecture reduces but
does not eliminate deployment risk; regulatory clearance in each deployment
jurisdiction remains Licensee's obligation.

## Falsifiability Test

Test: Given any SAVANT FRAMEWORK component, classify it as open or proprietary
using only Sections 2 and 3 of this document, then check the classification
against the repository's actual licensing headers.
Expected result: every component touching the deterministic engine layer
classifies as proprietary; every component of the FHIR R4 resource layer
classifies as open under AGPL-3.0; zero components classify ambiguously. If a
FHIR R4 resource artifact is found behind the commercial boundary, or a
deterministic engine artifact is found unlicensable under this CAA, the
open-core boundary claim is falsified.
