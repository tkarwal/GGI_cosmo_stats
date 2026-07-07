# Cosmological Parameter-Estimation Methods

Teaching material for GGI summer school in 2026 on statistical methods in
cosmology. The course develops practical skills in both Bayesian and
frequentist approaches to parameter inference, with an emphasis on building working implementations from scratch.

---

## Course overview

Modern cosmological analyses — CMB, large-scale structure, gravitational waves,
supernovae, ++ — all reduce to the same core problem: given noisy data and a
physical model, what do the data tell us about the parameters of the Universe?

This course covers two complementary families of methods:

**Bayesian inference** maps data onto a posterior probability distribution over
parameters, naturally incorporating prior knowledge and propagating
uncertainties. Bayesian MCMC (Markov chain Monte Carlo) is the dominant
framework in cosmology, underpinning codes such as [`CosmoMC`](https://cosmologist.info/cosmomc/), [`cobaya`](https://cobaya.readthedocs.io/en/latest/), and
[`MontePython`](https://github.com/brinckmann/montepython_public). 

**Frequentist methods — profile likelihoods** have been gaining significant
traction in cosmology as a cross-check on posterior-based results. The profile
likelihood traces the maximum likelihood achievable at each parameter value by
optimising over all other ("nuisance") parameters, as opposed to Bayesian 
approaches that marginalise over the other parameters. It offers complementary 
insight into the influence of priors on Bayesian posteriors.
Several profile likelihood codes are also publicly-available for use in 
conjunction with cosmological likelihoods, including [`Procoli`](https://github.com/tkarwal/procoli), [`pinc`](https://github.com/LauraHerold/pinc) and 
[`PROSPECT`](https://github.com/AarhusCosmology/prospect_public). 

Both approaches are taught here because in practice they should agree — and
when they don't, something interesting is happening.

---

## Software environment

All notebooks use only:

```
numpy  scipy  matplotlib  corner  tqdm
```
with some optional packages 
```
ipywidgets  ipympl
```
for interactive plots. 

Install with:

```bash
pip install numpy scipy matplotlib corner tqdm
```

or, if using conda:

```bash
conda install numpy scipy matplotlib corner tqdm
```

The easiest way to run these notebooks would be on Google colab, using the links below. 


---

## Notebooks by lecture 

| Lecture | Topic | Notebook | Colab link |
|---------|-------|----------|------------|
| Lecture 1 | Metropolis-Hastings MCMC | `ggi_write_MH_MCMC.ipynb` | [Open in Colab]() |
| Lecture 2 | Profile likelihoods | `ggi_write_profile_likelihood.ipynb` | [Open in Colab]() |
| Lecture 3 | MontePython and Cobaya demos | No notebooks | - |


---

## Further reading

- [Procoli implementation of profiles in cosmology](https://arxiv.org/pdf/2401.14225)
- [How to use profiles in cosmology](https://arxiv.org/pdf/2408.07700)
- [Why isn't every physicist a Bayesian? ](https://www.astro.princeton.edu/~strauss/AST303/bayesian_paper.pdf)
- [Feldman-Cousins boundary corrections](https://arxiv.org/pdf/physics/9711021)


---