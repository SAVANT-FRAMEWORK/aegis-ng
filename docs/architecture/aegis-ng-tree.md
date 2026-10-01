---
Version: 1.0.0
Author: Dr. Christabel Odeta — SAVANT FRAMEWORK · CLAI-OS · AEGIS-GLOBAL
Last Updated: 2026-08-11
SHA-256: [PENDING-FIRST-RELEASE]
---

# AEGIS-NG v2.0 — Directory Tree

> Repository role: the physical-safety instantiation of SAVANT FRAMEWORK. A 433 MHz LoRa
> mesh of **14 hardware node types (N-A01 through N-D02)** running **12 firmware
> subsystems (F-01 through F-12)** across **STM32L072, ESP32-S3, and ESP32-C3** targets,
> hosting **6 TFLite Micro edge models (M-01 through M-06)** with federated learning and
> differential privacy in Hausa, Fulfulde, Igbo, Yoruba, and Efik. Solar-only power,
> anti-tamper enclosures, offline CRDT sync, deployed across **12 Nigerian LGAs** at a
> published BOM of **$46.30 per node**.

## 1. Tree

```
aegis-ng/
│
├── README.md
├── LICENSE                            ← inherited dual license (AGPL-3.0 / Savant-Commercial-1.0)
│
├── firmware/
│   ├── README.md
│   ├── F-01-power-management/         ← STM32L072
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-02-lora-mesh-radio/          ← STM32L072
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-03-sensor-acquisition/       ← STM32L072
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-04-edge-ai/                  ← ESP32-S3
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-05-crdt-sync/                ← ESP32-S3 + ESP32-C3
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-06-anti-tamper-enclosure/    ← all three targets
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-07-secure-bootloader/        ← all three targets
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-08-ota-update/               ← ESP32-C3
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-09-hmi-alerts/               ← ESP32-S3
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-10-data-logger-storage/      ← STM32L072
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── F-11-diagnostics-watchdog/     ← ESP32-C3
│   │   ├── README.md
│   │   └── .gitkeep
│   └── F-12-field-provisioning/       ← ESP32-C3
│       ├── README.md
│       └── .gitkeep
│
├── hardware/
│   ├── README.md
│   ├── nodes/                         ← 14 node types N-A01…N-D02 (index, not 14 forks)
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── schematics/
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── gerber/
│   │   ├── README.md
│   │   └── .gitkeep
│   └── bom/
│       ├── README.md
│       └── .gitkeep
│
├── mesh/
│   ├── README.md
│   ├── topology/
│   │   ├── README.md
│   │   └── .gitkeep
│   ├── protocols/
│   │   ├── README.md
│   │   └── .gitkeep
│   └── lga-deployments/
│       ├── README.md
│       └── .gitkeep
│
└── field-ops/
    ├── README.md
    ├── deployment-playbooks/
    │   ├── README.md
    │   └── .gitkeep
    ├── lga-site-surveys/
    │   ├── README.md
    │   └── .gitkeep
    ├── maintenance-logs/
    │   ├── README.md
    │   └── .gitkeep
    └── training-drills/
        ├── README.md
        └── .gitkeep
```

Directory count: 28 directories (including repo root): repo root + 13 firmware (root +
F-01…F-12), 5 hardware, 4 mesh, 5 field-ops, plus repo-level files.

## 2. Firmware Leaf READMEs (F-01 … F-12)

### `firmware/README.md`
- **Constitutional purpose:** root of the firmware plane — all embedded logic for all 14
  node types, organized as 12 subsystems with immutable identifiers F-01…F-12.
- **Maps to:** patent claims PPA-001 (node architecture), PPA-003 (federated edge
  learning), PPA-004 (CRDT sync); compliance requirement — deterministic, auditable
  embedded behavior inherited from the constitution.
- **Will live here:** the twelve subsystem directories below only.
- **Governing agent/phase:** Agent 02 (Firmware Engineer) governs the plane; F-04 is
  co-governed with Agent 03; every subsystem is frozen at release gates.

### `firmware/F-01-power-management/README.md` — target: STM32L072
- **Constitutional purpose:** solar-only power autonomy — MPPT charge control, battery
  stewardship, brownout survival, and energy budgeting so no node ever requires grid
  power or battery servicing infrastructure.
