# Hunting Friction v2 — Mathematical Core

**Status:** P0-D mathematical reconstruction  
**Governance:** SymC GOM v0.8.0 applies as guardrail only.  
**Scientific priority:** mathematics first; process is documented only where required for falsification, provenance, or reproducibility.

# 1. Research object

Hunting Friction v2 studies the mathematics of error correction in interacting reviewer networks.

The fundamental object is not a workflow score and not an assumed SymC coordinate. It is the evolution of a set of uncertain estimators under interaction, contradiction, evidence, and revision.

For atomic proposition or quantitative target (p), reviewer (i) carries a signed belief / estimate

[
x_{i,p}(t).
]

For binary claims, (xin[-1,1]) may encode stance in the sign and confidence in the magnitude.  
For quantitative claims, (xinmathbb R) is the estimate itself.

Known-truth testbeds provide target (y_p).

Define error

[
e_{i,p}(t)=x_{i,p}(t)-y_p.
]

The initial mathematical questions are:

1. how much independent information exists across reviewers;
2. how correlated their errors are;
3. how interaction changes the error field;
4. how disagreement energy evolves;
5. when interaction improves truth alignment;
6. when it destroys useful diversity;
7. whether the dynamics are first-order, second-order, nonlinear, or irreducibly high-dimensional;
8. only then, whether a defensible SymC-like modal coordinate emerges.

# 2. Static ensemble mathematics

Before modeling debate, quantify what is available before interaction.

Let the initial reviewer error vector be

[
mathbf e_0 =
egin{bmatrix}
e_1 & e_2 & cdots & e_N
end{bmatrix}^{mathsf T},
]

with covariance matrix

[
Sigma = operatorname{Cov}(mathbf e_0).
]

For equal-variance reviewers with pairwise error correlation (ho),

[
operatorname{Var}(ar e)
=
rac{sigma^2}{N}
left[1+(N-1)hoight].
]

Consequences:

- (ho=0): variance contracts as (1/N);
- (ho=1): adding reviewers gives no variance reduction;
- positive correlated error imposes a hard diversity ceiling;
- negative correlation can outperform the independent case.

For unbiased estimators, the minimum-variance linear aggregate satisfies

[
mathbf w^*
=
rac{Sigma^{-1}mathbf 1}
{mathbf 1^{mathsf T}Sigma^{-1}mathbf 1},
]

with

[
hat y_{mathrm{MV}}
=
{mathbf w^*}^{mathsf T}mathbf x.
]

This is an important native mathematical baseline. Interactive adversarial review must be compared against what can already be gained from optimal noninteractive aggregation.

# 3. Interaction network

Represent reviewer interaction by a weighted graph

[
G=(V,E,W).
]

Let

[
W_{ij}(t)ge 0
]

represent effective influence or attention from reviewer (j) to reviewer (i).

Define degree matrix

[
D_{ii}(t)=sum_j W_{ij}(t)
]

and graph Laplacian

[
L(t)=D(t)-W(t).
]

For one proposition, collect reviewer states into

[
mathbf x(t)=
egin{bmatrix}
x_1(t) & cdots & x_N(t)
end{bmatrix}^{mathsf T}.
]

A native measure of raw disagreement is the graph Dirichlet energy

[
mathcal F(t)
=
rac12mathbf x(t)^{mathsf T}L(t)mathbf x(t)
=
rac12sum_{i,j}W_{ij}(t)left(x_i(t)-x_j(t)ight)^2.
]

This is the initial mathematical meaning of **friction** in v2.

It measures network-weighted contradiction.

It does **not** use ground truth and therefore does not define success by construction.

# 4. Truth-aligned error energy

When truth is available, define

[
mathcal E(t)
=
rac12
left(mathbf x(t)-ymathbf 1ight)^{mathsf T}
Q
left(mathbf x(t)-ymathbf 1ight),
]

where (Qsucceq0) controls reviewer or claim weighting.

The one-step truth gain is

[
G(t)
=
mathcal E(t)-mathcal E(t+1).
]

Thus

