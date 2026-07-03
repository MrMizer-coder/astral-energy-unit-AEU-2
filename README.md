Overview
The Astral Energy Unit (AEU) is the core micro‑commodity of the Astral Protocol. It represents a cryptographically‑verified unit of energy contribution within the Astral Grid — compute, storage, or physical energy — and serves as the foundation for allocation, emissions, governance weighting, and settlement across the ecosystem.

This repository contains the AEU ledger, metering logic, allocation models, and integration hooks used by Astral Grid nodes, the ACC, and the Astral Dashboard.

Key Features
AEU Ledger
Deterministic balance tracking

Merkle‑proof‑ready state structure

Node‑level and workload‑level accounting

Hooks for on‑chain settlement

Energy Metering
Compute → AEU conversion

Storage → AEU conversion

Physical energy → AEU conversion

Configurable multipliers and epoch‑based adjustments

Allocation & Emissions
Daily emission model

Epoch‑based distribution

Curve‑driven emission schedules

Governance‑weighted allocation

Governance
AEU → voting power conversion

Proposal lifecycle

Delegation hooks

Integration with ASTRAL governance

Integrations
Astral Grid node adapters

ACC workload metering

Dashboard analytics adapters

Settlement worker pipelines

Repository Structure
Code
astral-energy-unit-AEU-2/
│
├── core/
│   ├── ledger/
│   │   ├── aeu_ledger.ts
│   │   ├── balances.ts
│   │   ├── proofs.ts
│   │   └── index.ts
│   ├── metering/
│   │   ├── energy_capture.ts
│   │   ├── compute_meter.ts
│   │   ├── storage_meter.ts
│   │   └── index.ts
│   └── index.ts
│
├── allocation/
│   ├── emissions/
│   │   ├── daily_emission.ts
│   │   ├── epoch_model.ts
│   │   └── curves.ts
│   ├── governance/
│   │   ├── voting_power.ts
│   │   ├── proposals.ts
│   │   └── index.ts
│   └── index.ts
│
├── services/
│   ├── api/
│   │   ├── rest/
│   │   ├── graphql/
│   │   └── index.ts
│   ├── workers/
│   │   ├── meter_worker.ts
│   │   ├── settlement_worker.ts
│   │   └── index.ts
│   └── index.ts
│
├── contracts/
│   ├── AEU.sol
│   ├── EnergyLedger.sol
│   ├── Allocation.sol
│   └── Governance.sol
│
├── integrations/
│   ├── dashboard/
│   │   ├── hooks.ts
│   │   ├── adapters.ts
│   │   └── index.ts
│   ├── astral-grid/
│   │   ├── node_adapter.ts
│   │   ├── workload_meter.ts
│   │   └── index.ts
│   └── index.ts
│
├── docs/
│   ├── AEU_spec.md
│   ├── allocation_model.md
│   ├── governance.md
│   ├── settlement.md
│   └── api_reference.md
│
└── tests/
AEU Token Model
AEU is designed to be:

Auditable — deterministic ledger + proofs

Composable — integrates with ASTRAL token and ACC

Fair — emission curves reward real contribution

Scalable — supports millions of node‑level events

AEU is not a currency — it is a unit of contribution, similar to:

compute credits

energy certificates

micro‑commodity units

Integration Points
Astral Grid
Nodes meter workloads → workloads produce AEU → AEU settles into ledger.

ACC (Astral Compute Controller)
ACC sends workload metadata → metering converts → ledger updates.

Dashboard
Provides:

real‑time AEU balances

emission projections

governance weight

settlement history

Development
Install
Code
npm install
Build
Code
npm run build
Test
Code
npm test
License
MIT License — open for public use, modification, and integration.
