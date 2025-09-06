# ACIT4610-1-Assignment-1

\# README



\## Vehicle Routing Problem with Genetic Algorithm (GA)



\### Project Description

This project implements a Genetic Algorithm (GA) to solve the Vehicle Routing Problem (VRP).

The VRP involves finding efficient routes for a fleet of vehicles to serve a set of customers starting and ending at a central depot.



Our GA-based solver:

\- Minimizes the total Euclidean travel distance across all routes,

\- Ensures that each customer is visited exactly once,

\- Splits customer permutations into routes using dynamic programming (DP) to optimally assign vehicles.



The implementation is written in Python as a single Jupyter-compatible script (spaghetti style).



---



\### Problem Scenarios

We test three groups of scenarios, each with two instances:



\- Small: 2–10 vehicles, 10–20 customers

\- Medium: 11–25 vehicles, 15–30 customers

\- Large: 26–50 vehicles, 20–50 customers



For the large group, we use 35 vehicles and 40 customers (per assignment requirements).



---



\### Objective

\- Minimize total travel distance across all vehicles.

\- Every vehicle route starts and ends at the depot.

\- Every customer must be visited exactly once.

\- No time-window or vehicle-capacity constraints (simplified VRP).



---



\### GA Design



\- Representation:

&nbsp; Customers are represented as a permutation (list of indices).

&nbsp; Routes are split using a DP-based segmentation algorithm that assigns customers optimally across the available vehicles.



\- Operators:

&nbsp; - Selection: Tournament selection

&nbsp; - Crossover: Order Crossover (OX)

&nbsp; - Mutation: Swap mutation

&nbsp; - Elitism: Best individuals carried over each generation



\- Termination: Fixed number of generations.



---



\### GA Parameter Sets

We test three parameter sets as required:



\- Set A: Population 60, Generations 150, Crossover 0.90, Mutation 0.20

\- Set B: Population 100, Generations 120, Crossover 0.85, Mutation 0.10

\- Set C: Population 60, Generations 220, Crossover 0.90, Mutation 0.30



Each scenario is tested with all three parameter sets, repeated three trials each.



---



\### Performance Metrics

We measure:

\- Solution quality (best, average, worst distance per setting),

\- Runtime (seconds),

\- Convergence (best distance per generation),

\- Best generation where the optimum was found.



Outputs:

\- outputs/results\_raw.csv -> all trial data

\- outputs/results\_summary.csv -> aggregated best/avg/worst results

\- outputs/convergence\_\[scenario]\_\[param].png -> convergence plots

\- outputs/routes\_\[scenario].png -> best route visualization



---



\### How to Run



1\. Install Python (>=3.9 recommended).

2\. Install dependencies:

&nbsp;  pip install numpy matplotlib

3\. Open the Jupyter notebook or run the spaghetti .py file.

&nbsp;  In Jupyter/VS Code:

&nbsp;  - Use Run All Cells.

&nbsp;  - Results will be written to the outputs/ folder.



---



\### Repository Structure

assignment1 final.ipynb     # notebook version (all code in cells)

assignment1 final.py        # optional script version

README.md               # this file

outputs/

&nbsp;   results\_raw.csv

&nbsp;   results\_summary.csv

&nbsp;   convergence\_small\_1\_A.png

&nbsp;   convergence\_small\_1\_B.png

&nbsp;   ...

&nbsp;   routes\_small\_1.png

&nbsp;   ...



---



\### Notes

\- Results may differ slightly on each run due to GA randomness.

\- For reporting, we include best, average, and worst results from several runs (not just a single run).

\- Large scenarios (35 vehicles × 40 customers) may take longer — adjust population size and generations if needed on slower machines.



---



\### Authors

\- Group 4 Lara Hassanieh, Nicoleta Emilia Chisim and Hemen Waisi

\- OsloMet – ACIT 4610, Fall 2025



