<h1 align="center">Energy Discrepancy</h1>
<p align="center">
    <a href="https://nips.cc/virtual/2023/poster/72991"> <img alt="License" src="https://img.shields.io/static/v1?label=Pub&message=NeurIPS%2723&color=blue"> </a>
    <a href="https://nips.cc/virtual/2023/poster/72991"> <img src="https://img.shields.io/badge/Video-grey?logo=Kuaishou&logoColor=white" alt="Video"></a>
    <a href="https://nips.cc/virtual/2023/poster/72991"> <img src="https://img.shields.io/badge/Slides-grey?&logo=MicrosoftPowerPoint&logoColor=white" alt="Slides"></a>
    <a href="https://nips.cc/virtual/2023/poster/72991"> <img src="https://img.shields.io/badge/Poster-grey?logo=airplayvideo&logoColor=white" alt="Poster"></a>
</p>

This repo contains PyTorch implementation of the paper "[Energy Discrepancies: A Score-Independent Loss for Energy-Based Models](https://arxiv.org/abs/2307.06431)"

by [Tobias Schröder](https://tobias-schroeder.github.io/), [Zijing Ou](https://j-zin.github.io/), [Jen Ning Lim](https://scholar.google.com/citations?user=Uryp_N8AAAAJ&hl=en), [Yingzhen Li](http://yingzhenli.net/home/en/), [Sebastian Vollmer](https://scholar.google.co.uk/citations?user=WoqSEpYAAAAJ&hl=en), and [Andrew Duncan](https://www.imperial.ac.uk/people/a.duncan).

> We propose a novel loss function called Energy Discrepancy (ED)
which does not rely on the computation of scores or expensive Markov chain
Monte Carlo. We show that ED approaches the explicit score matching and negative log-likelihood loss under different limits, effectively interpolating between
both. Consequently, minimum ED estimation overcomes the problem of nearsightedness encountered in score-based estimation methods, while also enjoying
theoretical guarantees. Through numerical experiments, we demonstrate that ED
learns low-dimensional data distributions faster and more accurately than explicit
score matching or contrastive divergence. For high-dimensional image data, we
describe how the manifold hypothesis puts limitations on our approach and demonstrate the effectiveness of energy discrepancy by training the energy-based model
as a prior of a variational decoder model.

## Experiments

We provide the notebooks to reproduce the experiments in the paper:

- `myopia_ed_sm_mle.ipynb`: Reproduce Figure 1 (comparison of nearsightedness of Energy Discrepancy, Maximum Likelihood Estimation, and Score Matching)
- `w_stabilisation.ipynb`: Reproduce Figure 2 (understanding the w-stabilisation)
- `density_estimation.ipynb`: Density estimation on 2D toy data
- `edlebm_mnist.ipynb`: Training ED-LEBM on MNIST