- **Maps to:** patent claim PPA-001 (solar-only node architecture); grant deliverable —
  off-grid operability evidence for `african-development-bank/` and `unicef-innovation/`.
- **Will live here:** energy budgets per node type (N-A01…N-D02), MPPT parameters,
  brownout state machines, solar-soak test protocols.
- **Governing agent/phase:** Agent 02; co-reviewed by Agent 01 (Hardware); per-release.

### `firmware/F-02-lora-mesh-radio/README.md` — target: STM32L072
- **Constitutional purpose:** the 433 MHz LoRa radio plane — PHY/MAC configuration,
  regional duty-cycle compliance, and link-layer behavior for the sovereign mesh.
- **Maps to:** compliance requirement — Nigerian 433 MHz band regulation; the AEGIS-NG
  falsifiability claim (end-to-end alert delivery across ≥ 4-tier hops under 70% packet
  loss).
- **Will live here:** radio parameter tables, duty-cycle budgets, link-budget
  calculations per node type.
- **Governing agent/phase:** Agent 02; co-reviewed by Agent 05 for spectrum compliance.

### `firmware/F-03-sensor-acquisition/README.md` — target: STM32L072
- **Constitutional purpose:** deterministic sensor sampling and signal conditioning for
  the safety-sensing node types; sampling is a contract (fixed rates, fixed filters), not
  a heuristic.
- **Maps to:** compliance requirement — measurement integrity for safety evidence;
  falsifiability support (sensor contracts are preconditions of the alert-delivery claim).
- **Will live here:** per-node-type sensor contracts, calibration records, sampling
  tables.
- **Governing agent/phase:** Agent 02; calibration evidence witnessed by Agent 06.

### `firmware/F-04-edge-ai/README.md` — target: ESP32-S3 — **INFINITE Agent 03 mapping**
- **Constitutional purpose:** the edge intelligence plane. **This subsystem maps to
  INFINITE Agent 03 (ML / Edge AI Engineer), who governs it co-equally with Agent 02.**
  It hosts the six TFLite Micro edge models **M-01 through M-06**, executes on-device
  inference on the ESP32-S3, and participates in federated learning with differential
  privacy (ADR-004) so that model improvement never requires citizen data to leave its
  jurisdiction. Model languages: Hausa, Fulfulde, Igbo, Yoruba, Efik.
- **Maps to:** patent claim PPA-003 (federated edge learning with differential privacy —
  FILED); compliance requirement — DP bounds on information leakage; grant deliverable —
  edge-AI milestones for `doj-ojjdp/` (youth safety inference at the edge) and
  `mozilla-ford-foundation/` (open, privacy-preserving ML).
- **Will live here:** model cards and versioning pins for M-01…M-06, TFLite Micro
  integration contracts, federated-round protocols, per-model DP-budget ledgers,
  language-coverage matrices for the five supported languages.
- **Governing agent/phase:** **Agent 03 (ML / Edge AI Engineer)** governs; Agent 02
  co-signs embedded integration; Agent 05 audits DP budgets; models frozen at release
  gates.

### `firmware/F-05-crdt-sync/README.md` — targets: ESP32-S3 + ESP32-C3
- **Constitutional purpose:** node-side offline CRDT synchronization — mesh nodes merge
  divergent state without connectivity (ADR-003), guaranteeing eventual consistency with
  the CLAI-OS hub across zero-bandwidth intervals (18h guarantee).
- **Maps to:** patent claim PPA-004 (FILED); twin of `clai-os/deterministic/crdt-sync/`;
  compliance requirement — data residency (sync without foreign infrastructure).
- **Will live here:** node-side CRDT specifications, merge invariants, bandwidth-budget
  tables, soak-test protocols shared with the hub twin.
- **Governing agent/phase:** Agent 02 with Agent 04 (hub twin); per-release merge proofs.

### `firmware/F-06-anti-tamper-enclosure/README.md` — targets: all three
- **Constitutional purpose:** tamper detection, response, and evidence preservation —
  enclosure intrusion, voltage glitching, and debug-port abuse trigger deterministic
  response and signed evidence, never silent failure.
- **Maps to:** patent claim PPA-001 (anti-tamper architecture — FILED); compliance
  requirement — physical-security attestations for sovereign deployments; grant
  deliverable — custodial-safety evidence for `doj-ojjdp/`.
- **Will live here:** tamper-event taxonomies, response state machines, signed-evidence
  schemas, anti-tamper test harness specifications.
