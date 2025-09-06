# ACIT4610-1-Assignment-1



## Vehicle Routing Problem with Genetic Algorithm (GA)



### Project Description

The project implements a Genetic Algorithm (GA) to solve the Vehicle Routing Problem (VRP).

The VRP involves finding efficient routes for a fleet of vehicles to serve a set of customers starting and ending at a central depot.



Our GA-based solver minimizes the total Euclidean travel distance across all vehicles.



The implementation is written in Python as a single Jupyter Notebook.



---



### Problem Scenarios

We test three groups of scenarios, each with two instances:



- Small: 2–10 vehicles, 10–20 customers

- Medium: 11–25 vehicles, 15–30 customers

- Large: 26–50 vehicles, 20–50 customers






---



### Objective

- Minimize total travel distance across all vehicles.
- Every vehicle route starts and ends at the depot.
- Every customer must be visited exactly once.
- No time-window or vehicle-capacity constraints (simplified VRP).



---



### GA Design



- Representation:

&nbsp; Each individual is represented as a list with two parts: [route, vehicles]

&nbsp; A route is a permutation of customer locations

&nbsp; Vehicles list shows which vehicle goes to each customer



- Operators:

&nbsp; - Selection: Rank-based selection

&nbsp; - Crossover is crossover for routes + crossover for vehicles

&nbsp; - Crossover for routes: Order crossover 

&nbsp; - Crossover for vehicles: Uniform crossover 

&nbsp; - Mutation is mutation for route list or mutation for vehicles list

&nbsp; - Route mutation: randomly swap two customer locations

&nbsp; - Vehicles mutation: random resetting - in each position, with a probability, replace with a new vehicle value, from the list of admissible values

&nbsp; - Elitism: Best individuals (best 2 parents) carried over each generation



- Termination: Fixed number of generations.



---



### GA Parameter Sets

Each individual, for each scenario, is tested with the parameters: 



- Set A: Population 60, Generations 70, Crossover 0.90, Mutation 0.10

- Set B: Population 75, Generations 85, Crossover 0.80, Mutation 0.30

- Set C: Population 90, Generations 100, Crossover 0.70, Mutation 0.50






---



### Performance Metrics

- Runtime (seconds),

- Plot best fitness for each generations 


---



### How to Run



Install Python (>=3.9 recommended).

Install dependencies:

&nbsp;  pip install numpy matplotlib

&nbsp;  pip install numpy

This notebook has two parts:
1. Step-by-step walkthrough:
- Demonstrates how the solution was built.
- You can run all cells in order, but this is optional.
2. Final algorithm:
- The actual final code.
- You can skip the first part and run the cells in each section.



### Repository Structure

Assignment1.ipynb     # notebook version (all code in cells)


README.md               # this file



---



### Notes

- Results may differ slightly on each run due to GA randomness.




---



### Authors

- Group 4 Lara Hassanieh, Nicoleta Emilia Chisim and Hemen Waisi

- OsloMet – ACIT 4610, Fall 2025



