---
layout: posts
title: "Understanding Symmetry Breaking (Part III)"
categories: Prelim Series
author: Uzziel Perez
meta: "Explaining Symmetry breaking to my college self"
math: true
---

### Giving the gauge bosons a mass

Instead of just having a scalar field, we can redo the previous calculations we did for a complex scalar field $$\phi = \left(\phi_1 + i \phi_2 \right)/\sqrt(2)$$. The Lagrangian becomes

\\[ \mathcal{L} = \left(\partial_{\mu} \phi\right)*\left(\partial_{\mu} \phi\right) - \mu^2 \phi*\phi - \lambda - \lambda \left(\phi*\phi \right)^2 \\].

This is invariant under U(1) transformation, where $$\phi \rightarrow e^{i\alpha \phi}$$. When we rewrite the Lagrangian explicitly in terms of $$\phi_1$$ and $$\phi_2$$. We consider the same cases when $$\lambda > 0$$ and $$\mu^2 < 0$$.


When we plot the potential, the minima is a set of points forming a circle. This occurs when $$\lambda > 0$$ and $$\mu^2 < 0$$.

<img alt="Lumi" src="{{ "/assets/img/complexscalar.png" width="5" height="10"| prepend: site.baseurl }}" />

If we translate the field to a minimum energy position, take $$\phi_1 = v$$ and $$\phi_2 = 0$$, we can expand $$\mathcal{L}$$ about the vacuum in terms of $$\eta$$, $$\psi$$ with $$\phi (x) = v + \eta(x) + i \psi(x)$$, we then get

\\[ \mathcal{L}' = \frac{1}{2}\left(\partial_{\mu} \psi\right)^2 + \frac{1}{2}\left(\partial_{\mu} \eta\right)^2 + \mu^2 \eta^2 + const. + extra terms\\].

Here we now find a mass term in the third term ($$-\frac{1}{2}m_{\eta}^2 \eta^2$$) for the $$\eta$$-field. So the mass is just $$\sqrt{-2\mu^2}$$.
Notice that when we generate a massive gauge boson, we generate something what is called massless "Goldstone bosons". And it turns out these are unwanted consequences.

## The Higgs Mechanism

Ok, I won't go through the entire calculations here. Halzen and Martin did a very good job in Chapter 14.8 by first looking at the U(1) gauge symmetry and the SU(2) case. The first step is to make the lagrangian invariant under U(1) local gauge transformation and replace the derivatives with the covariant derivative $$D_{\mu} = \partial_{\mu} - ieA_{\mu}$$. We repeat the procedure of translating the field to the ground state. A goldstone boson $$\psi$$ is produced, a massive scalar $$\eta$$ and a massive vector $$A_{\mu}$$ is also found. If we repeat the procedure for a local SU(2) Gauge symmetry, what happens is that the gauge fields will "eat up" the Goldstone bosons and will become massive. In both the U(1) and SU(2) case the Higgs mechanism the scalar degrees of freedom has been turned into some longitudinal polarization of the massive gauge particle.

This is probably not a very good explanation for my college self yet. But the salient features are here. So we're going to do another iteration of learning this later on.