- **Governing agent/phase:** Agent 05 (Security Auditor) governs; Agent 02 implements.

### `firmware/F-07-secure-bootloader/README.md` — targets: all three
- **Constitutional purpose:** root of trust on every MCU — verified boot chains so that
  only S50-signed firmware executes, on STM32L072, ESP32-S3, and ESP32-C3 alike.
- **Maps to:** compliance requirement — supply-chain and update integrity; S50 signature
  law extended to silicon.
- **Will live here:** boot-chain specifications, key-ceremony records, rollback-protection
  parameters per target.
- **Governing agent/phase:** Agent 05 governs; Agent 02 implements; key ceremonies are
  S50-gated events.

### `firmware/F-08-ota-update/README.md` — target: ESP32-C3
- **Constitutional purpose:** over-the-air update distribution over the 433 MHz mesh —
  update images propagate hop-by-hop to nodes that may never see the internet, with
  signature verification before activation.
- **Maps to:** patent claim PPA-004 support (offline-first distribution); compliance
  requirement — patchability is a sovereign-maintenance obligation.
- **Will live here:** update-image formats, mesh-propagation protocols, activation and
  rollback contracts.
- **Governing agent/phase:** Agent 02; Agent 05 verifies signatures; Agent 06 schedules
  field rollouts.

### `firmware/F-09-hmi-alerts/README.md` — target: ESP32-S3
- **Constitutional purpose:** human-machine interface and local alerting — audible/visual
  alarm logic, multilingual alert presentation in the five supported languages, and
  accessibility constraints for low-literacy field conditions.
- **Maps to:** grant deliverable — community-usability evidence for `unicef-innovation/`
  and `doj-ojjdp/`; compliance requirement — alert comprehensibility is part of the
  safety case.
- **Will live here:** alert taxonomies, language asset index (Hausa, Fulfulde, Igbo,
  Yoruba, Efik), accessibility test protocols.
- **Governing agent/phase:** Agent 02; Agent 06 validates in field drills.

### `firmware/F-10-data-logger-storage/README.md` — target: STM32L072
- **Constitutional purpose:** tamper-evident local logging — append-only event storage on
  the node so that every alert, tamper event, and sync round is reconstructable from the
  node alone, consistent with the audit anchoring doctrine (ADR-005).
- **Maps to:** compliance requirement — evidentiary logging for sovereign audit; patent
  claim PPA-001 support (evidence preservation).
- **Will live here:** log schemas, retention/rotation contracts, integrity-sealing
  specifications.
- **Governing agent/phase:** Agent 02; Agent 05 audits log integrity.

### `firmware/F-11-diagnostics-watchdog/README.md` — target: ESP32-C3
- **Constitutional purpose:** self-diagnostics and watchdog supervision across the mesh —
  nodes report health, detect sibling-node silence, and escalate degradation before it
  becomes outage.
- **Maps to:** the AEGIS-NG falsifiability claim (mesh resilience is measurable only if
  health telemetry exists); grant deliverable — operations-readiness evidence.
- **Will live here:** health-metric definitions, watchdog contracts, escalation matrices.
- **Governing agent/phase:** Agent 02; Agent 06 consumes health telemetry in the field.

### `firmware/F-12-field-provisioning/README.md` — target: ESP32-C3
- **Constitutional purpose:** secure commissioning — a node is born in the field: identity
  issuance, LGA binding, key injection, and enrollment into the mesh without any
  connection back to the architect (sovereignty test, transfer policy).
- **Maps to:** compliance requirement — recipient-nation autonomy; grant deliverable —
  transfer-completeness evidence for `aegis-global/` certification graduates.
- **Will live here:** provisioning ceremonies, identity schemas, LGA registry bindings
  for the 12 deployment LGAs.
- **Governing agent/phase:** Agent 06 (Field Deployment) governs ceremonies; Agent 02
  implements; Agent 05 witnesses key injection.

## 3. Hardware Leaf READMEs

### `hardware/README.md`
- **Constitutional purpose:** root of the hardware plane — everything needed for a
  recipient nation to fabricate all 14 node types from open catalogs, blueprints never
  black boxes.
- **Maps to:** patent claim PPA-001; sovereign transfer policy (open BOM, $46.30/node);
  grant deliverables for manufacturing-transfer milestones.