- (G(t)>0): interaction improved truth alignment;
- (G(t)=0): no net truth gain;
- (G(t)<0): interaction made the group worse.

The central empirical object is therefore not friction alone, but the response surface

[
G=f(mathcal F,Sigma,L,	ext{evidence},	ext{confidence},	ext{task structure},ldots).
]

No monotonicity and no optimum are presumed.

# 5. First-order dynamics

The first dynamical candidate is a linear consensus-plus-evidence model:

[
dot{mathbf x}
=
-alpha Lmathbf x
+
Bmathbf u(t)
+
oldsymboleta(t),
]

or in discrete time,

[
mathbf x_{t+1}
=
A_tmathbf x_t
+
B_tmathbf u_t
+
oldsymboleta_t.
]

Here

- (L): interaction topology;
- (alpha): interaction susceptibility;
- (mathbf u(t)): new external evidence or independently generated reasoning;
- (B): evidence coupling;
- (oldsymboleta): stochastic/model noise.

For fixed (L), no external evidence, and (alpha>0),

[
rac{d}{dt}
left(
rac12mathbf x^{mathsf T}Lmathbf x
ight)
=
-alphamathbf x^{mathsf T}L^2mathbf x
le 0.
]

Ordinary consensus dynamics therefore dissipates disagreement.

That fact is mathematically important:

> reducing disagreement is not the same operation as reducing truth error.

A group can converge to the wrong answer.

The first-order model gives a clean null model for debate.

# 6. Spectral structure

Let

[
Lmathbf v_k=lambda_kmathbf v_k.
]

Expand

[
mathbf x(t)=sum_k z_k(t)mathbf v_k.
]

For first-order consensus,

[
dot z_k=-alphalambda_k z_k+u_k(t).
]

Each non-consensus mode decays with time scale

[
	au_k=rac{1}{alphalambda_k}.
]

The algebraic connectivity

[
lambda_2
]

controls the slowest nontrivial consensus mode in a connected graph.

This gives an immediate mathematical route to studying:

- isolated dissent;
- echo chambers;
- bottlenecks;
- excessive connectivity;
- topology-dependent correction;
- loss of useful heterogeneity.

# 7. Second-order candidate and the possible return of chi

A SymC-like damping coordinate is **not assumed**.

It becomes mathematically legitimate only if reviewer-state trajectories require a second-order model such as

[
ddot{mathbf x}
+
Gammadot{mathbf x}
+
Kmathbf x
=
Bmathbf u(t)
+
oldsymboleta(t).
]

If (Gamma=gamma I) and (K=L), then modal decomposition gives

[
ddot z_k
+
gammadot z_k
+
lambda_k z_k
=
u_k(t).
]

For each supported mode,

[
omega_k=sqrt{lambda_k},
]

and only then does the conventional damping ratio

[
chi_k
=
rac{gamma}{2sqrt{lambda_k}}
]

emerge naturally.

The associated characteristic roots are

[
r_{k,pm}
=
rac{-gammapmsqrt{gamma^2-4lambda_k}}{2}.
]

Thus

[
chi_k<1
]

corresponds to an underdamped mode,

[
chi_k=1
]

to a repeated-root critical boundary,

and

[
chi_k>1
]

to an overdamped mode.

But this interpretation is valid only if the second-order model is actually supported by reviewer-state trajectories and outperforms the first-order alternative on untouched data.

If first-order dynamics is sufficient, then Hunting Friction v2 has no justified damping-ratio chi.

# 8. Error-correction versus consensus

Let

[
mathbf e(t)=mathbf x(t)-ymathbf 1.
]

For a linear update without new evidence,

[
mathbf e_{t+1}=Amathbf e_t.
]

Truth error contracts only if the relevant induced dynamics contract the error:

[
|Amathbf e_t|_Q
<
|mathbf e_t|_Q.
]

Consensus alone guarantees no such thing.

This separates three mathematically distinct outcomes:

1. **consensus gain:** disagreement decreases;
2. **truth gain:** error decreases;
3. **productive friction:** nonzero disagreement participates in a transition that reduces truth error.

The project must not conflate them.

