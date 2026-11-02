---
title: "JSIMgraph"
description: "Queueing network and Petri net simulator with graphical user interface."
screenshots:
  - thumb: "/img/sshots/jmodel1s.png"
    full: "/img/sshots/jmodel1.png"
    caption: "Network topology definition"
  - thumb: "/img/sshots/jmodel2s.png"
    full: "/img/sshots/jmodel2.png"
    caption: "Classes definition"
  - thumb: "/img/sshots/jmodel3s.png"
    full: "/img/sshots/jmodel3.png"
    caption: "Service time distributions definition"
  - thumb: "/img/sshots/jmodel4s.png"
    full: "/img/sshots/jmodel4.png"
    caption: "Simulation queue animation"
  - thumb: "/img/sshots/jmodel5s.png"
    full: "/img/sshots/jmodel5.png"
    caption: "Simulation transient"
  - thumb: "/img/sshots/jmodel6s.png"
    full: "/img/sshots/jmodel6.png"
    caption: "What-if analysis"
---

JSIMgraph allows the design of a queuing network model or a stochastic Petri
net in a graphical way. The model can be solved either with simulation
techniques or, if the model is BCMP compliant, automatically exported to
[JMVA](/tools/jmva/) to be solved with exact or approximate MVA algorithms.

JSIMgraph provides all functionality of [JSIMwiz](/tools/jsimwiz/) plus:

- Creation of stations, links and grouping into blocking regions with drag and
  drop functionalities
- Queue animation during simulation process, providing smart information on
  queue (or place) state and utilizations