- **Will live here:** the four subdirectories below only.
- **Governing agent/phase:** Agent 01 (Hardware Engineer); frozen at release gates.

### `hardware/nodes/README.md`
- **Constitutional purpose:** the index of all **14 node types, N-A01 through N-D02** —
  one registry, not fourteen divergent forks. Series: N-A01…N-A04 sensing nodes,
  N-B01…N-B04 relay nodes, N-C01…N-C04 hub/gateway nodes, N-D01…N-D02 command and display
  nodes. Each node type binds to its firmware subsystems (F-01…F-12 subset), its MCU
  target, and its BOM line-set.
- **Maps to:** patent claim PPA-001; grant deliverable — node-type coverage matrices for
  deployment grants; falsifiability support (the $46.30 BOM claim is per node type).
- **Will live here:** the node registry (type → role → MCU → firmware subset → BOM),
  variant rules, deprecation log.
- **Governing agent/phase:** Agent 01 governs; Agent 02 co-signs firmware bindings.

### `hardware/schematics/README.md`
- **Constitutional purpose:** complete schematic sources for all 14 node types — the
  readable form of the hardware constitution; every net is inspectable, nothing is
  obfuscated.
- **Maps to:** patent claim PPA-001 (drawing support); sovereign transfer policy
  (blueprints, not product imports); grant deliverable for `india-dst/` and
  `african-development-bank/` local-manufacture milestones.
- **Will live here:** schematic sources per node type, design-rule records, review
  sign-offs.
- **Governing agent/phase:** Agent 01; reviews co-signed by Agent 05 (anti-tamper nets).

### `hardware/gerber/README.md`
- **Constitutional purpose:** fabrication outputs (Gerber/drill/pick-and-place) pinned per
  release — the exact files a recipient nation sends to JLCPCB or a local fab, versioned so
  a field unit can always be traced to its fabrication data.
- **Maps to:** grant deliverable — manufacturing pipeline reproducibility
  (`aegis-global/manufacturing/` consumes these); compliance requirement — supply-chain
  traceability.
- **Will live here:** per-node-type, per-release fabrication packages with SHA-256 pins.
- **Governing agent/phase:** Agent 01; release pins are S50-gated.

### `hardware/bom/README.md`
- **Constitutional purpose:** the published bills of materials — **$46.30 per node**,
  sourced entirely from open LCSC/JLCPCB catalogs, with alternates so no single part
  shortage can hold a nation hostage.
- **Maps to:** the AEGIS-GLOBAL falsifiability claim (any deployment whose
  field-maintainable components cannot be sourced at or below the published BOM cost
  forfeits the designation); patent claim PPA-001 support; grant deliverable — cost
  evidence for every infrastructure target.
- **Will live here:** per-node-type BOMs, alternates tables, price-snapshot log, the
  $46.30 cost model cross-reference to `aegis-global/manufacturing/cost-model/`.
- **Governing agent/phase:** Agent 01; price snapshots refreshed each phase; Agent 07
  cites in applications.

## 4. Mesh Leaf READMEs

### `mesh/README.md`
- **Constitutional purpose:** root of the mesh-network plane — the 433 MHz LoRa topology,
  protocols, and deployment geography that make the nodes a system rather than a parts
  list.
- **Maps to:** the AEGIS-NG falsifiability claim (≥ 4-tier hop delivery under 70% packet
  loss); ADR-002 (4-Tier Sovereign Mesh).
- **Will live here:** the three subdirectories below only.
- **Governing agent/phase:** Agent 02 with Agent 06; continuous.

### `mesh/topology/README.md`
- **Constitutional purpose:** topology doctrine and per-site designs — the 4-tier relay
  architecture (ADR-002) instantiated per deployment, bounding blast radius and latency
  simultaneously.
- **Maps to:** ADR-002; the mesh falsifiability claim; grant deliverable — coverage
  plans cited by `doj-ojjdp/` (facility perimeters) and `african-development-bank/`
  (community scale).
- **Will live here:** tier-design rules, per-site topology plans, hop/latency budgets.
- **Governing agent/phase:** Agent 02 designs; Agent 06 validates on site.

### `mesh/protocols/README.md`
- **Constitutional purpose:** mesh protocol specifications above the radio layer —
  routing, alert prioritization, store-and-forward behavior, and the CRDT sync transport
  that carries F-05 traffic.
