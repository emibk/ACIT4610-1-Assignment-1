# ACIT4610-1-Assignment-1

# README



## Vehicle Routing Problem with Genetic Algorithm (GA)



### Project Description

This project implements a Genetic Algorithm (GA) to solve the Vehicle Routing Problem (VRP).

The VRP involves finding efficient routes for a fleet of vehicles to serve a set of customers starting and ending at a central depot.



Our GA-based solver:

- Minimizes the total Euclidean travel distance across all routes,




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

- No time-window or vehicle-capacity constraints.



---



### GA Design



- Representation:
&nbsp; Each individual is represented by route and vehicles, through a list [route, vehicles]

&nbsp; Route is a permutation of customer locations (indices)

&nbsp; Vehicles represent which vehicle goes to a specific customer location.



- Operators:

&nbsp; Selection: Rank-based selection

&nbsp; Crossover: Route crossover + vehicles crossover.

&nbsp; Route crossover: swapping two customer locations at random. 

&nbsp; Vehicles crossover: uniform crossover.

&nbsp; Mutation: Route mutation or vehicles mutation.

&nbsp; Vehicles mutation: random resetting - In each position, with a probability, replace with a new vehicle value, from the list of admissible values.

&nbsp; Route mutation: swap two random locations.

&nbsp; Elitism: Best individuals(top 2 parents) carried over each generation



- Termination: Fixed number of generations.



---



### GA Parameter Sets

We test parameters, for two instances, of each scenario:



\- Set A: Population 15, Generations 70, Crossover 0.90, Mutation 0.10

\- Set B: Population 25, Generations 85, Crossover 0.80, Mutation 0.30

\- Set C: Population 40, Generations 100, Crossover 0.70, Mutation 0.05



Each test is over 20 runs of the algorithm.


---



### Performance Metrics

We measure:

- Solution quality (best, average, worst fitness per test) over 20 runs

- Runtime (seconds) - worst, average, worst over 20 runs

- Plot convergence (fitnesses per generation)




---



### How to Run



1. Install Python (>=3.9 recommended).

2. Install dependencies:

&nbsp;  pip install numpy matplotlib
&nbsp; pip install numpy

3. The notebook is split into two main parts:
   1. Step-by-step walkthrough:
   - This section demonstrates how the solution was developed.
   - Not required to be run to produce final results.
   2. Final algorithm
   - Contains the final GA implementation.
   - You can run only this part to generate the results.



---



### Repository Structure

Assignment1.ipynb     # notebook version (all code in cells)


README.md               # this file





---



### Notes

- Results may differ slightly on each run due to GA randomness.

- For reporting, we include best, average, and worst results from several runs (not just a single run).




---



### Authors

- Group 4 Lara Hassanieh, Nicoleta Emilia Chisim and Hemen Waisi

- OsloMet – ACIT 4610, Fall 2025



