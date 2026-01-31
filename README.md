[![header](https://capsule-render.vercel.app/api?type=rect&height=120&color=gradient&text=PostGD%20-%20Generation%E2%80%93Distillation%20Foundation%20Model&fontAlign=50&reversal=true&textBg=false&fontAlignY=37&fontSize=38&desc=For%20Post-Photocoagulation%20Fundus%20Follow-up%20in%20Medical%20Vision&descSize=24&descAlign=50&descAlignY=75)](https://arxiv.org/abs/XXXX.XXXXX)
---

[![Paper](https://img.shields.io/badge/arXiv-Paper-b31b1b)](https://arxiv.org/abs/XXXX.XXXXX)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Framework](https://img.shields.io/badge/PyTorch-2.x-ee4c2c)](https://pytorch.org/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-3776ab)](https://www.python.org/)

**PostGD** is a **Generation–Distillation Foundation Model** tailored for **post-photocoagulation fundus images**.  
It integrates **prior-guided synthesis** (therapy- & anatomy-consistent laser patterns) with **foundation distillation** (e.g., DINOv3 teacher → lightweight student) to learn **robust postoperative representations** under **limited annotations**, enabling **segmentation / localization / classification** follow-up tasks.

---

> **[Paper Title Here]**  
> Authors: *Your author list*  
> Venue: *IEEE TMI / MICCAI / ICCV workshop / etc.*  
> **Project Page:** (optional)  
> **arXiv:** https://arxiv.org/abs/XXXX.XXXXX

---

## ✨ Highlights

> **PostGD** — a generation–distillation paradigm that **pretrains on clinically constrained synthetic postoperative fundus** and **distills foundation priors** for **data-efficient** postoperative follow-up.

- 🧠 **Foundation-level distillation** from a frozen teacher backbone to a compact student
- 🧬 **Prior-guided postoperative synthesis** with anatomical constraints (disc / macula / vessels) + therapy constraints (laser placement)
- 🧩 **Multi-task adaptation** with lightweight heads for segmentation / localization / classification
- 📈 Consistent gains in few-shot / low-label settings across multiple downstream tasks

---

## 🧭 1. From Conventional Follow-up → Foundation-based Follow-up

Clinical follow-up is often **experience-driven** and subjective. PostGD enables **structured representations** and **quantitative measures** for objective postoperative assessment.

<div align="center">
  <img src="assets/fig1_pipeline.png" width="92%" alt="PostGD motivation and paradigm"/>
  <br>
  <em>PostGD bridges experience-driven follow-up and foundation-based follow-up via generation–distillation.</em>
</div>

---

## 🌀 2. Prior-Guided Postoperative Data Engine

Instead of naive synthesis, PostGD enforces **clinically valid priors**:
- anatomy: optic disc/cup, macula, vessels
- therapy: **photocoagulation spot layout constraints**
- realism: background generation + constrained spot synthesis

<div align="center">
  <img src="assets/fig2_generation.png" width="92%" alt="Prior-guided synthesis"/>
  <br>
  <em>Prior-guided synthesis produces anatomically and therapeutically consistent postoperative fundus images.</em>
</div>

---

## 🔥 3. Foundation Distillation for Postoperative Representation Learning

We distill rich structural/semantic priors from a frozen teacher (e.g., DINOv3) into a lightweight student backbone using large-scale synthetic postoperative data.

<div align="center">
  <img src="assets/fig3_distill.png" width="92%" alt="Representation distillation"/>
  <br>
  <em>Distillation aligns postoperative representations under limited real annotations.</em>
</div>

---

## 🧩 4. Multi-task Adaptation for Downstream Follow-up

A shared distilled backbone + lightweight task heads:
- **Segmentation:** laser spots / vessels / disc-cup / lesions
- **Localization:** fovea / disc center (ED in pixels)
- **Classification:** postoperative status / edema outcome / etc.

<div align="center">
  <img src="assets/fig4_multitask.png" width="92%" alt="Multi-task adaptation"/>
  <br>
  <em>One distilled backbone supports multiple postoperative tasks with minimal task-specific parameters.</em>
</div>

---

## 📦 News / Updates
- **2026-XX-XX:** Code release (initial).
- **2026-XX-XX:** Added synthetic generation scripts + distillation configs.
- **2026-XX-XX:** Added multi-task heads and evaluation.

---

## 🛠️ Installation

### 1) Clone
```bash
git clone https://github.com/<yourname>/<yourrepo>.git
cd <yourrepo>
