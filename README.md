# AEGIS-NG

**The sovereign hardware and node-infrastructure instantiation of the SAVANT
FRAMEWORK** — an offline-first, solar-only, 433 MHz LoRa safety mesh that a
recipient nation can fabricate, deploy, and operate without recourse to the
original architect.

Author and sole IP holder: **Dr. Christabel Odeta** — Nigerian systems architect,
systems engineer, LLM engineer, prompt engineer.

---

## What AEGIS-NG Is

AEGIS-NG is sovereign safety infrastructure: a mesh of ultra-low-cost hardware
nodes providing store-and-forward safety alerting with no dependence on cellular
or internet infrastructure. Blueprints, not black boxes — every schematic, BOM,
and firmware subsystem is organized so that local engineers can manufacture and
maintain the full system in-territory.

Canonical facts:

- **14 hardware node types, N-A01 … N-D02** — sensing nodes (N-A series), relay
  nodes (N-B), hub/gateway nodes (N-C), and command/display nodes (N-D), indexed in
  one registry, never forked.
- **12 firmware subsystems, F-01 … F-12** — from solar power management and the
  433 MHz LoRa mesh radio to secure boot, OTA update over the mesh, anti-tamper
  response, and field provisioning, across STM32L072, ESP32-S3, and ESP32-C3
  targets.
- **433 MHz LoRa mesh, offline-first** — 4-tier sovereign mesh architecture with
  store-and-forward alerting designed to hold delivery-rate floors under heavy
  packet loss and node churn.
- **Edge AI with privacy by construction** — six TFLite Micro edge models
  (M-01 … M-06) with federated learning and differential privacy, operating in
  Hausa, Fulfulde, Igbo, Yoruba, and Efik; citizen data never leaves its
  jurisdiction.
- **Offline CRDT sync** — node-side conflict-free replication guaranteeing
  eventual consistency with the CLAI-OS clinical hub across 18-hour
  zero-bandwidth intervals.
- **Humanitarian deployment tiers T1–T4** — from national/regional infrastructure
  down to community-level deployment, with field provisioning ceremonies that
  bind nodes to their Local Government Area at commissioning.
- **Open fabrication economics** — a published per-node bill of materials
  (USD 46.30 reference cost) sourced from open LCSC/JLCPCB catalogs, with
  alternates so no single part shortage can hold a deployment hostage.
- **Patent posture** — AEGIS-NG embodies filed provisional applications PPA-001,
  PPA-003, and PPA-004 (of the framework's five filed PPAs; PPA-006 is planned,
  not filed). See [PATENTS.md](PATENTS.md) for the enabling-level public
  abstracts and the defensive-publication strategy.

## Status — Read This First

This repository is an **engineering artifact in progressive public release**. The
governance instruments, licensing, patent abstracts, and architecture published
here are complete and canonical. The firmware, hardware, and mesh artifacts
themselves are released progressively under governance gates;
[STATUS.md](STATUS.md) is the honest-absence roadmap: every planned subsystem is
listed by name and marked `PENDING — progressive public release` until its
artifacts land. Nothing here pretends to be what it is not.

## Repository Contents

| Path | Contents |
|------|----------|
| [LICENSE](LICENSE) | Dual license: AGPL-3.0 OR Savant-Commercial-1.0 |
| [GOVERNANCE.md](GOVERNANCE.md) | Constitutional governance (SPOS / SIP / S50 gates) |
| [TRADEMARK.md](TRADEMARK.md) | Trademark policy |
| [DCO.md](DCO.md) | Developer Certificate of Origin |
| [PATENTS.md](PATENTS.md) | Defensive-publication strategy + PPA-001…005 public abstracts; PPA-006 gap disclosure |
| [STATUS.md](STATUS.md) | Honest-absence subsystem roadmap |
| [docs/architecture/00-master-tree.md](docs/architecture/00-master-tree.md) | Five-repository sovereign-deployment master tree |
| [docs/architecture/aegis-ng-tree.md](docs/architecture/aegis-ng-tree.md) | AEGIS-NG directory architecture and subsystem contracts |

## Planned Subsystem Planes (see STATUS.md)

- `firmware/` — the 12 subsystems F-01 … F-12 (the embedded plane)
- `hardware/` — node registry, schematics, gerber fabrication packages, BOMs (the fabrication plane)
- `mesh/` — topology doctrine, mesh protocols, LGA deployment registry (the network plane)

## Ecosystem

| Resource | Link |
|----------|------|
| Organization | https://github.com/SAVANT-FRAMEWORK |
| Documentation | https://savant-framework.github.io/savant-docs/ |
| Live demo | https://savant-framework.github.io/savant-demo/ |
| Prompt library | https://github.com/SAVANT-FRAMEWORK/savant-prompts |
| Companion clinical engine | CLAI-OS (clinical cognition engine; CRDT-sync twin) |

## Contributing

Contributions are accepted under [DCO.md](DCO.md) sign-off and the governance
process in [GOVERNANCE.md](GOVERNANCE.md). All safety-affecting changes pass
through the deterministic-first falsifiability gates described in the
architecture documents.

## Licensing

AEGIS-NG is dual-licensed: **AGPL-3.0** for the open layer, or
**Savant-Commercial-1.0** for commercial deployments. Patent rights in PPA-001
through PPA-005 flow to AGPL-3.0 users per AGPL-3.0 Section 11 and are
extinguished for any party instituting patent litigation against the project.
Sovereign humanitarian deployers under the technology-transfer carve-out receive
a no-fee covenant not to sue for in-territory non-commercial manufacture and use.
See [LICENSE](LICENSE) and [PATENTS.md](PATENTS.md).

---

*AEGIS-NG is a constitutional instantiation of the SAVANT FRAMEWORK. The private
development repository will be renamed `aegis-ng-internal`; this is the canonical
public mirror.*
