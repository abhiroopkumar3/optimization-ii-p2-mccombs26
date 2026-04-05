# Airline Overbooking: A Dynamic Programming Approach

Abhiroop Kumar · Arturo Juarez · Paolo Lopez Böttger · Thomas Garner

## Problem

An airline wants to find the optimal pricing and overbooking policy for a flight with 100 coach seats and 20 first-class seats. Using dynamic programming (backward induction), we maximize expected discounted profit over a 365-day selling horizon, accounting for stochastic demand and departure-day overbooking costs.

## Notebooks

| File | Description |
|------|-------------|
| `Optimization-II_Project2_G26_-_Analysis_Notebook__Final.ipynb` | Full group solution covering all 7 parts |
| `optimization2_project2.ipynb` | Arturo's individual solution |
| `parts1-3_tommy.ipynb` | Parts 1-3 solution (Tommy) |

## Parts

1. **Baseline (OB=5)** — DP with coach oversold by up to 5 seats; expected profit $41,909.75
2. **Optimal cap search** — Sweep OB limits 5–20; optimal is OB=9 at $42,171.35
3. **Flexible no-sale policy** — Add no-sale action, cap at 130 coach tickets; profit $42,177.14
4. **Sensitivity analysis** — OAT perturbation of all 5 sale probabilities ±5pp in 1pp steps; FC demand dominates
5. **Time-varying demand** — Demand scales by 0.75 + t/730; profit drops to ~$41,864 due to discounting of late sales
6. **Forward simulation** — 10,000 Monte Carlo runs validating Policy A (OB=9) and Policy B (No-Sale, OB=30)
7. **Executive summary** — Managerial recommendations comparing both policies

## Key Results

| Policy | DP Expected Profit | Simulated Mean |
|--------|--------------------|----------------|
| OB=5 (baseline) | $41,909.75 | — |
| OB=9 (optimal hard cap) | $42,171.35 | $42,183.65 |
| No-Sale, OB=30 (flexible) | $42,177.14 | ~$42,177 |
