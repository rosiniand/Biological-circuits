# Biological-circuits
Study of simple biological logical circuits via stochastic simulations

---
* Statistical Physics and Biophysics
* Politecnico di Torino
* Academic Year 2024/2025
---

## Aim of the project
Implement the **Gillespie Algorithm** to simulate the stochastic dynamics of simple gene regulatory circuits and analyse their emergent behaviour in terms of noise, bistability and oscillations.

## Contents

### `julia/`
Stochastic simulations written in Julia using the Gillespie algorithm.

| Notebook | Description |
|----------|-------------|
| `Gillespie_single_gene.ipynb` | Baseline model: single gene with constitutive expression |
| `Gillespie-feedback.ipynb` | Auto-regulatory negative/positive feedback loop |
| `Gillespie-forward_loop.ipynb` | Feed-forward loop (coherent and incoherent) |
| `Gillespie-separated.ipynb` | Two-species separated circuit with interaction |

## Methods
The **Gillespie Direct Method** (SSA) is used to generate exact trajectories of the Chemical Master Equation (CME). Each circuit is modelled as a set of biochemical reactions with propensity functions derived from mass-action kinetics. Observables such as mRNA/protein distributions, noise (Fano factor, CV) and switching times are computed from the simulated trajectories.

## Dependencies
- **Julia** ≥ 1.9
- `Catalyst.jl`, `JumpProcesses.jl` — reaction network definition and SSA
- `Plots.jl`, `StatsBase.jl` — visualisation and statistics