- **Maps to:** patent claim PPA-004 support; compliance requirement — deterministic
  alert-priority behavior is part of the safety case.
- **Will live here:** protocol specifications, state machines, conformance test matrices.
- **Governing agent/phase:** Agent 02; conformance tests run at every release gate.

### `mesh/lga-deployments/README.md`
- **Constitutional purpose:** the deployment registry for the **12 Nigerian LGAs** — one
  record per LGA binding topology, node census (by N-type), spectrum parameters, and
  sync health.
- **Maps to:** compliance requirement NDPR (deployment locality records); grant
  deliverable — deployment-evidence milestones for Nigerian and multilateral funders;
  F-12 provisioning registry bindings.
- **Will live here:** twelve LGA deployment records, census tables, coverage maps.
- **Governing agent/phase:** Agent 06 governs; Agent 05 audits records.

## 5. Field-Ops Leaf READMEs

### `field-ops/README.md`
- **Constitutional purpose:** root of the field-operations plane — the doctrine by which
  hardware becomes safety in real communities, operated by local engineers without
  recourse to the architect.
- **Maps to:** sovereign transfer policy (sovereignty test); grant deliverables —
  operational-readiness evidence portfolio-wide.
- **Will live here:** the four subdirectories below only.
- **Governing agent/phase:** Agent 06 (Field Deployment Lead); continuous.

### `field-ops/deployment-playbooks/README.md`
- **Constitutional purpose:** step-by-step deployment playbooks — site acceptance, node
  placement, commissioning (with F-12), and handover to local operators.
- **Maps to:** grant deliverable — repeatable-deployment evidence for `doj-ojjdp/` and
  `unicef-innovation/`; transfer-policy completeness.
- **Will live here:** playbooks, checklists, acceptance forms.
- **Governing agent/phase:** Agent 06; drilled with `training-drills/`.

### `field-ops/lga-site-surveys/README.md`
- **Constitutional purpose:** pre-deployment survey records for each of the 12 LGAs —
  RF environment, solar insolation, security posture, and community liaison notes that
  drive topology design.
- **Maps to:** compliance requirement — deployment due diligence; feeds
  `mesh/topology/` and `mesh/lga-deployments/`.
- **Will live here:** survey instruments, per-LGA survey records, risk registers.
- **Governing agent/phase:** Agent 06; surveys precede any deployment tranche.

### `field-ops/maintenance-logs/README.md`
- **Constitutional purpose:** the maintenance record — every field intervention logged so
  that fleet health is auditable and MTBF claims are evidence, not assertion.
- **Maps to:** grant deliverable — operations-sustainability evidence; falsifiability
  support (maintenance data feeds the resilience claims).
- **Will live here:** log schemas, per-LGA maintenance records, fleet-health rollups.
- **Governing agent/phase:** Agent 06; Agent 09 samples for evaluation metrics.

### `field-ops/training-drills/README.md`
- **Constitutional purpose:** drill scenarios for local operators and AEGIS-GLOBAL
  certification candidates — alert response, tamper response, sync-failure response —
  so competence is demonstrated before it is needed.
- **Maps to:** grant deliverable — training evidence supporting the certification
  curriculum (`aegis-global/curriculum/`); compliance requirement — operator
  competence is part of the safety case.
- **Will live here:** drill scripts, scoring rubrics, drill records.
- **Governing agent/phase:** Agent 06; co-designed with Agent 09 (metrics alignment).

## Falsifiability Test

**Gate question for `aegis-ng`:** from directory names alone, can a systems engineer (a)
enumerate the 12 firmware subsystems and state each one's MCU target, (b) locate the edge
models M-01…M-06 in exactly one place (`F-04-edge-ai/`) and name its governing agent
(Agent 03), (c) find the fabrication path schematics → gerber → BOM and the $46.30 cost
anchor, and (d) trace a deployment from site survey → topology → LGA registry →
maintenance log?

Test procedure: a cold reviewer performs (a)–(d) using names and first-lines only. Any
subsystem whose name does not predict its content (e.g., a name hiding which MCU it
targets) is renamed before the next S50 gate. **Invalidation condition:** if any firmware
subsystem is found hosting artifacts belonging to another subsystem's constitutional
purpose — in particular, if any TFLite Micro model M-01…M-06 is found outside
`F-04-edge-ai/` — the subsystem boundary is void and this tree's release signature is
revoked pending re-partition.