# 9. Productive-friction response

Raw friction is

[
mathcal F(t).
]

Truth gain is

[
G(t).
]

Define the conditional response curve

[
R(F)
=
mathbb E!left[Gmidmathcal F=Fight].
]

Candidate shapes to test include:

- monotone positive;
- monotone negative;
- threshold;
- saturation;
- inverted-U;
- multimodal;
- task-dependent;
- no stable relation.

If an optimum exists,

[
F^*
=
argmax_F R(F),
]

it is estimated from the data.

There is no requirement that (F^*=1), that any normalized version equal 1, or that the response be unimodal.

# 10. Cost-normalized gain

Let computational / human cost be

[
C(t)>0.
]

Define marginal efficiency

[
eta(t)
=
rac{G(t)}{C(t)}.
]

For full-run comparison,

[
eta_{mathrm{run}}
=
rac{mathcal E(0)-mathcal E(T)}
{sum_{t=0}^{T-1}C(t)}.
]

This distinguishes a method that improves accuracy from one that improves accuracy efficiently.

# 11. Conformity and corrective transitions

For proposition (p), define correctness indicator

[
c_i(t)=
mathbf 1
left[
operatorname{sign}(x_i(t))
=
operatorname{sign}(y)
ight].
]

A harmful conformity flip is

[
1ightarrow0,
]

while a corrective flip is

[
0ightarrow1.
]

For a run,

[
N_{10}
=
sum_i
mathbf 1[c_i(0)=1,c_i(T)=0],
]

[
N_{01}
=
sum_i
mathbf 1[c_i(0)=0,c_i(T)=1].
]

Define net corrective balance

[
B_{mathrm{corr}}
=
N_{01}-N_{10}.
]

This provides a direct mathematical measure of whether interaction creates more correction than corruption.

# 12. Information ceiling from correlated reviewers

For equal-variance reviewers, define effective independent reviewer count

[
N_{mathrm{eff}}
=
rac{N}
{1+(N-1)ho}.
]

Examples:

- (ho=0Rightarrow N_{mathrm{eff}}=N);
- (ho=1Rightarrow N_{mathrm{eff}}=1);
- large positive (ho) means apparent reviewer count greatly overstates independent information.

This quantity should be estimated before attributing gains to nominal model diversity.

# 13. Mathematical sequence

The scientific sequence is:

### M1 — Error covariance
Estimate (Sigma), pairwise correlations, and (N_{mathrm{eff}}).

### M2 — Static aggregation
Compare equal-weight, confidence-weighted, covariance-aware, and other mathematically justified aggregators.

### M3 — Interaction graph
Infer (W(t)), (L(t)), network structure, and disagreement energy (mathcal F(t)).

### M4 — First-order dynamics
Fit and test

[
dot{mathbf x}=-alpha Lmathbf x+Bmathbf u+eta.
]

### M5 — Spectral decomposition
Measure (lambda_k), modal decay, bottlenecks, and topology-dependent failure.

### M6 — Second-order challenge
Test whether

[
ddot{mathbf x}+Gammadot{mathbf x}+Kmathbf x=Bmathbf u+eta
]

is actually required.

### M7 — Modal chi, only if earned
If M6 is supported, derive

[
chi_k=rac{gamma_k}{2omega_k}
]

using the empirically supported (Gamma) and (K) conventions.

### M8 — Nonlinear extension
Only if residual structure demands it, test confidence-dependent susceptibility, saturation, hysteresis, asymmetric influence, or state-dependent topology.

### M9 — Function and Limit Maps
Map the mathematics of where correction works and where it fails.

# 14. Current claim ceiling

At project start, Hunting Friction v2 claims only that interacting reviewer systems can be represented and tested mathematically through estimator covariance, network disagreement, truth-error dynamics, and competing dynamical models.

It does **not** yet claim:

- a universal friction optimum;
- a validated CAF scalar;
- a second-order dynamical law;
- a justified SymC chi;
- an exceptional point;
- superiority of debate;
- superiority of heterogeneous models;
- or generality across domains.

Those are questions for the mathematics to answer.
