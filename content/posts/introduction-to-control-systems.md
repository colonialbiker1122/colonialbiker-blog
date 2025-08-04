+++
date = '2025-08-04T22:32:27+05:30'
draft = false
title = 'Introduction to Control Systems'
+++
## Introduction
System: Collection of interconnected parts that form a larger more complex whole

3 different problems
1. System identification problem
  - Determine mathematical problem
  - Ask following questions:
    - How can I model the system that I’m trying to control ?
    - What are the relevant dynamics/
    - What equation will convent known inputs to measured outputs?
    - i. Black box method
    - ii. White box method
2. Simulation problem
  - Predicting how outputs change
  - Ask the following questions:
    - Does my system model match my test data?
    - Will my system work in all operating environments?
    - How my system behaves with potentially destructive commands?
3. Control problem
  - How do we generate the appropriate system input that will produce the desired output?
  - Ask the following questions:
    - How can I get my system to meet my performance requirements?
    - How can I automate a process that currently involves humans in the loop?
    - How can my system operate in a dynamic and noisy environment?

## Miscellaneous
- Open Loop System
- Closed Loop System

- Control system: Mechanism that alters behaviour (future state) of a system towards a desired state

- Transfer function: Laplace transform of the impulse response of a linear, time-invariant system with a single input and single output when you set the initial conditions to 0. They allow us to connect several systems in series by performing convolution through simple multiplication.

- Transfer functions require that you have an LTI system
- LTI : Linear and time invariant system
- LTI allowable operations:
  - Multiply/ divide by constant: a.x(t)
  - Integrate/ differentiate input
  - Add/ subtract multiple inputs: x1(t) + x2(t)
- LTI systems have following properties:
  - Homogeneity: If Input scaled, Output also scaled
  - Superposition
  - Time-invariance: Same behaviour regardless of when in time the action takes place
- Impulse function : Dirac delta function:
