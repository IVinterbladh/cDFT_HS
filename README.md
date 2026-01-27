[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/mlund/template-for-supporting-information/HEAD)
[![CC BY 4.0][cc-by-shield]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

# Electronic Notebook for cDFT calculations

A slit system with Lennard-Jones fluid is studied with classical density functional theory (cDFT). The walls are parallel at the distances $z=0$ and $z=h$. 

The grand potential functional is minimized via Picard iterations by solving the Euler-Lagrange equation to obtain equilibrium density profiles $n(z)$ for different wall separations, $h$. From these equilibrium densities, the grand potential per unit area $\Omega(h) \equiv \omega(h)$ and the solvation force $F_s(h) = -d\omega/dh$, which is the effective interaction between the two walls of the slit system, are calculated. 

The values used for the parameters are taken from the article by Freasier and Nordholm [1]. The parameters $\epsilon, \sigma, \epsilon_w$ and $\sigma_w$ were set to 1.0 and the bulk density was set to 0.035. 




## Layout

Description of the directory layout.

- `README.md` This is the file you're viewing right now.
- `environment.yml` Defines the required Python packages using conda. 
- `pyproject.toml` and `github/workflows/ruff.yml` sets up ruff linting for Python and Jupyter Notebooks. Delete if not relevant to your project.

## Requirements

To run the Notebooks online, click on the _Launch Binder_ badge above. Alternatively, to run on your own computer,
install Python using _e.g._ [Miniforge](https://github.com/conda-forge/miniforge) or [Anaconda](https://docs.conda.io)
and make sure all required packages are loaded by issuing the following terminal commands

``` bash
conda env create -f environment.yml
source activate my_environment
jupyter-lab
```

## References
[1] Ben C. Freasier, Sture Nordholm; A generalized van der Waals model for solvation forces between solute particles in a colloidal suspension. J. Chem. Phys. 1 November 1983; 79 (9): 4431–4438. https://doi.org/10.1063/1.446328

