# First Order Scalar Nonlinear Control System

## Overview

This repository contains the implementation of a **First Order Scalar Nonlinear Control System** using adaptive control techniques. The system aims to track a desired trajectory while simultaneously estimating the unknown parameters of the system.

The control system uses a combination of **proportional feedback** and an **adaptive mechanism** for parameter estimation. The desired trajectory is a nonlinear function of time, and the system is able to adjust its control input to minimize the tracking error. The system is modeled and solved using MATLAB's ODE solver (`ode45`), which simulates the dynamics over time.

## Key Features
- **Scalar Nonlinear System**: The system state is a single variable (position) that evolves over time according to a nonlinear differential equation.
- **Adaptive Control**: The system adapts its estimates of unknown parameters using an adaptive gain approach.
- **Trajectory Tracking**: The system aims to track a desired trajectory composed of sinusoidal functions.
- **ODE Solver**: The system dynamics are solved using MATLAB's `ode45` solver for high accuracy.

## Files
- `main.m`: The main MATLAB script that defines the system dynamics, solves the ODE, and generates the results.
- `Dynamics.m`: Defines the dynamics of the system, including the control law and the parameter estimation update rule.

## Requirements
To run this project, you will need:
- MATLAB (R2018 or later recommended)
- MATLAB's `ode45` solver

## How It Works
1. **System Definition**: The system is defined by a second-order nonlinear differential equation, where the state variables are the position (`x(t)`), and two parameter estimates (`a_hat` and `b_hat`).
2. **Control Input**: The control input (`u(t)`) is calculated using the tracking error and the estimated parameters.
3. **Parameter Estimation**: The parameters `a` and `b` are unknown to the system, but are estimated over time using an adaptive algorithm.
4. **Simulation**: The system is simulated over a time span `[0, 100]` with an initial condition, and the results are plotted for analysis.

## Results
The script generates four plots:
1. **System state vs. Desired trajectory**: Shows the actual state of the system and how well it tracks the desired trajectory.
2. **Parameter estimates (`a_hat`) vs. True value**: Compares the estimated value of `a` over time with its true value.
3. **Parameter estimates (`b_hat`) vs. True value**: Compares the estimated value of `b` over time with its true value.
4. **Control input**: Displays the control input (`u(t)`) used to drive the system.

## Example Output

The following is an example of the results produced by the system after running the simulation:

- The first plot shows how the system tracks the desired trajectory.
- The second and third plots show the convergence of the estimated parameters (`a_hat` and `b_hat`) to their true values.
- The fourth plot shows how the control input changes over time to minimize the tracking error.


## License
This project is licensed under the MIT License
