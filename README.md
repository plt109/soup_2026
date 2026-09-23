# SoUP2026 — Statistics lectures: slides and exercises

Teaching material for the Statistics lectures at [SoUP2026](https://soup2026.ca.infn.it/), the INFN School on Underground Physics (CeUB, Bertinoro, 26–30 October 2026).

The material covers two topics, each self-contained: **maximum likelihood estimation (MLE)** and **Monte Carlo / Markov chain Monte Carlo (MCMC)**. Each topic has a slide deck and Jupyter notebooks. 

## Contents

```
mle/
├── slides/
│   ├── soup_2026_mle.pptx          # editable
│   └── soup_2026_mle.pdf
└── coding_exercises/
    ├── mle_basics.ipynb                            # likelihood intuition, asymptotic distribution of the MLE
    ├── mle_extended_likelihood.ipynb               # extended likelihood fit on simulated particle showers
    ├── mle_extended_likelihood_instructions.pdf    # task sheet for the notebook above
    ├── mle_extended_likelihood_instructions/       # LaTeX source of the task sheet
    └── extended_likelihood_fake_data/              # simulated e-, gamma, mu- events + a "mystery" sample (.npy)

mcmc/
├── slides/
│   ├── soup_2026_mcmc.pptx         # editable
│   └── soup_2026_mcmc.pdf
└── coding_exercises/
    ├── mc_intro.ipynb              # estimating pi, inverse transform sampling, accept-reject
    └── metropolis_hastings.ipynb   # Metropolis-Hastings, autocorrelation, Gelman-Rubin statistic
```

### MLE

- **`mle_basics.ipynb`**: builds intuition for the likelihood function and shows numerically that the MLE of a Gaussian mean is asymptotically distributed as N(μ, σ²/N).
- **`mle_extended_likelihood.ipynb`**: a longer exercise using Geant4-style simulated showers of electrons, photons and muons. One would explore the data, compute Poisson upper and lower limits (Neyman construction), and estimate the electron fraction in a mystery sample with an extended likelihood fit. The task sheet is `mle_extended_likelihood_instructions.pdf`. The notebook loads its data from `./extended_likelihood_fake_data/`, so run it from `mle/coding_exercises/`.

### MCMC

- **`mc_intro.ipynb`**: Monte Carlo basics. Estimating π, inverse transform sampling and the accept-reject algorithm.
- **`metropolis_hastings.ipynb`**: writing a Metropolis-Hastings sampler, checking correlations between samples with the autocorrelation function, and assessing convergence across chains with the Gelman-Rubin statistic.

## Running the notebooks

The notebooks were developed with Python 3.11 and need:

```bash
pip install numpy scipy matplotlib tqdm jupyter
```

Then run `jupyter lab` from the repository root and open any notebook.

## Editing the slides

The `.pptx` files are the editable versions. They open in PowerPoint, Keynote and LibreOffice, and can be re-imported into Google Slides. The `.pdf` files are for viewing. If you edit a deck, re-export the PDF.

## Contact

Pueh Leng Tan, puehleng.tan@gmail.com
