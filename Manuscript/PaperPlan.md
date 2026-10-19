# Paper Plan: Network Games, Group Inverses, and Comparative Statics

## 1. Reading-based summary of the underlying idea

I reviewed the thesis abstract in the extracted PDF and the main themes are consistent with the following research program:

- network centrality is central to the analysis;
- eigenvector centrality and matrix-based centrality measures are the key objects;
- equilibrium behavior is studied when network structure is fixed;
- the author uses recent matrix derivative methods to study equilibria and centrality measures; and
- the design objective is to derive comparative statics in network games and network systems.

The natural extension for a journal paper is to make the role of the group inverse explicit: in a network game or linear-quadratic network system, the relevant equilibrium mapping often takes the form

A x = b + B \Delta,

or more generally a fixed-point system with Jacobian J(x;G) that is singular or near-singular at the equilibrium. The group inverse J^{\#} provides a canonical generalized inverse that is useful for comparative statics when standard inverses fail because the Jacobian is singular or has a unit eigenvalue. The paper can build around using J^{\#} to compute equilibrium multipliers, response elasticities, and welfare effects from small changes in link strength, network structure, or external shocks.

## 2. Research question

How can group-inverse methods be used to characterize and compute comparative statics in network games and network-embedded economic systems where equilibrium conditions feature a singular or nearly singular Jacobian?

The paper will answer this by combining:

- network structure;
- equilibrium characterization;
- generalized inverse methods; and
- welfare and comparative static analysis.

## 3. Proposed contribution

The paper contributes a tractable analytical framework for equilibrium comparative statics in networks using the group inverse. The core contribution is not merely to compute derivatives numerically, but to show that the group inverse provides economically interpretable network multipliers: it measures how equilibrium actions, prices, or welfare respond to perturbations in network links and node-specific fundamentals.

The intended contribution is threefold:

1. Formalize the equilibrium system in a network setting.
2. Derive comparative statics via the group inverse of the Jacobian.
3. Connect the results to policy and welfare analysis in a way suitable for a theory journal.

## 4. Proposed model

### 4.1 Network and actions

Let the network be represented by a weighted adjacency matrix G or W, with entries w_{ij} denoting connection strength between nodes i and j. A set of agents i = 1, ..., n choose actions x_i. The equilibrium condition is

x = F(x, G, z),

where z is a vector of primitives or shocks.

A simpler and more elegant version for a theory paper is a linear-quadratic network game:

u_i(x_i, x_{-i}; G, z) = a_i x_i - (1/2)b_i x_i^2 + \sum_j w_{ij} x_i x_j + z_i x_i,

or in reduced form an equilibrium condition of the form

(I - M(G)) x = c(G,z).

When I - M(G) is singular or nearly singular, the standard inverse is unavailable and the group inverse becomes the natural object.

### 4.2 Group inverse as the key object

Let

J(G,z) = I - \partial F / \partial x

or the relevant Jacobian of the equilibrium mapping. If det J = 0 or J is singular at the candidate equilibrium, then the generalized inverse J^{\#} is used to compute equilibrium responses:

\frac{\partial x^*}{\partial \theta} = -J^{\#} \frac{\partial J}{\partial \theta} x^* + J^{\#} \frac{\partial c}{\partial \theta}.

This formula is the core technical object of the paper.

The paper will emphasize that the group inverse is not a technical curiosity but the relevant network multiplier: it captures the propagation of perturbations through the network while respecting the singularity induced by network feedback.

## 5. Main analytical results to target

The paper should aim to establish the following results:

1. Existence and uniqueness (or local uniqueness) of equilibrium under network regularity conditions.
2. Characterization of the Jacobian and its spectral properties.
3. Formulae for comparative statics using the group inverse.
4. Conditions under which network externalities amplify or dampen responses.
5. Welfare interpretation of comparative statics.
6. A tractable application to public goods, production networks, or contagion-type interactions.

## 6. Proposed structure of a 30-page body

### Section 1: Introduction (3-4 pages)

- Motivation, economic relevance of networks.
- Why standard inverse methods fail in network equilibrium models.
- The group inverse as a general solution to comparative statics in singular systems.
- Contribution and related literature.

### Section 2: Model Setup and Network Geometry (4-5 pages)

- Graph and adjacency matrix.
- Node-level strategic environment.
- Equilibrium mapping and network externalities.
- Statement of regularity conditions.

### Section 3: Centrality, Network Structure, and the Group Inverse (4-5 pages)

- Link to eigenvector centrality.
- Jacobian structure in terms of network matrices.
- Why group inverses arise naturally from redundant directions in the equilibrium system.

### Section 4: Equilibrium Characterization (4-5 pages)

- Existence and comparative static environment.
- Derive equilibrium conditions.
- Analyze the role of the null space and network feedback loops.

### Section 5: Comparative Statics via the Group Inverse (6-8 pages)

- Derive the main formula for d x^* / d \theta using J^{\#}.
- Analyze link-strength perturbations.
- Analyze node-level fundamentals and policy shocks.
- Conclude with network multiplier formulas.

### Section 6: Welfare and Policy (4-5 pages)

- Welfare effects of network changes.
- Planner problem or policy intervention.
- Tax/subsidy or network-design interpretation.

### Section 7: Applications and Discussion (3-4 pages)

- Application to local public goods, information networks, or production networks.
- Interpretation and constraints.
- Discussion of empirical or numerical implementation.

### Section 8: Conclusion (1-2 pages)

- Summarize main message and possible extensions.

Target total body length: roughly 30 pages (excluding figures and references).

## 7. Proposed appendix structure (around 40 pages)

### Appendix A: Proofs of the main propositions (12-15 pages)

- Proposition 1: equilibrium existence.
- Proposition 2: properties of J^{\#}.
- Proposition 3: comparative static formula.
- Proposition 4: welfare derivative formula.

### Appendix B: Matrix calculus and generalized inverses (10-12 pages)

- matrix derivative identities;
- group inverse properties;
- singular Jacobian decompositions;
- network spectral decomposition.

### Appendix C: Computational and numerical methods (6-8 pages)

- algorithm to compute J^{\#};
- numerical stability considerations;
- examples for small networks.

### Appendix D: Additional examples and calibration details (8-10 pages)

- stylized networks;
- counterexamples or knife-edge cases;
- robustness to link heterogeneity.

### Appendix E: Supplementary welfare and policy derivations (5-7 pages)

- planner first-order condition;
- translation to practical policy instruments.

Total appendix length: about 40 pages.

## 8. Target journal fit

This project is well aligned with journals such as:

- Journal of Economic Theory (JET)
- Public Economic Theory
- Games and Economic Behavior
- Economic Theory

The best fit is a theory-heavy paper that emphasizes:

- clear equilibrium characterization;
- elegant generalized-inverse methods; and
- sharp comparative static propositions with policy interpretation.

## 9. Suggested title options

1. Network Games, Group Inverses, and Comparative Statics
2. Comparative Statics in Network Games with Singular Jacobians
3. Centrality, Generalized Inverses, and Equilibrium Responses in Networks
4. Group-Inverse Multipliers in Network Equilibrium Models
5. Network Externalities, Spectral Structure, and Group Inverse Comparative Statics

## 10. Recommended drafting sequence

1. Draft the model and notation.
2. Prove the equilibrium characterization and Jacobian decomposition.
3. Write the key proposition for J^{\#} comparative statics.
4. Add the welfare theorem.
5. Then add one application and policy section.
6. Fill appendices after the main model is complete.

## 11. Immediate next step

The next concrete step is to create a LaTeX skeleton for the paper in the Manuscript folder and begin drafting the title, abstract, introduction, and model sections in the actual document.
