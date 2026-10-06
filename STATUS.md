# STATUS.md — AEGIS-NG Honest-Absence Roadmap

**What this file is:** the public record of what does *not yet* exist in this
repository. AEGIS-NG is released progressively under governance gates; rather
than staging empty directories or placeholder files, every planned subsystem is
listed here by name, with a one-line description of what it will contain. Each
entry is marked `PENDING — progressive public release` until its artifacts land,
at which point the entry is removed and the directory appears in the tree.

**Rule:** an absence listed here is a commitment, not a gap. An absence *not*
listed here does not exist anywhere in the program.

Last updated: initial public mirror release.

---

## Firmware Plane (`firmware/`) — 12 subsystems, F-01 … F-12

| Subsystem | Target MCU | Status | Will contain |
|-----------|-----------|--------|--------------|
| `F-01-power-management` | STM32L072 | PENDING — progressive public release | Solar-only power autonomy: MPPT charge control, battery stewardship, brownout survival, and per-node-type energy budgets so no node ever requires grid power. |
| `F-02-lora-mesh-radio` | STM32L072 | PENDING — progressive public release | The 433 MHz LoRa radio plane: PHY/MAC configuration, regional duty-cycle compliance, and link-layer behavior for the sovereign mesh. |
| `F-03-sensor-acquisition` | STM32L072 | PENDING — progressive public release | Deterministic sensor sampling and signal conditioning for safety-sensing node types; sampling as a contract (fixed rates, fixed filters), with calibration records. |
| `F-04-edge-ai` | ESP32-S3 | PENDING — progressive public release | The edge intelligence plane: six TFLite Micro models (M-01…M-06), on-device inference, and federated learning with differential privacy in Hausa, Fulfulde, Igbo, Yoruba, and Efik. |
| `F-05-crdt-sync` | ESP32-S3 + ESP32-C3 | PENDING — progressive public release | Node-side offline CRDT synchronization: merge invariants and bandwidth budgets guaranteeing eventual consistency with the CLAI-OS hub across 18h zero-bandwidth intervals (twin of `clai-os/deterministic/crdt-sync/`). |
| `F-06-anti-tamper-enclosure` | all three targets | PENDING — progressive public release | Tamper detection, deterministic response, and signed evidence preservation for enclosure intrusion, voltage glitching, and debug-port abuse — never silent failure. |
| `F-07-secure-bootloader` | all three targets | PENDING — progressive public release | Root of trust on every MCU: verified boot chains ensuring only governance-signed firmware executes, with key-ceremony records and rollback protection per target. |
| `F-08-ota-update` | ESP32-C3 | PENDING — progressive public release | Over-the-air update distribution over the 433 MHz mesh: hop-by-hop propagation to nodes that may never see the internet, with signature verification before activation. |
| `F-09-hmi-alerts` | ESP32-S3 | PENDING — progressive public release | Human-machine interface and local alerting: audible/visual alarm logic, multilingual alert presentation in the five supported languages, and accessibility constraints for low-literacy field conditions. |
| `F-10-data-logger-storage` | STM32L072 | PENDING — progressive public release | Tamper-evident local logging: append-only event storage so every alert, tamper event, and sync round is reconstructable from the node alone. |
| `F-11-diagnostics-watchdog` | ESP32-C3 | PENDING — progressive public release | Self-diagnostics and watchdog supervision across the mesh: health telemetry, sibling-node silence detection, and degradation escalation before outage. |
| `F-12-field-provisioning` | ESP32-C3 | PENDING — progressive public release | Secure commissioning: field-born node identity issuance, LGA binding, key injection, and mesh enrollment without any connection back to the architect. |

## Hardware Plane (`hardware/`)

| Subsystem | Status | Will contain |
|-----------|--------|--------------|
| `bom` | PENDING — progressive public release | The published bills of materials (USD 46.30 per node reference cost), sourced from open LCSC/JLCPCB catalogs, with alternates tables and price-snapshot log. |
| `gerber` | PENDING — progressive public release | Fabrication outputs (Gerber/drill/pick-and-place) pinned per release with SHA-256, traceable from any field unit back to its fabrication data. |
| `nodes` | PENDING — progressive public release | The registry of all 14 node types (N-A01…N-D02): type → role → MCU → firmware subset → BOM bindings, variant rules, and deprecation log. |
| `schematics` | PENDING — progressive public release | Complete schematic sources for all 14 node types — every net inspectable, nothing obfuscated. |

## Mesh Plane (`mesh/`)

| Subsystem | Status | Will contain |
|-----------|--------|--------------|
| `topology` | PENDING — progressive public release | Topology doctrine and per-site designs: the 4-tier relay architecture instantiated per deployment, bounding blast radius and latency simultaneously. |
| `protocols` | PENDING — progressive public release | Mesh protocol specifications above the radio layer: routing, alert prioritization, store-and-forward behavior, and the CRDT sync transport carrying F-05 traffic. |
| `lga-deployments` | PENDING — progressive public release | The deployment registry for the 12 Nigerian LGAs: one record per LGA binding topology, node census (by N-type), spectrum parameters, and sync health. |

## Deliberately Absent

- `patents/defensive-publications/` — **withheld: pre-disclosure legal review
  pending.** The archived defensive publication (AEGIS-NG-DEFPUB-v2.0-S51)
  referenced in [PATENTS.md](PATENTS.md) remains private until that review
  completes.
- `field-ops/` — field-operations doctrine (deployment playbooks, LGA site
  surveys, maintenance logs, training drills) is retained in the private
  repository pending operational-security review of real deployment geography.


## Deployment Agent Corpus — AEGIS-GLOBAL Track (2026-10-06)

The AEGIS-GLOBAL deployment agent corpus (v2.0/v3) is canonical: ten specialist
agents (AEGIS-DEPLOY-01..10) spanning sovereign manufacturing, field deployment,
threat audit, supply chain, lawful interoperation, funding, certification,
training, patent prosecution, and master orchestration. Agents are licensed
Savant-Commercial-1.0 — public catalog, SIP trigger matrix, and SHA-256
existence-commitments live in
[savant-prompts](https://github.com/SAVANT-FRAMEWORK/savant-prompts) and the
[agent stack documentation](https://savant-framework.github.io/savant-docs/agents/).
Full RASCEF bodies remain commercial.

Governance: PRIME → S1 → S50 → S52. Sovereignty invariant: open-architecture
sovereignty transfer, not product export. Safety invariant: no
surveillance-as-a-service, no predictive policing, no foreign data extraction.

---

*Entries are removed from this file only in the commit that lands the
subsystem's artifacts. This file is the honesty mechanism of the progressive
public release.*
