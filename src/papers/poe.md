---
title: Identifiability of Product of Experts Models
date: 2024-04-18
topics: ["Causal Inference", "Algebraic Geometry"]
publication: Proceedings of AISTATS
authors: Manav Kant, Eric Y Ma, Andrei Staicu, Leonard J Schulman, Spencer Gordon
---

Product of experts (PoE) are layered networks in which the value at each node is an AND (or product) of the values (possibly negated) at its inputs. These were introduced as a neural network architecture that can efficiently learn to generate high-dimensional data which satisfy many low-dimensional constraints-thereby allowing each individual expert to perform a simple task. PoEs have found a variety of applications in learning. We study the problem of identifiability of a product of experts model having a layer of binary latent variables, and a layer of binary observables that are iid conditional on the latents. The previous best upper bound on the number of observables needed to identify the model was exponential in the number of parameters. We show: (a) When the latents are uniformly distributed, the model is identifiable with a number of observables equal to the number of parameters (and hence best possible). (b) In the more general case of arbitrarily distributed latents, the model is identifiable for a number of observables that is still linear in the number of parameters (and within a factor of two of best-possible). The proofs rely on root interlacing phenomena for some special three-term recurrences.

[PMLR](https://proceedings.mlr.press/v238/kant24a.html)
[arXiv](https://arxiv.org/abs/2310.09397)