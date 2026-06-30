# Nonlinear System Modelling and Control using Physics-Based and Deep Learning Models

## Overview

This project investigates the modelling, identification, and control of a nonlinear rotary pendulum (ball-on-board/propeller-driven pendulum platform) by combining first-principles physics with modern deep learning techniques.

The objective is to accurately predict the nonlinear dynamics of the system and compare classical physics models with data-driven and hybrid approaches for simulation and Model Predictive Control (MPC).

The project includes nonlinear system identification, neural network modelling, recursive prediction, and real-time control using Model Predictive Control.

---

## Pendulum Reference

The rotary pendulum platform modelled in this project behaves as shown below. The animation illustrates the open-loop oscillation of the pendulum about its pivot point.

![Pendulum Oscillation](pendulum.gif)

**Behaviour modes:**

- [ ] **MPC OFF** — pendulum swings freely (open-loop oscillation, as shown in the GIF above)
- [x] **MPC ON** — controller actively drives the pendulum into closed-loop behaviour, stabilizing it at the reference set-point and rejecting disturbances in real time

> Toggling the MPC checkbox conceptually represents switching the system from open-loop (uncontrolled, free-swinging) dynamics to closed-loop (controlled, stabilized) dynamics. When MPC is enabled, the controller continuously predicts future states and computes optimal control inputs to counteract the natural oscillation seen in the GIF.

---

## Project Objectives

* Develop a nonlinear mathematical model from system dynamics.
* Implement numerical integration using the Runge–Kutta 4th Order (RK4) method.
* Build data-driven neural network models from experimental measurements.
* Develop a hybrid grey-box model by combining physics-based equations with neural network residual learning.
* Compare prediction accuracy of different modelling approaches.
* Implement Model Predictive Control (MPC) using the developed models.
* Evaluate controller performance for reference tracking and disturbance rejection.

---

## System Description

The nonlinear system consists of

* Rotary actuator
* Mechanical linkage
* Nonlinear pendulum dynamics
* Experimental sensors
* External control input

The system exhibits

* Nonlinear dynamics
* Coupled motion
* Friction effects
* Saturation
* Time-varying behaviour

making it an excellent benchmark for nonlinear modelling and advanced control algorithms.

---

## Modelling Approaches

### 1. Physics-Based Model

A nonlinear mathematical model is derived from the equations of motion.

Features:

* Nonlinear dynamics
* RK4 numerical integration
* Parameter-based simulation
* Interpretable physical model

---

### 2. Neural Network Model

A fully connected neural network is trained using experimental data to learn the nonlinear system behaviour.

Features:

* Data-driven modelling
* One-step prediction
* Recursive multi-step prediction
* Nonlinear approximation

---

### 3. Hybrid Grey-Box Model

The hybrid model combines

**Physics Prediction + Neural Network Residual Correction**

Advantages:

* Higher prediction accuracy
* Better generalization
* Improved robustness
* Reduced modelling error

---

## Model Predictive Control (MPC)

The developed models are integrated into an MPC framework.

The controller performs:

* Reference tracking
* Optimal control input computation
* Future trajectory prediction
* Constraint handling
* Closed-loop stabilization

The MPC repeatedly

1. Predicts future system behaviour.
2. Solves an optimization problem.
3. Applies the first control action.
4. Repeats the process at every sampling instant.

When MPC is active, the pendulum transitions from the free, open-loop oscillation shown in the GIF above to a controlled, closed-loop response that tracks the desired reference and rejects disturbances.

---

## Technologies Used

* Python
* PyTorch
* NumPy
* SciPy
* Matplotlib
* Jupyter Notebook

---

## Key Features

* Nonlinear system identification
* Physics-based modelling
* Deep learning models
* Hybrid grey-box modelling
* RK4 numerical integration
* Recursive prediction
* Residual learning
* Model Predictive Control
* Experimental data validation
* Performance comparison

---

## Results

The project compares

* Physics model
* Neural network model
* Hybrid grey-box model

using metrics such as

* Root Mean Square Error (RMSE)
* Prediction accuracy
* Recursive prediction performance
* Closed-loop tracking performance
* Control effort

The hybrid model demonstrated improved prediction performance by combining physical knowledge with data-driven learning.

---

## Future Improvements

Potential extensions include

* Neural Ordinary Differential Equations (Neural ODEs)
* Physics-Informed Neural Networks (PINNs)
* Real-time embedded MPC
* Adaptive MPC
* Reinforcement Learning based control
* State estimation using Kalman Filters
* Hardware-in-the-loop implementation

---

## Authors

* **Benedikt Hartmann**
* **Lalith**
* **Enrique Lewin**

Interested in

* Control Systems
* Machine Learning
* Robotics
* System Identification
* Embedded Intelligence
* Autonomous Systems
