# ⚡ E-Scoot Charging Network Optimization

## 📌 Business Overview
Efficient "Last Mile" transportation is critical for modern campuses and smart cities. This project applies **Operations Research** techniques to design the charging infrastructure for an E-Scooter fleet at Arizona State University. The goal was to solve the **Facility Location Problem**: deciding *where* to build stations and *how many* chargers to install to minimize cost.

## 🧮 Mathematical Model (MILP)
We formulated the problem as a **Mixed-Integer Linear Program**:

* **Objective Function:** Minimize Total Cost (Fixed Construction Cost + Variable Charger Cost).
* **Decision Variables:**
    * $y_i$ (Binary): 1 if a station is built at location $i$, 0 otherwise.
    * $x_i$ (Integer): Number of chargers installed at location $i$.
* **Constraints:**
    * $\sum$ Capacity $\ge$ Demand (Demand Satisfaction).
    * $\sum$ Cost $\le$ $35,000 (Budget Constraint).
    * Residential Coverage $\ge$ 70% (Equity Constraint).

## 📈 Key Outcomes
1.  **Budget Optimization:** The model identified a solution costing **$28,350**, successfully saving $6,650 while meeting all strict service requirements.
2.  **Strategic Selection:** Out of 8 potential sites, the solver prioritized high-traffic hubs (e.g., *Sun Devil Fitness Center*) and dense residential dorms (*Hassayampa*), rejecting low-ROI locations.
3.  **Scalability:** The Python/Gurobi framework allows for instant re-calculation if budget or demand parameters change in the future.

<img width="534" height="270" alt="image" src="https://github.com/user-attachments/assets/96f164d0-37f2-43cd-b919-5fb872311652" />

## 🛠 Tools Used
* **Python:** Gurobi Optimizer (`gurobipy`), Pandas.
* **Excel:** Solver (for prototype validation).
* **Visualization:** Network maps and cost analysis charts.

## 🚀 How to Run
1.  Clone the repository.
2.  Install Gurobi License (or use the limited trial).
3.  Run `M6 Python E-Scoot Optimization.ipynb`.
