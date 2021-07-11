---
layout: post
title:  "Syntax Highlighting Test"
date:   2017-03-24 01:30:13 +0800
categories: default
tags: test syntax
---

Free energy is a very important indicator of whether a process is spontaneous. Given the free energy of a process can we determine the important properties including binding affinities and protein folding. In addition, the free energy barrier can be helpful to determine the kinetics and rates of the process.



Two kinds of free energy is often considered. Helmholtz and Gibbs free energies. With definition
$$
F=U-TS\\
G=H-TS=U+pV-TS
$$
The free energy is dependent on international energy and entropy, so changes in interatomic interactions and entropy would cause significant change in free energy. Particularly, the entropy change induced by solvent can be dominant to free energy change.



One important implication of free energy is that the probability of being one state is related to its free energy
$$
p(x)\propto e^{-G(x)/k_BT}
$$
And such relation can be extremely helpful when we want to estimate the free energy difference between state A and B:
$$
\frac{p(A)}{p(B)}=e^{-\Delta G/k_BT}
$$
By simply simulating the process between A and B and the free energy difference can be obtained by evaluating the populations in A and B.



There are also other methods to obtain free energy differences. Umbrella sampling and thermodynamic integration are two methods that is particularly useful for processes including free energy barriers, for example, the binding, unbinding, conformational transitions, protein folding processes.

#### Umbrella sampling

#### Thermodynamic integration





### Theoretical background 

#### Definition of free energy

The free energy can be obtained from the partition function of  an ensemble.

Helmholtz Free energy can be obtained from canonical partition function
$$
F=-\frac{1}{\beta}lnQ(N,V,T)
$$
 Where the partition function can be expressed
$$
Q(N,V,T)=\frac{1}{h^{3N}N!}\int...\int e^{-\beta H(\bold{p_1,p_2,...,p_N,q_1,q_2,...,q_N})}d\bold{p_1}...d\bold{p_N}d\bold{q_1}...d\bold{q_N}
$$
For simulation, this partition function can be not so feasible to obtain 



Gibbs free energy can be obtained from isothermal–isobaric ensemble
$$
G=-\frac{1}{\beta}lnQ(N,P,T)
$$
With partition function represented as:
$$
Q(N,P,T)=\frac{1}{h^{3N}N!}\int...\int e^{-\beta H(\bold{p_1,p_2,...,p_N,q_1,q_2,...,q_N}+PV)}d\bold{p_1}...d\bold{p_N}d\bold{q_1}...d\bold{q_N}
$$




As the Hamiltonian can be divided into kinetics part and potential part, the partition function can be also considered to consist of kinetic partition function  and configurational partition function

### Equilibrium Simulations

#### Perturbation Approach

The free energy perturbation (FEP) method introduced by Zwanzig[ref 7]
$$
\Delta G_{AB}=G_B-G_A=-\frac{1}{\beta}ln\frac{Q_B}{Q_A}=-\frac{1}{\beta}<e^{-\beta(H_B(\bold{p,q})-H_A(\bold{p,q}))}>
$$
The bracket denotes an ensemble average.



The approach relies on equilibrium sampling at state A and subsequent evaluation of the produced configurations with the Hamiltonian of state B.



The Hamiltonian is controlled by an external parameter often denoted as λ: 



The accuracy of the FEP method is strongly dependent on the phase space overlap of the states A and B.



For small overlap case, the configurations generated at state one state will be considered to be high energetic according to the Hamiltonian of the other state. As a result, it will contribute little to the exponential average. 

As a consequence, the method is only of use when the overlap in the phase space is large.



#### Bennet's Acceptance Ratio (BAR)

Bennet's estimate can be expressed as:


$$
\Delta G_{A B}=\frac{1}{\beta} \ln \frac{\left\langle f\left(H_{A}(\mathbf{p}, \mathbf{q})-H_{B}(\mathbf{p}, \mathbf{q})+C\right)\right\rangle_{B}}{\left\langle f\left(H_{B}(\mathbf{p}, \mathbf{q})-H_{A}(\mathbf{p}, \mathbf{q})-C\right)\right\rangle_{A}}+C
$$
Here, $f$ represents the fermi function
$$
f(x)=\frac{1}{1+exp(\beta x)}
$$
$C=\frac{1}{\beta}ln(\frac{Q_A}{Q_B}\frac{n_B}{n_A})$

n A and n B are the numbers of configurations generated at state A and B



The equation can be solved by finding such C that
$$
\sum_{B} f\left(H_{A}(\mathbf{p}, \mathbf{q})-H_{B}(\mathbf{p}, \mathbf{q})+C\right)=\sum_{A} f\left(H_{B}(\mathbf{p}, \mathbf{q})-H_{A}(\mathbf{p}, \mathbf{q})-C\right)
$$
Then the free energy difference can be obtained
$$
\Delta G=-\frac{1}{\beta} \ln \frac{n_{B}}{n_{A}}+C
$$




BAR is a minimal variance free energy estimate



Shirts et al. [14] also derived Bennet’s formula using maximum
likelihood formulation, thus, demonstrating that BAR provides
the most likely free energy estimate for the observed work
distributions.





Both methods introduced so far (FEP and BAR) were defined
for free energy calculations by sampling physical end states of a
system.
