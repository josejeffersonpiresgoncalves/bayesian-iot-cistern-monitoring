# Bayesian Decision Architecture for Adaptive IoT Monitoring

This repository contains the artifacts associated with the paper:

**A Bayesian Decision Architecture for Adaptive IoT Monitoring under Energy, Connectivity, and Measurement Uncertainty**

accepted at **ISE 2026 – Intelligent Software Engineering Workshop**.

The repository provides the initial Bayesian Network specification, prior probabilities, conditional probability tables (CPTs), and the simulated scenarios used in the preliminary evaluation reported in the paper.

## Bayesian Network Structure

The proposed Bayesian Network contains five input nodes:

- `Cistern_Level`
- `Measurement_Uncertainty`
- `Precipitation`
- `Link_Quality`
- `Battery_Status`

Two intermediate nodes are inferred from these inputs:

- `Water_Risk`
- `Transmission_Viability`

The final output node is:

- `Operational_Decision`

The dependency structure is:

```text
Cistern_Level ───────────────┐
Measurement_Uncertainty ─────┼──> Water_Risk ───────────────┐
Precipitation ───────────────┘                               │
                                                            ├──> Operational_Decision
Link_Quality ────────────────┐                               │
                             ├──> Transmission_Viability ────┘
Battery_Status ──────────────┘
