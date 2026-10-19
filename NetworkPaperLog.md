# NetworkPaper project log

## Current objective

Build a technical economic theory paper on networks and comparative statics, using the group inverse as the core analytic device. The paper is intended to fit the style of journals such as JET or Public Economic Theory, with a main body of roughly 30 pages and appendices of around 40 pages.

## Reading and idea development

We reviewed the extracted thesis PDF in the Manuscript folder (`Manuscript/thesis.pdf`) and identified the central themes that matter for this project:

- network centrality and eigencentrality;
- fixed-network equilibrium analysis;
- matrix-derivative methods;
- comparative statics in network systems;
- generalized inverses when the equilibrium Jacobian is singular or nearly singular.

The key conceptual direction is to frame the paper around the group inverse of the equilibrium Jacobian. In this setting, standard inverse formulas break down when the system has a zero eigenvalue or redundant directions due to network feedback. The group inverse is then used to characterize equilibrium responses to shocks and network perturbations.

## Current modelling approach

The paper is being built around a network game or networked strategic system of the form:

- agents choose actions `x_i` in a networked environment;
- the network is represented by a weighted adjacency or influence matrix `G` (or `W`);
- equilibrium conditions are summarized by `x = F(x, G, z)` or a reduced form like `(I - M(G))x = c(G, z)`;
- the relevant Jacobian is `J(G, z) = I - \partial F / \partial x` or an equivalent equilibrium operator;
- when `J` is singular or near-singular, the group inverse `J^{#}` is used to compute comparative statics.

The core formula under development is of the form:

`d x^* / d theta = - J^{#} (dJ/dtheta) x^* + J^{#} (dc/dtheta)`,

which is the candidate technical object from which the paper derives comparative statics, network multipliers, and welfare effects.

## Work completed to date

1. Created the project structure:
   - `Manuscript/`
   - `Numerics/`
   - `Data/`
   - `Thesis/`
2. Created the root project log file: `NetworkPaperLog.md`.
3. Extracted the thesis PDF into the manuscript folder for reference (`Manuscript/thesis.pdf`).
4. Reviewed the thesis abstract and relevant sections to identify the underlying theory.
5. Drafted a research plan in `Manuscript/PaperPlan.md`.
6. Created a LaTeX manuscript scaffold in `Manuscript/main.tex`.
7. Created the section and appendix skeleton files under `Manuscript/sections/` and `Manuscript/appendices/`.
8. Verified the draft LaTeX skeleton compiles successfully as `Manuscript/main.pdf`.

## Proposed paper structure

Main body (around 30 pages):

1. Introduction
2. Model and network geometry
3. Centrality, network structure, and the group inverse
4. Equilibrium characterization
5. Comparative statics via the group inverse
6. Welfare and policy implications
7. Application
8. Conclusion

Appendices (around 40 pages):

- proofs of main propositions;
- matrix calculus and generalized inverses;
- numerical methods and implementation;
- examples and robustness checks.

## Planned next steps

1. Draft the introduction and model section in LaTeX.
2. Formalize the equilibrium system and state regularity conditions.
3. Prove the main comparative-static proposition using the group inverse.
4. Derive welfare implications and policy interpretations.
5. Add one tractable application (public goods, production networks, or information diffusion).
6. Expand appendices with proofs and matrix identities.
7. Prepare the final manuscript for submission-style formatting.

## Repository status

The project is currently staged and pushed to GitHub under the repository:

`https://github.com/julian-williams31/NetworkPaper`

The manuscript work is being developed in the `Manuscript/` directory, with the theory and drafting materials stored in the project repository.
