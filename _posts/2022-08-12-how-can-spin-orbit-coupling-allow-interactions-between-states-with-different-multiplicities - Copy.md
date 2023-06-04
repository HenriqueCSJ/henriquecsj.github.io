---
title: How can Spin-Orbit-Coupling allow interactions between states with different multiplicities?
author: Henrique
date: 2022-08-12 14:10:00 +0800
categories: [Theory]
tags: [notekeeping, quantum mechanics, soc]
render_with_liquid: true
toc: true
math: true
---

> This whole text was riginally posted [here](https://chemistry.stackexchange.com/questions/159555/how-can-spin-orbit-coupling-allow-interactions-between-states-with-different-mul).
{: .prompt-info }

In the *absence* of spin–orbit coupling (SOC), the available states have well-defined spin and orbital angular momentum components which can be separated. We could, for example, write the total wavefunction as a product of spin and orbital components:

$$|\psi\rangle = |\chi_{\text{spin}}\phi_{\text{orbital}}\rangle \cong |\chi_{\text{spin}}\rangle \otimes |\phi_{\text{orbital}}\rangle. \tag{1}$$

Each spin part $\|\chi_{spin}\> $ has a well-defined value of $S$, and each orbital part $\left \| \phi_{orbital} \right \>$ has a well-defined value of $L$. So the total state $\left \| \psi \right \>$ has well-defined values of both $S$ and $L$.

When a system is placed under some kind of perturbation $H'$, the transition probability per unit time (i.e. how likely the system is to go from state $i$ to state $j$) is proportional to

$$| \langle i | H' | j \rangle |^2  \tag{2}$$

(this is part of [Fermi's golden rule](https://en.wikipedia.org/wiki/Fermi%27s_golden_rule)). For radiative transitions, the perturbation $H'$ is proportional to the position operator $\vec{r} = (x, y, z)$ (this integral is then called the [transition dipole moment](https://en.wikipedia.org/wiki/Transition_dipole_moment)). It's not important to actually bother with what this exactly is. The important bit is that this operator depends only on spatial components (it's independent of spin). So, the matrix element in eq. $(2)$ can be rewritten as

$$\begin{align}
\langle i | H' | j \rangle &= \left< \chi_\text{spin}^{(i)}\phi_\text{orbital}^{(i)} \middle| H' \middle| \chi_\text{spin}^{(j)}\phi_\text{orbital}^{(j)} \right> \tag{3} \\[5pt]
&= \left< \chi_\text{spin}^{(i)} \middle| \chi_\text{spin}^{(j)} \right> \left< \phi_\text{orbital}^{(i)} \middle| H' \middle| \phi_\text{orbital}^{(j)} \right> \tag{4} \\
\end{align}$$

Now, notice that the spin part of this integral, $\langle \chi_\text{spin}^{(i)} | \chi_\text{spin}^{(j)} \rangle$, is zero unless the two spin states are the same (because spin states are orthogonal). That means that the matrix element, and hence the transition probability, between states of different spin is zero.

-------

Now, when you turn on SOC, the available states no longer have well-defined $S$ and $L$. In general, they will be *linear combinations* of different $S$ and $L$:

$$|\psi\rangle = c_1\left|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\right> + c_2\left|\chi_{\text{spin}}^{(2)}\phi_{\text{orbital}}^{(2)}\right> +  ​\cdots + c_n\left|\chi_{\text{spin}}^{(n)}\phi_{\text{orbital}}^{(n)}\right> + \cdots \tag{5}$$

Crucially, there is no guarantee that the spin components

$\left\|\chi_{spin}^{(n)}\right\rangle$

all have the same value of $S$. You may mix together singlets, triplets, ... all into the same state.

When you calculate the matrix element $\langle i | H' | j \rangle$ between these states, it's therefore no longer guaranteed that it goes to zero. It's not that the spin selection rule is no longer obeyed; it's more like all the states have a little bit of different-spin-character mixed into them, so that transitions between each pair of states is no longer strictly forbidden.

The slightly confusing part arises because often, the SOC is a fairly weak phenomenon. That means that the extent of mixing is pretty small, or mathematically, one of the coefficients in the linear expansion $(5)$ is much greater than the others, such that

$$|\psi\rangle \approx c_1\left|\chi_{\text{spin}}^{(1)}\phi_{\text{orbital}}^{(1)}\right> + \text{(small contributions from other states)} \tag{6}$$

In this case we can say that the quantum number $S$ is *almost* well-defined, or that it is an *almost* good quantum number; and we can label the states *as if* they did have a well-defined value of $S$. This is the case with atomic term symbols, for example.

However, just because those other contributions are small doesn't mean that they are zero. So, for example, a state that is *almost* $S = 1$ can have a bit of $S = 0$ character mixed in; that means that the transition between this state, and a second state that is predominantly $S = 0$, is not entirely forbidden.

This mixing is caused by SOC, and hence SOC is precisely the mechanism which allows transitions between states which nominally have different values of $S$. (In actual fact, it is more accurate to say that $S$ is not perfectly well-defined for these states.)

-----

(Many quantum mechanics textbooks cover angular momentum, and angular momentum coupling, in great detail. Normally these are presented using $j_1$ and $j_2$ as the "sources of angular momentum", but in fact SOC is precisely the same thing, just that we use $s$ and $l$ as the labels instead. So if you want a more in-depth treatment of this, you can look in any reputable textbook.)