---
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
---

# SAVANT FRAMEWORK — CONTRIBUTOR LICENSE AGREEMENT (CLA)

This document contains the Individual Contributor License Agreement (ICLA) and
the Entity Contributor License Agreement (ECLA) for the SAVANT FRAMEWORK
repositories: `savant-core`, `clai-os`, `aegis-ng`, `aegis-global`, and
`grants`.

Project Steward and Licensor: Dr. Christabel Odeta — SAVANT FRAMEWORK ·
CLAI-OS · AEGIS-GLOBAL ("the Steward").

---

## 0. ENFORCEMENT — NO UNSIGNED CODE ENTERS THE TREE

  0.1 Every pull request against any SAVANT FRAMEWORK repository is BLOCKED by
      CLA Assistant until the submitting author has a signed CLA on file. There
      are no exceptions for trivial patches, typo fixes, documentation, or
      governance members.

  0.2 Signature requires, at minimum:
      - Real legal name (no pseudonyms, no handles);
      - A verifiable email address;
      - A GPG key fingerprint (full 40-character fingerprint), which must match
        the key used to sign the contributor's commits where commit signing is
        enforced by the S50 governance engine.

  0.3 Entity contributors must additionally name an authorized signatory and
      provide the entity's jurisdiction of incorporation. Compliance adapters
      P61–P70 use this jurisdiction to route NDPR (Nigeria), GDPR (EU), or
      other applicable data-protection obligations to the contributor's
      submissions involving personal data fixtures or test corpora.

## 1. DEFINITIONS

  "Contribution" — any original work of authorship, including prompts, prompt
  fragments within SPOS-P1 through SPOS-P12, SIP invocation templates,
  deterministic engine logic, FHIR R4 resource mappings, LoRa mesh firmware,
  Hyperledger anchoring scripts, documentation, and test vectors, that is
  intentionally submitted for inclusion in any SAVANT FRAMEWORK repository.

  "Submit" — any form of electronic, verbal, or written communication sent to
  the project, including pull requests, commits, issues, patches, and SIP
  invocation artifacts merged into the prompt genealogy ledger.

  "You" — the individual or entity signing this agreement.

## 2. INDIVIDUAL CONTRIBUTOR LICENSE AGREEMENT (ICLA)

By signing, You agree:

  2.1 Copyright License. You grant the Steward a perpetual, worldwide,
      non-exclusive, no-charge, royalty-free, irrevocable copyright license to
      reproduce, prepare derivative works of, publicly display, publicly
      perform, sublicense, and distribute Your Contributions and derivative
      works under BOTH AGPL-3.0 AND Savant-Commercial-1.0, at the Steward's
      election per the dual-license model declared in LICENSE. You
      acknowledge and accept that the Steward may distribute Your Contribution
      commercially under Savant-Commercial-1.0 without further compensation or
      consent, and simultaneously under AGPL-3.0. This explicit dual-license
      grant is a condition of contribution; contributors who cannot grant it
      must not submit.

  2.2 Patent License. You grant the Steward and all recipients of the software
      a perpetual, worldwide, non-exclusive, no-charge, royalty-free,
      irrevocable (except as stated in this section) patent license to make,
      use, sell, offer for sale, import, and otherwise transfer Your
      Contribution, where such license applies only to patent claims licensable
      by You that are necessarily infringed by Your Contribution alone or in
      combination with the work to which it was submitted. If You institute
      patent litigation alleging that Your Contribution or the work constitutes
      infringement, this patent license terminates as of the filing date, per
      the retaliation clause in LICENSE Section 4.

  2.3 Originality. You represent that each Contribution is Your original
      creation, or that You have sufficient rights to grant the licenses above.
      You represent that no Contribution contains code or prompts copied from a
      source incompatible with AGPL-3.0 or with Savant-Commercial-1.0
      dual-licensing.

  2.4 No Obligation of Support. You provide Contributions on an "AS IS" basis.

  2.5 Employment. If Your Contribution is made within the scope of employment,
      Your employer must sign the ECLA (Section 3) or provide written
      authorization before CLA Assistant will unblock Your pull requests.

## 3. ENTITY CONTRIBUTOR LICENSE AGREEMENT (ECLA)

  3.1 The signing entity grants the Steward the same copyright and patent
      licenses as Sections 2.1 and 2.2 for all Contributions submitted by its
      employees, contractors, or agents whom it designates in writing to the
      Steward.

  3.2 The entity represents that its designated signatory has authority to bind
      it, and that it will maintain a current list of designated contributors.
      Sovereign entities receiving technology under the Sovereign Technology
      Transfer carve-out (LICENSE Section 5) must still execute this ECLA
      before contributing modifications back; the fee exemption does not
      exempt contribution hygiene.

  3.3 The entity acknowledges the dual-license reality: contributions it
      submits may be distributed under AGPL-3.0 OR Savant-Commercial-1.0, and
      it waives any claim that commercial distribution of its Contribution
      requires separate negotiation.

## 4. GOVERNANCE-SPECIFIC OBLIGATIONS

  4.1 Contributions that modify any load-bearing prompt (SPOS-P1 through
      SPOS-P12), any SIP trigger routing table, or any S50 checkpoint rule must
      include a completed prompt genealogy entry (see GOVERNANCE.md Section 4.3).
      CLA Assistant and the S50 engine jointly reject prompt modifications
      lacking genealogy lineage.

  4.2 Contributions touching the deterministic engine layer are additionally
      reviewed for commercial-boundary integrity per CAA.md; a Contribution
      that would move proprietary logic into the open FHIR R4 layer, or open
      logic into the proprietary layer without authorization, will be rejected
      regardless of CLA status.

## 5. EXECUTION

Sign by submitting the following block as a comment on your first pull request
(or by GPG-signed email to the project legal address), which CLA Assistant
verifies and records:

    I, [REAL LEGAL NAME], email [EMAIL], GPG fingerprint
    [40-CHARACTER FINGERPRINT], have read and agree to the SAVANT FRAMEWORK
    CLA v1.0.0 (ICLA / ECLA as applicable), including the explicit dual-license
    grant under BOTH AGPL-3.0 AND Savant-Commercial-1.0, election of
    distribution terms being reserved to the Steward per Section 2.1.
    Date: [YYYY-MM-DD]

## Falsifiability Test

Test: Attempt to merge a pull request from (a) an unsigned author, (b) an
author whose CLA omits the GPG fingerprint, and (c) an author whose CLA
disclaims the dual-license grant.
Expected result: CLA Assistant blocks (a) and (b) at status-check time, and the
Steward rejects (c) as a failed grant under Section 2.1 — in all three cases no
code enters the tree. If any of the three merges successfully, the CLA
enforcement claim in Section 0 is falsified.
