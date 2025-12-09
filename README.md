<div align="center">

  <h2>✨ FLAIR: Frequency- and Locality-Aware Implicit Neural Representations</h2>

  <div style="margin-top:6px;">
    <a href="https://scholar.google.com/citations?user=-VcWf7oAAAAJ&hl=ko" target="_blank">Sukhun Ko</a><sup>1</sup>&nbsp;
    <a href="https://scholar.google.com/citations?user=GTWolqAAAAAJ&hl=ko" target="_blank">Seokhyun Yoon</a><sup>1</sup>&nbsp;
    <a href="https://scholar.google.com/citations?user=B9OneWIAAAAJ&hl=ko" target="_blank">Dahyeon Kye</a><sup>1</sup>&nbsp;
    <a href="https://sites.google.com/view/kylemin" target="_blank">Kyle Min</a><sup>2</sup>&nbsp;
    <a href="https://scholar.google.com/citations?user=3feNfdUAAAAJ&hl=ko&oi=sra" target="_blank">Chanho Eom</a><sup>1</sup>&nbsp;
    <a href="https://sites.google.com/view/ozbro" target="_blank">Jihyong Oh</a><sup>† 1</sup>
  </div>

  <div style="margin-top:4px;">
    <sup>1</sup>Chung-Ang University, South Korea<br>
    <sup>2</sup>Oracle, USA
  </div>

  <div style="margin-top:2px;">
    <sup>†</sup>Corresponding author
  </div>

</div>

---

<div align="center" style="margin-top:10px;">
  <a href="https://cmlab-korea.github.io/FLAIR/" target="_blank">
    <img src="https://img.shields.io/badge/🌐-Project%20Page-blue">
  </a>
  <a href="https://www.arxiv.org/pdf/2508.13544" target="_blank">
    <img src="https://img.shields.io/badge/arXiv-2508.13544-b31b1b.svg">
  </a>
  <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/cmlab-korea/FLAIR-arxiv">
</div>

---

<div align="center" style="margin-top:12px;">
  <h4>
    Official implementation of  
    <b>"FLAIR: Frequency- and Locality-Aware Implicit Neural Representations"</b>
  </h4>
</div>

<div align="center" style="margin-top:10px;">
    <img src="assets/fitting.png" alt="Teaser Result" width="95%">
    <p style="font-size:0.95em; max-width:850px;">
        <b>Qualitative comparison.</b> FLAIR achieves faithful reconstruction while mitigating frequency leakage, 
        enabled by the band-limited behavior of BLA. Existing INR models show noise amplification and high-frequency distortion.
    </p>
</div>

---

## 📧 News
- **Dec 09, 2025:** This repository is updated.

---

## ✨ Abstract

Implicit Neural Representations (INRs) encode signals by mapping coordinates to values using neural networks, enabling compact and continuous representations. While effective, existing INRs lack mechanisms for frequency selectivity and spatial localization, resulting in redundant feature learning and strong spectral bias—favoring low-frequency components while struggling to represent sharp details.

To address these limitations, we introduce **FLAIR**, a framework integrating two complementary innovations:  
(1) **Band-Localized Activation (BLA)**, a novel activation that enforces learnable band selection and spatial locality under the time-frequency uncertainty principle (TFUP).
(2) **Wavelet-Energy-Guided Encoding (WEGE)**, which leverages discrete wavelet energy to guide frequency signals into the network.

FLAIR consistently improves reconstruction fidelity across 2D image representation, 3D shape modeling, and novel-view synthesis.

---

## ⚙️ Method Overview

<div align="center">
    <img src="assets/fig1.png" alt="Architecture" width="95%">
</div>

**Right:** WEGE computes normalized wavelet-energy scores \(\tilde{w}_b\), assigning low weights to homogeneous regions (green) and higher weights to textured regions (red), enabling spatial frequency relevance.  
**Left:** The scores are concatenated with input coordinates and passed into BLA, where learnable parameters \((\zeta, T, \sigma)\) modulate frequency shifting and band-limiting behavior.

---


## 🚀 Code Release Plan

- [ ] 2D representation pipeline  
- [ ] 3D NeRF / SDF integration (built on external implementations)  
- [ ] Ablation studies (NTK, FFT, etc.)  
- [ ] Visualization toolkit  

---

## 📝 Citation

The official BibTeX entry will be updated.

