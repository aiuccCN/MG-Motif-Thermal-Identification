# Integral parameter identification for thermal-hydraulic systems using mechanism-guided transient motifs

**Authors:** Dingyu Cao<sup>1</sup>, Rongxi Wang<sup>1, *</sup>, Zhenhu Zhang<sup>2</sup>, Haitao Zhang<sup>2</sup>, Yufan Li<sup>1</sup>, Jiangbo Li<sup>1</sup>, Jianmin Gao<sup>1</sup>

<sup>1</sup> *State Key Laboratory for Manufacturing Systems Engineering, Xi'an Jiaotong University, Xi'an 710049, China*  
<sup>2</sup> *Shaanxi Yanchang Petroleum (Group) Co., Ltd., Xi'an 710048, China*  
<sup>*</sup> *Corresponding author: Rongxi Wang (Email: rongxiwang@163.com)*

---

## Abstract

Thermal-hydraulic models calibrated on narrow commissioning data often lose accuracy during wide-range load cycling. Sparse historian sampling, sensor noise, and contiguous observation gaps complicate retrospective recalibration: numerical differentiation amplifies high-frequency noise, whereas unconstrained per-window splines can oscillate or overfit across missing intervals. This paper presents a dual-loop parameter identification method that combines mechanism-guided transient motifs (MG-Motif) with window-integral estimation. With initial parameters held fixed, the inner loop represents state trajectories as an observed-prefix baseline plus event-triggered cubic B-spline responses regularized by sliding-window conservation balances. Continuous $L^2$ Gram-weighted singular value decomposition extracts a low-rank orthonormal motif library with a bound on source truncation error. On wider-load batches, the outer loop estimates constitutive parameters and relaxation time constants via constrained window-integral least squares and screens candidate updates by open-loop validation before refreshing the motif library. On an isomorphic steam reheater benchmark at 20% Gaussian output noise, calibration reduces the relative parameter error $E_\theta$ from 14.43% to 3.12% ± 1.97% (component-balanced error 8.68%). Under structural mismatch on six unseen Simscape reheater cases, open-loop temperature root-mean-square error (RMSE) decreases from 1.268 to 0.570 K. On 2016 operating data from a 1036 MW ultra-supercritical steam turbine, calibration lowers open-loop normalized mean-square error (NMSE) by 31.0% (0.7893 to 0.5446) on 16 active-gap test windows and by 8.7% (0.5695 to 0.5198) across the 177-window wide-cycling test set, using 5.1- to 9.0-fold fewer per-window parameters than generalized smoothing.

**Keywords:** Thermal-hydraulic systems; Parameter identification; Mechanism-guided motifs; Integral conservation; State reconstruction; Steam turbine

---

## Highlights

- Event-triggered motifs identify thermal parameters from gapped plant data.
- Gram-orthogonal motifs reconstruct continuous states across missing intervals.
- An operator-norm bound links motif truncation to conservation residuals.
- Reheater parameter error drops from 14.43% to 3.12% at 20% noise.
- Open-loop error falls by 31.0% and 8.7% on a 1036 MW steam turbine.

---

## Repository Structure

```text
MG-Motif-Thermal-Identification/
├── code/          # Placeholder directory for MG-Motif & baseline scripts
├── data/          # Placeholder directory for benchmark & anonymized summary data
└── README.md      # Manuscript metadata, abstract, and availability statement
```

---

## Code and Data Availability

This repository currently hosts the project directory structure and manuscript metadata during journal submission and peer review.

- **For Peer Review:** Source code (`code/`) and anonymized benchmark datasets (`data/`) are available to editors and reviewers upon request from the corresponding author (`rongxiwang@163.com`).
- **Public Release:** Full reproducibility scripts and benchmark datasets will be uploaded to `code/` and `data/` upon formal publication of the manuscript, while raw power-plant DCS historian records remain subject to utility confidentiality agreements.

---

## Acknowledgements

This work was supported by the Shaanxi Provincial Key Research and Development Program under Grant 2024QY2-GJHX-02, and by the Science and Technology Project of China Huaneng Group Co., Ltd., under Grant HNKJ24-H86.
