# A Generation–Distillation Foundation Model for Post-Photocoagulation Fundus Images

---

[![Status](https://img.shields.io/badge/Manuscript-Under%20Review-orange)]()
[![Framework](https://img.shields.io/badge/PyTorch-2.x-ee4c2c)](https://pytorch.org/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-3776ab)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

**PostGD** is a **Generation–Distillation Foundation Model** designed for  
**post-photocoagulation fundus image analysis**.

It integrates **prior-guided postoperative image synthesis** with **foundation-level representation distillation** to learn **robust and transferable postoperative representations** under **extremely limited annotations**, supporting dense and semantic follow-up tasks such as **segmentation, localization, and classification**.

> 📌 **Note**: The accompanying manuscript is currently *under review*.  
> A public preprint and project page will be released upon acceptance.

---

## ✨ Highlights

> **PostGD** — A generation–distillation paradigm that bridges **clinically constrained synthesis** and **foundation model distillation** for objective postoperative fundus follow-up.

- 🧬 Prior-guided synthesis with anatomical & therapeutic constraints  
- 🧠 Foundation distillation from a frozen teacher to a lightweight student  
- 🧩 Unified multi-task adaptation for postoperative analysis  
- 📈 Strong performance under few-shot / low-label regimes  

---

## 🧭 1. Motivation: From Experience-driven to Foundation-based Follow-up

Conventional post-photocoagulation follow-up relies heavily on **subjective visual inspection** by clinicians.  
PostGD enables **structured representations and quantitative measurements**, facilitating **objective and reproducible** postoperative assessment.

<div align="center">
  <img src="assets/fig1_paradigm.png" width="92%"/>
  <br>
  <em>PostGD transforms experience-driven follow-up into foundation-based representation learning.</em>
</div>

---

## 🌀 2. Prior-Guided Postoperative Data Engine

Instead of naive synthesis, PostGD enforces **clinically valid constraints** during data generation:

- **Anatomical priors**: optic disc/cup, macula, vessels  
- **Therapeutic priors**: laser spot placement and distribution  
- **Visual realism**: foundation-generated backgrounds + constrained spot synthesis  

<div align="center">
  <img src="assets/fig2_generation.png" width="92%"/>
  <br>
  <em>Anatomically and therapeutically consistent postoperative fundus synthesis.</em>
</div>

---

## 🔥 3. Foundation Distillation for Postoperative Representation Learning

PostGD distills structural and semantic priors from a **frozen foundation teacher** into a **compact student backbone**, using large-scale synthetic postoperative data.

This enables:
- Stable representation learning under limited real annotations  
- Efficient downstream adaptation  
- Lightweight deployment  

<div align="center">
  <img src="assets/fig3_distillation.png" width="92%"/>
  <br>
  <em>Foundation distillation aligns synthetic and real postoperative representations.</em>
</div>

---

## 🧩 4. Multi-task Adaptation

A shared distilled backbone supports multiple follow-up tasks with lightweight heads:

- **Segmentation**: laser scars, vessels, optic disc/cup  
- **Localization**: fovea, optic disc center  
- **Classification**: postoperative outcomes  

<div align="center">
  <img src="assets/fig4_multitask.png" width="92%"/>
  <br>
  <em>One backbone, multiple postoperative tasks.</em>
</div>

---

## 🛠️ Installation

```bash
git clone https://github.com/<yourname>/<yourrepo>.git
cd <yourrepo>

conda create -n postgd python=3.10 -y
conda activate postgd
pip install -r requirements.txt

