---
title: "Formal Methods @ LaBRI"
subtitle: LaBRI - CNRS, Bordeaux INP, Univ Bordeaux (Talence, FR)
geolocation: 44.80827, -0.59652
summary: Formal methods and tools for the verification, control, and synthesis of Boolean networks
members: Loïc Paulevé
website: https://loicpauleve.name
---

We develop formal computer science methods and tools related to the semantics, verification, control, and synthesis of Boolean networks and related formalisms.
Our research interests include the following topics:

* Most Permissive Boolean networks ([Paulevé et al, 2020](https://doi.org/10.1038/s41467-020-18112-5)) which bring formal guarantees for the abstract modeling of quantitative systems. Moreover, they offer a much lower complexity than traditional (a)synchronous Boolean networks for verifying trajectories and attractors. They can address Boolean networks at the genome-scale, with several thousands of nodes.

* Reprogramming of Boolean networks to predict control strategies for driving a Boolean network from one attractor to another. With collaborators in theoretical and experimental biology, we investigate applications in cellular reprogramming. See  [notebooks for Boolean network reprogramming](https://github.com/algorecell/flavors-of-reprogramming).

* Synthesis (inference) of Boolean networks from architecture (influence graph) and dynamical properties using Answer-Set Programming. We are currently investigating applications to single-cell data of cellular differentiation processes.

We are involved in the [CoLoMoTo Docker environment and Interactive Notebook](/notebook). We develop the tools
[Pint](/software/pint/) devoted to the analysis of reachability in asynchronous automata networks;
[mpbn](/software/mpbn/) for the analysis of reachability and attractors in Most Permissive Boolean networks;
and [BoNesis](https://github.com/bioasp/bonesis/) for the synthesis of Most Permissive Boolean networks from architecture and dynamical properties.
