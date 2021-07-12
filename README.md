**[abstract](#Abstract) | [contents](#Contents) | [usage](#Usage) | [running the notebooks](#running-the-notebooks) | [issues](#issues) | [citation](#citation) | [license](#license)**

# Hybrid parametric/smooth inversion of electrical resistivity tomography data
[![DOI](https://zenodo.org/badge/299123589.svg)](https://zenodo.org/badge/latestdoi/299123589)

These notebooks can be used to reproduce inversion results from the following paper submitted to Computers & Geosciences: [(Herring et al., 2021)](./herring-et-al-C&G-2021.pdf). 

## Abstract 

The standard smooth electrical resistivity tomography inversion produces an estimate of subsurface conductivity that has blurred boundaries, damped magnitudes, and often contains inversion artifacts. In many problems the expected conductivity structure is well constrained in some parts of the subsurface, but incorporating prior information in the inversion is not a trivial task. In this study we developed an electrical resistivity tomography (ERT) inversion algorithm that combines parametric and smooth inversion strategies. In regions where the subsurface is well constrained, the model was parameterized with only a few variables, while the rest of the subsurface was parameterized with voxels. We tested this hybrid inversion strategy on two synthetic models that contained a well constrained highly resistive or conductive near-surface horizontal layer and a target beneath. In each testing scenario, the hybrid inversion improved resolution of feature boundaries and magnitudes and had fewer inversion artifacts than the standard smooth inversion. A sensitivity analysis showed that the hybrid inversion successfully recovered subsurface features when a range of regularization parameters, initial models, and data noise levels were tested. The hybrid inversion strategy can potentially be expanded to a range of applications including marine surveys, permafrost/frozen ground studies, urban geophysics, or anywhere that prior information allows part of the model to be constrained with simple geometric shapes.

## Contents

There are two notebooks in this repository. Each notebook tests the hybrid inversion using a synthetic resistivity dataset. Two scenarios are considered here:

1. [frozen_layer](./frozen_layer.ipynb): This notebook presents a scenario with a conductive contaminant plume beneath a seasonally frozen surface layer.
2. [cnns-for-uxo](./infiltration.ipynb): This notebook presents a scenario where the ERT survey is installed at the base of a managed aquifer recharge pond. There is a water layer above the electrodes and a zone of infiltration below the electrodes.

There are also several files that are loaded into the notebooks to describe the temperature profiles, the soil freezing characteristic curve for the frozen layer scenario, and the saturation profile for the infiltration scenario.

## Usage

Here are step-by-step instructions for running these notebooks locally on your machine:

Install Python. You can use [anaconda](https://www.anaconda.com/download/) for this.

Clone this repository by running the following in your command line:

```
git clone https://github.com/simpeg-research/Herring-2021-Hybrid-ERT-Inversion.git
```

Next, `cd` into the directory you just created:

```
cd Herring-2021-Hybrid-ERT-Inversion
```

You can use the provided conda environment to set up the necessary software packages:

```
conda env create -f environment.yml
conda activate hybrid_ert
```

You can then launch Jupyter with the following command

```
jupyter notebook
```

And a Juputer notebook will launch in your web browser.

## Running the notebooks

You can run each cell in the notebook individually by pressing  `shift + enter`, or you can run the entire notebook by selecting `Cell`, `Run All` in the toolbar.

## Issues

Please [make an issue](https://github.com/simpeg-research/Herring-2021-Hybrid-ERT-Inversion/issues) if you encounter any problems while trying to run the notebooks.

## Citation

To cite this work, please reference

Herring, T., Heagy, L., Pidlisecky, A. & Cey, E. (2021, in review). Hybrid parametric/smooth inversion of electrical resistivity tomography data. Computers & Geosciences.

## License
These notebooks are licensed under the [MIT License](/LICENSE) which allows academic and commercial re-use and adaptation of this work.

