---
title: Weinberg–Witten theorem
published: 2025-11-10
description: ''
image: ''
tags: [String Theory, Elementary Particle Physics, Quantum Gravity]
category: 'String Theory'
draft: false 
lang: 'en'
---

# Statement of the Theorem

The Weinberg–Witten theorem has two separate parts. 

## Current Version
If a Lorentz-covariant conserved current $J^\mu(x)$ exists, so that the global charge $Q=\int\,d^3xJ^0$ is well defined and transforms covariantly ([Appendix A](#appendix-a)), then the theory cannot contain a massless one-particle state of helicity $h\gt 1/2$ that carries nonzero charge $q$ under $Q$. In other words, there are no charged massless particles with spin $\gt 1/2$.

## Stress-energy Version
If there is a Lorentz-covariant, conserved stress-energy tensor $T^{\mu\nu}(x)$, so that the 4-momentum $P^\mu=\int\,d^3xT^{0\mu}$ is well defined and covariant, then the theory cannot contain a massless one-particle state of helicity $h\gt1$ that carries nonzero momentum charge, i.e. a particle that transforms nontrivially under translations. In other words, a massless particle of helicity $\gt 1$ cannot have a Lorentz-covariant energy-momentum current.


### Proof:
Assume a covariant conserved current $J^\mu$ exists and that there is a massless one-particle state $|p, h\rangle$ with helicity $h\gt 1/2$ carrying charge $q$ under $Q$. We will show that this leads to a contradiction. We are going to achieve this by first computing a matrix element:

$$
\begin{align}
\langle p', h'|\hat{Q}|p, h\rangle
&=\int\,d^3x\langle p', h'|J^0(0, \mathbf{x})|p, h\rangle\\
&=\int\,d^3x\langle p', h'|e^{i\hat{\mathbf{p}}\cdot\hat{\mathbf{x}}}J^0(0, \mathbf{0})e^{-i\hat{\mathbf{p}}\cdot\hat{\mathbf{x}}}|p, h\rangle \quad \text{$\hat{\mathbf{p}}, \hat{\mathbf{x}}$ acting on the states}\\
&=\underbrace{\int\,d^3xe^{i(\mathbf{p}-\mathbf{p'})\cdot\mathbf{x}}}_{\text{Fourier Transform}}\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle\\
&=(2\pi)^3\delta^{(3)}(\mathbf{p}-\mathbf{p'})\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle.
\end{align}
$$
Since $\hat{Q}|p, h\rangle=q|p, h\rangle$ (usually $q$ is omitted in the state description because it is conserved by assumption), 
$\langle p', h'|\hat{Q}|p, h\rangle=q\delta^{(3)}(\mathbf{p}-\mathbf{p'})\delta_{hh'}$. Then, comparing both sides,
$$
\begin{equation}
\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle=\frac{q}{(2\pi)^3}\delta_{hh'}
\end{equation}
$$
where the value is divided by $(2\pi)^3$ for the normalization. Now extend this to the four-vector ([Appendix B](#appendix-b)):

<a id="eq-current-matrix-element"></a>
$$
\begin{equation}
\langle p', h'|J^\mu(0)|p, h\rangle \xrightarrow{p' \to p} \frac{qp^\mu}{(2\pi)^3p^0}\delta_{hh'}.
\end{equation}
$$
Next, let's see what rotational invariance has to say about the same matrix element. The plan is the following. The limit above tells us that the matrix element must survive as $p'\to p$. We will show that for $h\gt 1/2$ Lorentz covariance forces it to vanish, and the two statements cannot coexist unless $q=0$. Note that the $\delta_{hh'}$ obtained above allows us to set $h'=h$ from now on.

Take two lightlike momenta $p\neq p'$ that are not collinear. Their sum is then timelike, since
$$
\begin{equation}
(p+p')^2=2p\cdot p'\neq 0,
\end{equation}
$$
so we can go to the center-of-momentum frame in which the two spatial momenta are back to back:
$$
\begin{equation}
\mathbf{p}'=-\mathbf{p}, \quad \hat{\mathbf{z}}\equiv\hat{\mathbf{p}}.
\end{equation}
$$
Now perform a rotation $R_\theta$ by an angle $\theta$ about this common axis. A massless one-particle state is a helicity eigenstate, and a rotation about its own momentum direction produces only a phase:
$$
\begin{equation}
U(R_\theta)|p, h\rangle=e^{ih\theta}|p, h\rangle.
\end{equation}
$$
For the primed state the same rotation is a rotation by $-\theta$ about $\hat{\mathbf{p}}'=-\hat{\mathbf{p}}$, hence
$$
\begin{equation}
U(R_\theta)|p', h\rangle=e^{-ih\theta}|p', h\rangle.
\end{equation}
$$
The two phases do not cancel between the bra and the ket — they add up. Inserting $U^\dagger(R_\theta)U(R_\theta)=1$ on both sides of the current and using that $J^\mu$ transforms as a four-vector, $U(R_\theta)J^\mu(0)U^\dagger(R_\theta)=(R_\theta^{-1})^\mu_\nu J^\nu(0)$,
$$
\begin{align}
\langle p', h|J^\mu(0)|p, h\rangle
&=\langle p', h|U^\dagger(R_\theta)\big(U(R_\theta)J^\mu(0)U^\dagger(R_\theta)\big)U(R_\theta)|p, h\rangle\\
&=e^{ih\theta}\,e^{ih\theta}\,(R_\theta^{-1})^\mu_\nu\langle p', h|J^\nu(0)|p, h\rangle\\
&=e^{2ih\theta}(R_\theta^{-1})^\mu_\nu\langle p', h|J^\nu(0)|p, h\rangle,
\end{align}
$$
or, equivalently,
$$
\begin{equation}
(R_\theta)^\mu_\nu\langle p', h|J^\nu(0)|p, h\rangle=e^{2ih\theta}\langle p', h|J^\mu(0)|p, h\rangle.
\end{equation}
$$
Read as a statement of linear algebra, this says that the four-component object $\langle p', h|J^\mu(0)|p, h\rangle$ is an eigenvector of the rotation matrix $R_\theta$ with eigenvalue $e^{2ih\theta}$. But a rotation about the $z$-axis acting on a four-vector has eigenvalues
$$
\begin{equation}
\{1, 1, e^{i\theta}, e^{-i\theta}\},
\end{equation}
$$
where the first two belong to the $t$ and $z$ components and the last two to the combinations $J^1\mp iJ^2$. A nonvanishing matrix element therefore requires
$$
\begin{equation}
e^{2ih\theta}\in\{1, e^{i\theta}, e^{-i\theta}\} \quad \text{for all } \theta,
\end{equation}
$$
i.e. $|2h|\le 1$. For $h\gt 1/2$ none of the eigenvalues can be matched, so every component must vanish:
$$
\begin{equation}
\langle p', h|J^\mu(0)|p, h\rangle=0 \quad \text{for all non-collinear } p\neq p'.
\end{equation}
$$
Taking the limit $p'\to p$ of this vanishing quantity and comparing with the limit [computed above](#eq-current-matrix-element), we are forced to conclude
$$
\begin{equation}
\frac{qp^\mu}{(2\pi)^3p^0}=0,
\end{equation}
$$
i.e. $q=0$. This contradicts the assumption that the particle carries a nonzero charge, and the current version of the theorem follows. (Strictly speaking, the limit should be taken with wave packets rather than plane-wave states. This is how the original paper ([References](#references)) handles it, and the conclusion is unchanged.)

<div style="text-align: right;">

$\blacksquare$

</div>

The stress-energy version goes through the same steps with $T^{\mu\nu}$ in place of $J^\mu$. The analogue of the limit above is
$$
\begin{equation}
\langle p', h|T^{\mu\nu}(0)|p, h\rangle \xrightarrow{p' \to p} \frac{p^\mu p^\nu}{(2\pi)^3p^0},
\end{equation}
$$
which cannot vanish, because this time the "charge" is the four-momentum itself and every particle carries it. On the other hand, $T^{\mu\nu}$ has two vector indices, so under the back-to-back rotation the eigenvalues now range over $e^{ik\theta}$ with $k\in\{0, \pm1, \pm2\}$, and a nonvanishing matrix element requires $|2h|\le 2$, i.e. $h\le 1$. Hence a massless particle of helicity $h\gt 1$ — the graviton being the obvious candidate — cannot appear in any theory equipped with a Lorentz-covariant conserved stress-energy tensor.

<div style="text-align: right;">

$\blacksquare$

</div>

It is worth pausing on why familiar theories evade the theorem. Gluons ($h=1$) do carry color charge, but the color current of Yang–Mills theory is not gauge invariant, so no Lorentz-covariant conserved current satisfies the hypothesis. General relativity escapes the stress-energy version for a similar reason. The energy-momentum of the gravitational field cannot be localized covariantly, and the candidate currents are only pseudo-tensors. What the theorem genuinely forbids is an emergent, composite graviton in a Lorentz-invariant theory with a covariant conserved $T^{\mu\nu}$. Any attempt at emergent gravity must therefore give up at least one of these assumptions.

### Appendix A 
Let's quickly check the covariance of the global charge. For that purpose, introduce a Cauchy hypersurface $\Sigma$ with surface element $d\Sigma_\mu$, which points normal to the hypersurface and whose magnitude is the volume element of the slice. For example, if $\Sigma$ is a constant-time slice with $n_\mu=(1, 0, 0, 0)$, then $\,d\Sigma_\mu=n_\mu\,d^3x=(d^3x,0,0,0)$. Using it, we can define the global charge as $Q=\int\,d^3xJ^0=\int_{\Sigma}\,d\Sigma_{\mu}J^{\mu}$. We are going to show the following two parts:
#### A.1 $Q$ is independent of the choice of $\Sigma$
Assuming locality of charges and fields, i.e. $Q=\int\,d^3xJ^0\lt\infty$, and using the continuity equation $\partial_\mu J^\mu = 0$,
$$
\begin{align}
Q(\Sigma_j)-Q(\Sigma_i)&=\int_{\Sigma_j}\,d\Sigma_\mu J^\mu-\int_{\Sigma_i}\,d\Sigma_\mu J^\mu + 0\\
&=\int_{\Sigma_j}\,d\Sigma_\mu J^\mu + \int_{-\Sigma_i}\,d\Sigma_\mu J^\mu + \underbrace{\int_{\text{sides at infinity}} d\Sigma_\mu J^\mu}_{= 0 \text{ if } J^\mu \to 0\, \text{as}\, |x|\to \infty}\\
&=\int_{\partial V}\,d\Sigma_\mu J^\mu \quad \text{by Gauss's theorem}\\
&=\int_{V}\,d^4x\partial_\mu J^\mu \quad \text{by } \partial_\mu J^\mu = 0\\
&=0.
\end{align}
$$
Hence the global charge is independent of the choice of hypersurface.
#### A.2 Lorentz covariance of $Q$
Consider a Lorentz transformation $x'^\mu=\Lambda^\mu_\nu x^\nu$ and $J'^\mu(x')=\Lambda^\mu_\rho J^\rho(x)$. Then
$$
\begin{align}
Q'&=\int_{\Sigma'}\,d\Sigma'_\mu J'^\mu(x')\\
&=\int_{\Sigma}(\Lambda_\mu^\nu\,d\Sigma_\nu)(\Lambda^\mu_\rho J^\rho)\\
&=\int_{\Sigma}\,d\Sigma_\nu\underbrace{(\Lambda_\mu^\nu\Lambda_\rho^\mu)}_{=\delta^\nu_\rho}J^\rho\\
&=\int_{\Sigma}\,d\Sigma_\nu J^\nu\\
&=Q.
\end{align}
$$
Combining A.1 and A.2, the covariance of the global charge is proved.

### Appendix B
In the process of extending the $J^0$ result to the full $J^\mu$ expression, let us first introduce an important identity called the Ward–Takahashi identity.
#### B.1 Ward–Takahashi Identity
We are going to show $q_\mu\langle p'|J^\mu|p\rangle=0$, with $q^\mu=p^\mu-p'^\mu$, using the current conservation $\partial_\mu J^\mu=0$.
Observe
$$
\begin{align}
0
&=\langle p'|\partial_\mu J^\mu(0)|p\rangle\\
&=\langle p'|\partial_\mu (e^{i(p-p')\cdot x}J^\mu(0))|p\rangle\\
&=i(p-p')_\mu e^{i(p-p')\cdot x}\langle p'|J^\mu(0)|p\rangle + \langle p'|e^{i(p-p')\cdot x}\underbrace{\partial_\mu J^\mu(0)}_{=0}|p\rangle\\
&=iq_\mu \underbrace{e^{i(p-p')\cdot x}}_{\neq 0}\langle p'|J^\mu(0)|p\rangle.
\end{align}
$$
We can factor out the exponential factor to arrive at the identity.

#### B.2 Extending to the four-vector
Given a massless one-particle state, Lorentz covariance and the available momenta imply that, for a fixed helicity, we can generally write the matrix element as:
$$
\begin{equation}
\langle p', h|J^\mu(0)|p, h\rangle
=A(p, p')p^\mu + B(p, p')p'^\mu + C(p, p')q^\mu
\end{equation}
$$
with some coefficients $A, B, C$ and $q^\mu=p^\mu-p'^\mu$.

### References
1. S. Weinberg and E. Witten, "Limits on Massless Particles," *Phys. Lett. B* **96** (1980) 59–62. [doi:10.1016/0370-2693(80)90212-9](https://doi.org/10.1016/0370-2693(80)90212-9)
