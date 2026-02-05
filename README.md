# GBF & NER (Kerr black hole)

This repository contains a Julia notebook, `gbf_nmr.ipynb`, for computing (with $M=1$):

- The grey-body factors $\Gamma_{lm}(\omega)$ (numerical result vs. a QNM/GBF approximation)
- The particle number emission rate $\frac{\partial^2 N}{\partial \omega\partial t}$

Default example: We follow what is done in https://arxiv.org/abs/2504.01909v4 (Trinity of black hole correspondences: Shadows, quasinormal modes, graybody factors, and cautionary remarks) and set `a=0.99, s=1, l=1, m=1`.

## Dependencies

Julia packages used in the notebook:

- `GeneralizedSasakiNakamura`
- `Plots`
- `LaTeXStrings`

## How to run
Install Julia (recommend 1.10) and ensure your Jupyter setup has a Julia kernel (IJulia)

1. Clone this repository
2. Add the required packages in Julia REPL:

    ```julia
    using Pkg
    Pkg.activate(".")
    Pkg.add("GeneralizedSasakiNakamura")
    Pkg.add("Plots")
    Pkg.add("LaTeXStrings")
    ```
3. Open `gbf_nmr.ipynb` in vscode or Jupyter notebook
4. Run all cells to compute and plot the grey-body factors and emission rates.

Notes: the notebook plots $\Gamma_{lm}(\omega)$ and the corresponding emission rate, and compares numerics against the QNM/GBF approximation.


## How to cite
If you have used this code in your research that leads to a publication, please cite the following articles:
```
@article{Lo:2023fvv,
    author = "Lo, Rico K. L.",
    title = "{Recipes for computing radiation from a Kerr black hole using a generalized Sasaki-Nakamura formalism: Homogeneous solutions}",
    eprint = "2306.16469",
    archivePrefix = "arXiv",
    primaryClass = "gr-qc",
    doi = "10.1103/PhysRevD.110.124070",
    journal = "Phys. Rev. D",
    volume = "110",
    number = "12",
    pages = "124070",
    year = "2024"
}
```
and 
```
@article{Huang:2025rxx,
    author = "Huang, Zun-Xian and Li, Peng-Cheng",
    title = "{Quasinormal mode/grey-body factor correspondence for Kerr black holes}",
    eprint = "2512.23510",
    archivePrefix = "arXiv",
    primaryClass = "gr-qc",
    month = "12",
    year = "2025"
}
```
