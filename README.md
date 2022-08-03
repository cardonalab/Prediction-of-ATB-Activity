# Introduction
This repository provides trained weights and materials associated with the manuscript "A Machine Learning Model trained on a High-Throughput Antibacterial Screen Increases the Hit Rate of Drug Discovery".

The code of directed message passing neural network (D-MPNN) used in this study was implemented in the open-source package [Chemprop](https://github.com/chemprop/chemprop), which is an effective graph neural network for molecular property prediction. The introduction, implementation, and application of D-MPNN can be found in below links:
- Yang et al (2019). Analyzing Learned Molecular Representations for Property Prediction. JCIM, 59(8), 3370–3388. https://doi.org/10.1021/acs.jcim.9b00237
- The original code: https://github.com/chemprop/chemprop
- Stokes et al (2020). A Deep Learning Approach to Antibiotic Discovery. Cell, 180(4), 688–702.e13. https://doi.org/10.1016/j.cell.2020.01.021

# Result summary
### Classification 
> Random split

| Model | Additional Features | ROC-AUC | PRC-AUC |
| ---- | ------ |  ------  |  ------  |
| 1 | No molecule-level features | 0.788 | 0.186 |
| 2 | [RDKit descriptors](https://github.com/bp-kelley/descriptastorus) | 0.795 | 0.232 |
| 3  | [RDKit descriptors + count-based Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 0.808 | 0.091 |
| 4 | [RDKit descriptors + binary Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 0.815 | 0.238 |

> Scaffold split

| Model | Additional Features | ROC-AUC | PRC-AUC |
| ---- | ------ |  ------  |  ------  |
| 5 | No molecule-level features | 0.845 | 0.170 |
| **6** | [RDKit descriptors](https://github.com/bp-kelley/descriptastorus) | 0.823 | 0.241 |
| 7  | [RDKit descriptors + count-based Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 0.784 | 0.191 |
| 8 | [RDKit descriptors + binary Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 0.820 | 0.180 |

### Regression 
> Random split

| Model | Additional Features | RMSE | MAE |
| ---- | ------ |  ------  |  ------  |
| 9 | No molecule-level features | 2.326 | 1.125 |
| 10 | [RDKit descriptors](https://github.com/bp-kelley/descriptastorus) | 2.290 | 1.104 |
| 11  | [RDKit descriptors + count-based Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 2.806 | 1.130 |
| 12 | [RDKit descriptors + binary Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 2.818 | 1.094 |

> Scaffold split

| Model | Additional Features | RMSE | MAE |
| ---- | ------ |  ------  |  ------  |
| 13 | No molecule-level features | 2.823 | 1.135 |
| 14 | [RDKit descriptors](https://github.com/bp-kelley/descriptastorus) | 2.548 | 1.138 |
| 15  | [RDKit descriptors + count-based Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 2.508 | 1.077 |
| 16 | [RDKit descriptors + binary Morgan fingerprints](https://github.com/bp-kelley/descriptastorus) | 2.564 | 1.058 |
