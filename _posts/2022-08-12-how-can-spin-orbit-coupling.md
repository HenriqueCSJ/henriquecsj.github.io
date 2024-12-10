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

$$|\psi\rangle = |\chi_{\text{spin}}\phi_{\text{orbital}}\rangle \cong |\chi_{\text{spin}}\rangle \otimes |\phi_{\text{orbital}}\rangle. \tag{1}$$

Each spin part $|\chi_{\text{spin}}\rangle$ has a well-defined value of $S$, and each orbital part $|\phi_{\text{orbital}}\rangle$ has a well-defined value of $L$. So the total state $|\psi\rangle$ has well-defined values of both $S$ and $L$.

When a system is placed under some kind of perturbation $H'$, the transition probability per unit time (i.e., how likely the system is to go from state $i$ to state $j$) is proportional to

$$|\langle i | H' | j \rangle|^2. \tag{2}$$

(This is part of [Fermi's golden rule](https://en.wikipedia.org/wiki/Fermi%27s_golden_rule).) For radiative transitions, the perturbation $H'$ is proportional to the position operator $\vec{r} = (x, y, z)$ (this integral is then called the [transition dipole moment](https://en.wikipedia.org/wiki/Transition_dipole_moment)). It's not important to know the exact form of this operator; the important bit is that it depends only on spatial components and is independent of spin. Thus, the matrix element in eq. (2) can be rewritten as

$$
\begin{align}
\langle i | H' | j \rangle &= \langle \chi_{\text{spin}}^{(i)} \phi_{\text{orbital}}^{(i)} | H' | \chi_{\text{spin}}^{(j)} \phi_{\text{orbital}}^{(j)} \rangle \tag{3} \\[6pt]
&= \langle \chi_{\text{spin}}^{(i)} | \chi_{\text{spin}}^{(j)} \rangle \langle \phi_{\text{orbital}}^{(i)} | H' | \phi_{\text{orbital}}^{(j)} \rangle. \tag{4}
\end{align}
$$

Now, notice that the spin part of this integral, $\langle \chi_{\text{spin}}^{(i)} | \chi_{\text{spin}}^{(j)} \rangle$, is zero unless the two spin states are the same (because distinct spin states are orthogonal). That means that the matrix element, and hence the transition probability, between states of different spin is zero.

-----

Now, when you turn on SOC, the available states no longer have well-defined $S$ and $L$. In general, they will be *linear combinations* of different $S$ and $L$:

$$|\psi\rangle = c_1|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\rangle + c_2|\chi_{\text{spin}}^{(2)}\phi_{\text{orbital}}^{(2)}\rangle + \cdots + c_n|\chi_{\text{spin}}^{(n)}\phi_{\text{orbital}}^{(n)}\rangle + \cdots. \tag{5}$$

Crucially, there is no guarantee that the spin components $|\chi_{\text{spin}}^{(n)}\rangle$ all have the same value of $S$. You may mix together singlets, triplets, and so forth, all into the same state.

When you calculate the matrix element $\langle i | H' | j \rangle$ between these states, it's therefore no longer guaranteed to vanish. It's not that the spin selection rule is no longer "obeyed" in some fundamental sense; it's that each state is now a mixture of components with different spin quantum numbers. Thus, a state that is predominantly of one spin multiplicity can have a small admixture of another, making transitions between what were previously spin-forbidden states now allowed, albeit with small probability.

The slightly confusing part arises because, often, the SOC is a fairly weak phenomenon. That means that the extent of mixing is usually small, or mathematically, one of the coefficients in the linear expansion (5) is much larger than the others, such that

$$|\psi\rangle \approx c_1|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\rangle + \text{(small contributions from other states)}. \tag{6}$$

In this case, we can say that the quantum number $S$ is *almost* well-defined, or that it is an *almost* good quantum number; and we can label the states *as if* they had a well-defined value of $S$. This is the case with atomic term symbols, for example.

However, just because those other contributions are small doesn't mean that they are zero. So, for example, a state that is *almost* $S = 1$ can have a bit of $S = 0$ character mixed in; that means that the transition between this state and another state that is predominantly $S = 0$ is not completely forbidden.

This mixing is caused by SOC, and hence SOC is precisely the mechanism that allows transitions between states which nominally have different values of $S$. In fact, it's more accurate to say that $S$ is not perfectly well-defined for these states once SOC is considered.

-----

(Many quantum mechanics textbooks cover angular momentum and angular momentum coupling in detail. Typically, these are presented using $j_1$ and $j_2$ as sources of angular momentum. SOC is conceptually the same thing, just using $s$ and $l$ as labels. For a more in-depth treatment, you can consult any reputable quantum mechanics textbook.)