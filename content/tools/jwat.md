---
title: "JWAT"
description: "Workload characterization from log data."
screenshots:
  - thumb: "/img/sshots/jwat1.png"
    full: "/img/sshots/jwat1.png"
    caption: "Input data customization"
  - thumb: "/img/sshots/jwat2.png"
    full: "/img/sshots/jwat2.png"
    caption: "Input scatter plot"
  - thumb: "/img/sshots/jwat3.jpg"
    full: "/img/sshots/jwat3.jpg"
    caption: "K-means clustering"
  - thumb: "/img/sshots/jwat4.png"
    full: "/img/sshots/jwat4.png"
    caption: "Clustering info"
---

JWAT allows workload analysis using clustering techniques. Input data can be
collected from any kind of textual file: support for standard apache log files
is provided but users can specify customized formats. During the input phase,
users can provide the following extraction criteria:

- **All**: selects every observation
- **Interval**: selects only observations in a given range
- **Random**: given number of observations, selects that number at random from
  data
- **N every K**: picks at random N observations every K observations in input
  file (K>N)

The application supports a complete environment for statistical analysis. In
that environment it is possible to calculate univariate and bivariate
statistics and to draw frequency, quantiles and scatter plots.

Data can be normalized with the following transformations:

- Logarithmic
- Minimum-Maximum
- Standard deviation

and trimmed to a selected percentile.

Clustering is performed with the following algorithms:

- K-means
- Fuzzy

JWAT provides also an interface to the similarity clustering tool
[CLUTO](http://www.cs.umn.edu/~karypis/cluto). This is important for workloads
including qualitative data.

Data analysis is guided with a *wizard* interface.
