---
title: How can Spin-Orbit Coupling allow interactions between states with different multiplicities?
author: Henrique
date: 2022-08-12 14:10:00 +0800
categories: [Theory]
tags: [notekeeping, quantum mechanics, soc]
toc: true
math: true
---

> This whole text was originally posted [here](https://chemistry.stackexchange.com/questions/159555/how-can-spin-orbit-coupling-allow-interactions-between-states-with-different-mul).
{: .prompt-info }

In the *absence* of spin–orbit coupling (SOC), the available states have well-defined spin and orbital angular momentum components which can be separated. We could, for example, write the total wavefunction as a product of spin and orbital components:

$$
|\psi\rangle = |\chi_{\text{spin}}\phi_{\text{orbital}}\rangle \simeq |\chi_{\text{spin}}\rangle \otimes |\phi_{\text{orbital}}\rangle.
\tag{1}
$$

Each spin part $\lvert\chi_{\text{spin}}\rangle$ has a well-defined value of $S$, and each orbital part $\lvert\phi_{\text{orbital}}\rangle$ has a well-defined value of $L$. Thus, the total state $\lvert\psi\rangle$ has well-defined values of both $S$ and $L$.

When a system is placed under some kind of perturbation $H'$, the transition probability per unit time (i.e. how likely the system is to go from state $i$ to state $j$) is proportional to

$$
|\langle i | H' | j \rangle|^2.
\tag{2}
$$

(This is part of [Fermi's golden rule](https://en.wikipedia.org/wiki/Fermi%27s_golden_rule).) For radiative transitions, the perturbation $H'$ is proportional to the position operator $\vec{r} = (x,y,z)$, which is related to the [transition dipole moment](https://en.wikipedia.org/wiki/Transition_dipole_moment). The exact form of the operator is not important here. The key point is that $H'$ depends only on spatial coordinates and not on spin.

Thus, the matrix element in eq. (2) can be rewritten as

$$
\begin{align}
\langle i | H' | j \rangle 
&= \langle \chi_{\text{spin}}^{(i)}\phi_{\text{orbital}}^{(i)} | H' | \chi_{\text{spin}}^{(j)}\phi_{\text{orbital}}^{(j)} \rangle 
\tag{3}\\[6pt]
&= \langle \chi_{\text{spin}}^{(i)} | \chi_{\text{spin}}^{(j)} \rangle 
\langle \phi_{\text{orbital}}^{(i)} | H' | \phi_{\text{orbital}}^{(j)} \rangle.
\tag{4}
\end{align}
$$

Now, notice that $\langle \chi_{\text{spin}}^{(i)} | \chi_{\text{spin}}^{(j)} \rangle = 0$ unless the spin states are the same, since orthogonal spin states yield zero overlap. Consequently, in the absence of SOC, transitions between states of different spin are strictly forbidden.

-----

Now, when you turn on SOC, the available states no longer have well-defined $S$ and $L$. In general, they can be *linear combinations* of basis states with different $S$ and $L$:

$$
|\psi\rangle = c_1|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\rangle 
+ c_2|\chi_{\text{spin}}^{(2)}\phi_{\text{orbital}}^{(2)}\rangle 
+ \cdots 
+ c_n|\chi_{\text{spin}}^{(n)}\phi_{\text{orbital}}^{(n)}\rangle + \cdots.
\tag{5}
$$

Crucially, the spin parts $|\chi_{\text{spin}}^{(n)}\rangle$ need not all have the same $S$. Singlet and triplet character (for example) can become mixed into a single state.

When computing $\langle i | H' | j \rangle$ under SOC, each state $|i\rangle$ and $|j\rangle$ is now a mixture of spin characters. This means the previously strict selection rule (no transitions between different spins) is softened. It's not that the spin selection rule is "broken" per se, but that each eigenstate is no longer a pure spin eigenstate. Thus, what used to be "forbidden" transitions can now occur with some small probability.

Often SOC is a weak effect. This means that, although a state might be mostly a certain spin state, it will have small admixtures of others:

$$
|\psi\rangle \approx c_1|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\rangle 
+ \text{(small contributions from states with different $S$)}.
\tag{6}
$$

Such a state is said to have an *almost* well-defined $S$, making $S$ an *almost* good quantum number. We can still label the state using $S$ as if it were well-defined, but we must remember that there's a small contamination from other spin states. This small contamination allows transitions that would be strictly forbidden in the absence of SOC. Hence, SOC enables interactions (transitions) between states of different multiplicities.

-----

For a more in-depth treatment, consult textbooks on quantum mechanics that discuss angular momentum coupling. The mathematics of combining $s$ and $l$ into $j$ is analogous to combining other angular momenta. SOC is essentially just one more example of angular momentum coupling in quantum mechanics.
