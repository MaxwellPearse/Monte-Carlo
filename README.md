# Assignment 4 Summary

## Question 1: MCMC Concepts
- **1a & 1b:** Diagrams provided to explain theoretical MCMC concepts.

---

## Question 2: Bayesian Inference Using MCMC

### 2a
- Data (`x` and `y`) were read into R.

### 2b: Gibbs Sampling
- Implemented a custom Gibbs sampler for the model parameters (`mu`, `sigma²`).
- Ran two chains with different starting values.
- Trace plots show that both chains **mixed well** and **behaved similarly**.

### 2c: Gibbs Posterior Summaries
- Removed first 50 iterations as **burn-in**.
- Estimated:
  - Posterior mean of `mu` and `sigma²`.
  - 95% credible intervals for both parameters.

### 2d: Metropolis-Hastings Sampling
- Implemented custom Metropolis-Hastings sampler.
- Ran two chains with different starting points.
- Trace plots indicate **good mixing** and **convergence**.

### 2e: Metropolis Posterior Summaries
- Removed first 1000 samples as **burn-in**.
- Estimated:
  - Posterior means of `mu` and `sigma²`.
  - 95% credible intervals for both parameters.

### 2f and 2g: Posterior Distributions
- Plots shown for posterior densities of `mu` and `sigma²`.

### 2h: Variational Inference (CAVI)
- Implemented **Coordinate Ascent Variational Inference (CAVI)**.
- Two different initializations were tested.
- Both runs converged to the same posterior approximation:
  - \( q^*_{\mu}(\mu) \sim N(0.818, 0.031) \)
  - \( q^*_{\sigma^2}(\sigma^2) \sim \text{Inverse-Gamma}(12.5, 6.095) \)
- **Evidence Lower Bound (ELBO)** increased at each iteration, confirming convergence.

---

## Overall Summary
- Successfully applied **Gibbs sampling**, **Metropolis-Hastings**, and **Variational Inference**.
- All methods provided consistent and stable estimates for `mu` and `sigma²`.
- Diagnostics (trace plots, ELBO plots) confirmed **good convergence and mixing**.

