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
