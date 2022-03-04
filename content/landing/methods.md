---
title: "Methods"
date: 2022/03/03 11:37
weight: 100
style: hg2
---


{{<box class="feat">}}
# Updating semantics

Qualitative models provide logical rules controlling the activity level of each component. The updating
semantics further defines the application of these rules, especially when the level of multiple components
can be updated in the current state.

Deterministic semantics (e.g. [synchronous](updatings/synchronous)) define a single successor. They are
convenient for simulations but could generate artefactual behaviours due to their strong kinetic assumptions.

Non-deterministic semantics (e.g. [asynchronous](updatings/asynchronous) or [permissive](updatings/permissive))
provide a collection of alternative trajectories to capture the incertainty often associated to qualitative models.
They are more likely to generate realistic biological behaviours, but it can be burried among a large number of
trajectories (some artefactual) and they are more difficult to simulate.


See the [list of updating semantics](updatings).
{{</box>}}



{{<box class="feat">}}
# Simulations

Simulations provide a natural way to evaluate the dynamical behaviour of a qualitative model by defining an
initial state and applying the update functions.

**Deterministic**: [Traces](simulation/trace) or [continuous view](simulation/continuous).

**Non-deterministic**: [State Transition graph](simulation/stg) or [stochastic sampling](simulation/stochastic).

{{</box>}}

{{<box class="feat">}}
# Static analysis

Static analysis methods provide some dynamical informations without performing explicit simulations,
which is especially useful for large models where classical simulations become untractable.
These methods are well suited for the identification (or at least approximation) of attractors
(representing stable phenotypes) and some reachability properties.

See the [list of static analysis methods](static).
{{</box>}}

