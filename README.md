# Crop Allocation Optimisation — Linear Programming (Excel Solver)

> LP model for **optimal crop allocation** using **Excel Solver**, maximising farm revenue subject to land, labour, water and demand constraints. Includes full sensitivity analysis with shadow-price interpretation.
>
> ** Operations Analytics**

---

## 🎯 Problem

A farm must decide how many hectares to allocate to each crop to **maximise total revenue** (or profit), given constraints on:

- **Available land** (total hectares)
- **Labour hours** per crop per season
- **Water / irrigation** capacity
- **Minimum / maximum demand** commitments per crop
- Non-negativity of all decision variables

## 🧮 LP Formulation

```text
Maximise   Z = Σ (revenue_per_hectare_i × hectares_i)

Subject to
  Σ hectares_i          ≤ Total land available
  Σ (labour_i × hectares_i)  ≤ Labour hours available
  Σ (water_i × hectares_i)   ≤ Water capacity
  hectares_i            ≥ 0   for all i
  (+ demand cap constraints per crop)
```

## 📈 Results

- Optimal allocation determined via **Simplex LP** in Excel Solver
- Shadow-price analysis identifies which resource constraints are binding
- Sensitivity report shows allowable increase / decrease ranges for RHS and objective coefficients
- Scenario analysis explores impact of relaxing binding constraints

### Shadow-Price Insights

- Binding constraints identified with their shadow prices (marginal value of one additional unit of resource)
- Non-binding constraints identified with their slack values
- Allowable ranges provided for strategic planning

## 🧰 Tech Stack

`Microsoft Excel` · `Solver` (Simplex LP) · Sensitivity Report · Answer Report

## 📁 Repo Structure

```text
.
├── Report/                    # Full written analysis and interpretation
├── Solved File/               # Pre-configured Solver workbook
├── LICENSE
└── README.md
```

## ▶️ How to Use

1. Open the workbook in `Solved File/` using **Microsoft Excel**
2. Navigate to `Data` → `Solver` — parameters are already configured
3. Click **Solve** to reproduce the optimal crop allocation
4. Review the Sensitivity and Answer reports for shadow-price interpretation

## 📄 Report

Full solution with LP formulation, Solver output, sensitivity analysis and strategic recommendations → see `Report/` directory.

---

<sub>MIT-licensed · Author: [Parth Badiger](https://github.com/parthbadiger24-creator)</sub>
