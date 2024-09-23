# Numerical Methods for Solving Differential Equations in Predator-Prey Models

## Overview

This project focuses on solving differential equations to model the dynamics of predator-prey systems. Using various numerical methods, we aim to find the most accurate and efficient solver to simulate these models. The project evaluates two test cases provided, applying different computational methods.

### Problem Definition

The predator-prey model is described by the following system of differential equations:
dx/dt = αx − βxy + f(t) dy/dt = δxy − γy + g(t)

Where:
- `x(t)` represents the prey population,
- `y(t)` represents the predator population,
- `α, β, γ, δ` are positive constants,
- `f(t)` and `g(t)` are functions describing external migration.

### Test Cases

1. **Test Case 1**:
   - Parameter set: `α = β = γ = δ = 1`
   - Functions: 
     - `f(t) = −sin(t)− cos(t)^2 − cos(t)`
     - `g(t) = sin(t) + cos(t)^2 − cos(t)`
   - Initial conditions: `x(t=0) = 2`, `y(t=0) = 0`
   - Exact solution:
     - `x(t) = 1 + cos(t)`
     - `y(t) = 1 - cos(t)`

2. **Test Case 2**:
   - Parameter set: `α = 2/3, β = 4/3, γ = 1, δ = 1`
   - Functions: `f(t) = 0`, `g(t) = 0`
   - Initial conditions: `x(t=0) = 0.9`, `y(t=0) = 0.9`
   - The solution is not exact but repeats itself, with consistent population maxima over time.

### Methods

You are tasked with evaluating the following methods using the internal solver provided (`solvers.py`):

- **Heun's Method**
- **Ralston's Method**
- **Runge-Kutta**
- **SSPRK3**
- **Van der Houwen**
- **3/8-rule**

### Project Structure

- **Implementation**: 
  - The code is structured to allow running three selected methods for any set of initial conditions, time steps, and model parameters. 
- **Results**: 
  - Simulate and show the results for each test case across a range of time steps (`T/100`, `T/200`, `T/400`, `T/800`, `T/1600`).
  - The results focus on demonstrating the accuracy and efficiency of each method.
- **Analysis**: 
  - Analyze the efficiency and accuracy of each method and present your findings in both graphical and tabular formats.
- **Conclusion**: 
  - Recommend the best numerical method based on the comparison of accuracy, efficiency, and computational cost.

### Submission

Submit a Jupyter notebook containing:
- Code to run the simulations.
- Results for the test cases.
- Analysis and commentary on the methods.
- Markdown for documentation and explanations.

### Learning Outcomes

- Choose appropriate computational algorithms for solving differential equations, balancing accuracy and efficiency.
- Understand and measure errors in numerical algorithms.
- Implement and compare numerical algorithms for complex systems.

## References

For additional information on predator-prey models, you can refer to:
- [Wikipedia: Lotka-Volterra Equations](https://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra_equations)
- [Mathworld: Lotka-Volterra Equations](https://mathworld.wolfram.com/Lotka-VolterraEquations.html)

---

**Module Title**: Numerical Computation  
**Module Code**: COMP/XJCO2421  
**Assignment Type**: Final Coursework  
**Weighting**: 80%  
**Submission Deadline**: 2pm Wed 20 Dec
