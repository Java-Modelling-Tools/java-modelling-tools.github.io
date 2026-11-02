---
title: "JSIMwiz"
description: "Queueing network and Petri net simulator with wizard-based user interface."
screenshots:
  - thumb: "/img/sshots/jsim1s.png"
    full: "/img/sshots/jsim1.png"
    caption: "Classes definition"
  - thumb: "/img/sshots/jsim2s.png"
    full: "/img/sshots/jsim2.png"
    caption: "Stations definition"
  - thumb: "/img/sshots/jsim3s.png"
    full: "/img/sshots/jsim3.png"
    caption: "Performance indices definition"
  - thumb: "/img/sshots/jsim4s.png"
    full: "/img/sshots/jsim4.png"
    caption: "Finite capacity regions definition"
  - thumb: "/img/sshots/jsim5s.png"
    full: "/img/sshots/jsim5.png"
    caption: "Simulation process"
  - thumb: "/img/sshots/jsim6s.png"
    full: "/img/sshots/jsim6.png"
    caption: "What-if analysis"
---

JSIMwiz is the GUI front-end to the JMT simulation engine. It allows the
solution of open, closed or mixed queuing networks, stochastic Petri nets, and
queueing Petri nets. Arrival rates for open classes and service times for
stations can be randomly generated with the following distributions:

- Constant
- Erlang
- Exponential
- Gamma
- Hyperexponential
- Normal
- Pareto
- Poisson
- Student-T
- Uniform
- Burst (General)
- Burst (MMPP2)

The following strategies are available for queuing:

- First Come First Served
- First Come First Served with priority
- Last Come First Served
- Last Come First Served with priority
- Shortest job first
- Longest job first

While routing can be specified with the following strategies:

- Fastest service
- Least utilization
- Probability
- Random
- Round robin
- Join the shortest queue (JSQ)
- Shortest response time

Some interesting additional features are:

- Load dependent service time strategies
- Support for parallelism via fork-join components
- Support for finite capacity regions
- Automated support for what-if analysis
- Customization of default values
- Modular architecture based on Java reflection that allows the introduction
  of new classes into the simulation engine without any modification to other
  classes code
- Import/Export to and from [JMVA](/tools/jmva/)

Users will have an immediate graphical feedback of the selected performance
indices during simulation and the engine will perform automatic on-line
statistical analysis of measured indices to discard the initial transient and
calculate confidence intervals.

Model definition is guided with a *wizard* interface.
