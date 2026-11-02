---
title: "JMVA"
description: "Mean Value Analysis and approximate solution algorithms for queueing network models."
screenshots:
  - thumb: "/img/sshots/jmva1s.png"
    full: "/img/sshots/jmva1.png"
    caption: "Classes definition"
  - thumb: "/img/sshots/jmva2s.png"
    full: "/img/sshots/jmva2.png"
    caption: "Stations definition"
  - thumb: "/img/sshots/jmva3s.png"
    full: "/img/sshots/jmva3.png"
    caption: "Residence times definition"
  - thumb: "/img/sshots/jmva4s.png"
    full: "/img/sshots/jmva4.png"
    caption: "Synopsis panel"
  - thumb: "/img/sshots/jmva5s.png"
    full: "/img/sshots/jmva5.png"
    caption: "What-if analysis definition"
  - thumb: "/img/sshots/jmva6s.png"
    full: "/img/sshots/jmva6.png"
    caption: "What-if analysis graphical results"
---

JMVA is the GUI front-end to the JMT analytic engine. It allows the solution
of open, closed or mixed queuing networks with the exact or approximate MVA
algorithm with single or multiple customer classes. Service centres can be of
three types:

1. Load Independent
2. Load Dependent (currently supported only in single-class closed models)
3. Delay

JMVA allows the automated execution of *what-if analysis*, i.e. different
models are evaluated by changing a defined control parameter.

Model definition is guided with a *wizard* interface. Optionally, the created
model can be solved with the simulator by importing it into
[JSIM](/tools/jsimwiz/).
