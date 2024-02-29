# Bayesian Spherical Harmonics Estimation
Assume some noisy map of the sky with resolution Nside distributed as:
$$ x \sim \mathcal{N}(M, \mathbb{C})$$
One can then draw a statistical model for $M$:
$$ a_{\ell m} \sim \mathcal{N}(\hat{a}_{\ell m}, 1) $$
$$ M({\rm Nside}) \gets \sum_{\ell} \sum_{m = 2\ell  +1} a_{\ell m} Y_{\ell m}({\rm Nside})$$
$$ x \sim \mathcal{N}(M, \mathbb{C})$$
where:
$$ \hat{a}_{\ell m } =  \sum_{\ell} \sum_{m = 2\ell  +1} M Y_{\ell m} $$
with gradient:
$$ \frac{\partial \mathcal{L}}{\partial a_{\ell m}} = \frac{\partial \mathcal{L}}{\partial M} \cdot \frac{\partial M}{\partial a_{\ell m}}  = \frac{\partial \mathcal{L}}{\partial M} Y_{\ell m}$$