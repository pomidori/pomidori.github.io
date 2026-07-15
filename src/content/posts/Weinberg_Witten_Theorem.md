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

Weinberg–Witten theorem has two separate parts. 

## Current Version
If a Lorentz-covariant conserved current $J^\mu(x)$ exists, so the global charge $Q=\int\,d^3xJ^0$ is well defined and transforms covariantly [Appendix A](#appendix-a), then the theory cannot contain a massless one-particle state of helicity $h\gt 1/2$ that carries nonzero charge $q$ under $Q$. In other words, no charged massless particles with spin $\gt 1/2$.

## Stress-energy Version
If there is a Lorentz-covariant, conserved stress-energy tensor $T^{\mu\nu}(x)$, so the 4-momentum $P^\mu=\int\,d^3xT^{0\mu}$ is well defined and covariant., then the theory cannot contain a massless one-particle state of helicity $h\gt1$ that caeeries nonzero momentum chage, i.e. a particle that transforms nontrivially under translations. In other word, a massless particle of helicity $\gt 1$ cannot have a Lorentz-covariant energy-momentum current.


### Proof:
Assume a covariant conserved current $J^\mu$ and there is a massless one-particle state $|p,\lambda\rangle$ with helicity $\lambda\gt 1/2$ carrying charge $q$ under $Q$. We will show that this leads to a contradiction. We are going to achieve this by first computing a matrix element:

$$
\begin{align}
\langle p', h'|\hat{Q}|p, h\rangle
&=\int\,d^3x\langle p', h'|J^0(0, \mathbf{x})|p, h\rangle\\
&=\int\,d^3x\langle p', h'|e^{i\hat{\mathbf{p}}\cdot\hat{\mathbf{x}}}J^0(0, \mathbf{0})e^{-i\hat{\mathbf{p}}\cdot\hat{\mathbf{x}}}|p, h\rangle \quad \text{$\hat{\mathbf{p}}, \hat{\mathbf{x}}$ acted on the state}\\
&=\underbrace{\int\,d^3xe^{i(\mathbf{p}-\mathbf{p'})\cdot\mathbf{x}}}_{\text{Fourier Transform}}\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle\\
&=(2\pi)^3\delta^{(3)}(\mathbf{p}-\mathbf{p'})\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle.
\end{align}
$$
Since $\hat{Q}|p, h\rangle=q|p, h\rangle$ (usually $q$ is omitted in the state description because it is conserved by the assumption), 
$\langle p', h'|\hat{Q}|p, h\rangle=q(2\pi)^3\delta^{(3)}(\mathbf{p}-\mathbf{p'})\delta_{hh'}$. Then comparing the both sides,
$$
\langle p', h'|J^0(0, \mathbf{0})|p, h\rangle=\frac{q}{(2\pi)^3}\delta_{hh'}
$$
where the value is divided by $(2\pi)^3$ for the normalization. Now extend this to the four vector ([Appendix B](#appendix-b)):

<a id="eq-current-matrix-element"></a>
$$
\langle p', h'|J^\mu(0)|p, h\rangle \xrightarrow{p' \to p} \frac{qp^\mu}{(2\pi)^3p^0}\delta_{hh'}.
$$
Next 


### Appendix A 
Let's quickly check covariance check of the global charge. For that purpose, introduce a Cauchy hypersurface $\Sigma$, it points normal to the hypersurface and its magnitude being the volume element of the slice, for example if $\Sigma$ is a constant in time $n_\mu=(1, 0, 0, 0)$, then $\,d\Sigma_\mu=n_\mu\,d^3x=(d^3x,0,0,0)$. Using it, we can define a global charge as $Q=\int\,d^3xJ^0=\int_{\Sigma}\,d\Sigma_{\mu}J^{\mu}$. We are going to show the following two parts:
#### A.1 $Q$ is independent of the choice of $\Sigma$
Assuming locality of charges and fields, i.e. $Q=\int\,d^3xJ^0\lt\infty$, then using continuity equation $\partial_\mu J^\mu = 0$,
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
Together with A.1 and A.2, covariance of a global charge is proved.

### Appendix B
In the process of extending $J^0$ to $J^\mu$ expression, let us first introduce an important identity called Ward-Takahashi Identity.
#### B.1 Ward-Takahashi Identity
We are going to show $q_\mu\langle p'|J^\mu|p\rangle=0$ with $q^\mu=p^\mu-p'^\mu$ and the current conservation $\partial_\mu J^\mu=0$.
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

#### B.2 Extending to the four vector
Given one massless particle state with Lorentz covariance and momentum dependence, for a fixed helicity generally we can write the matrix element as:
$$
\langle p', h|\partial_\mu J^\mu(0)|p, h\rangle
=A(p, p')p^\mu + B(p, p')p'^\mu + C(p, p')q^\mu
$$
with some coefficient $A, B, C$ and $q^\mu=p^\mu-p'^\mu$.
