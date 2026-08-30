---
layout: page
title: RESEARCH
permalink: /research/
nav: true
nav_order: 3
---

<link rel="stylesheet" href="{{ '/assets/css/loop.css' | relative_url }}">
> In the era of AI drug discovery, computational predictions are abundant.
> **Experimental validation is the bottleneck.**

Machine learning generates thousands of drug candidates, but a prediction is only worth
what the ground truth behind it is worth. LOOP Lab works on that side of the problem.
We build human tissue in microphysiological systems, run perturbations on it, and turn
the result into data a model can be judged against.

Research runs as one loop: build the tissue, pull data from it, and let that data design
the next experiment.

---

## Microphysiological systems for human tissue

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">세포가 스스로 젤을 수축시키는 힘을 이용해, 두 기둥 사이에 밴드 모양의 3차원 근조직을 만듭니다. 세포외기질의 조성과 물성이 조직의 표현형을 결정합니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/device.jpg" title="Microfluidic device on the microscope stage" class="img-fluid rounded" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/tissue.jpg" title="Band-shaped 3D muscle formed by cell contractile force" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Left: the device. Right: cell contractile force compacts an extracellular matrix
  hydrogel between two pillars into a band-shaped three-dimensional muscle.
</div>

Cells do not simply sit in a gel; they pull on it. We use that force as the forming
mechanism. Hydrogel fills the central channel, and the cells compact it against two
anchor pillars into a suspended tissue band. Pillar geometry, matrix composition,
gelation time and seeding density decide whether the result is robust enough to measure
repeatedly, and we characterised each of them.

**Extracellular matrix mechanobiology** is the control knob. Stiffness and
viscoelasticity of the matrix set cell phenotype, so the same cells give different
tissue depending on what we build them into.

#### Journal Publications

"Strategic Approaches in Generation of Robust Microphysiological 3D Musculoskeletal Tissue System."
Kim et al., *Advanced Functional Materials* 2024

"Development of a 3D Vascularized Skeletal Muscle Model Using Bi-Layered Seeding Methods."
Kim et al., *BioChip Journal* 2025

---

## Screening at a throughput a model can learn from

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">농도구배 칩으로 조직 하나에서 약물 조건 96개를 동시에 시험합니다. 모델이 학습할 만큼 데이터가 쌓이는 지점을 만드는 것이 목표입니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/screening.jpg" title="Drug concentration gradient chip" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Drug concentration gradient chip: a linear series of concentrations generated across
  the well array from two inlets and two outlets, verified against simulation.
</div>

A model needs more than a handful of conditions, and three-dimensional tissue is
expensive to run. Our answer is a concentration gradient chip that turns one tissue
specimen into a screen.

- **24 independent drug districts** from only two inlets and two outlets
- One 4 × 4 mm tissue specimen tested against **96 drug conditions in parallel**
- Well pitch matched to a 384-well plate, so a multichannel pipette works directly
- 300 × 300 µm culture compartments

That is the point at which organ-on-a-chip data becomes large enough to train on, not
only to validate against.

---

## Quantitative readouts of tissue state

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">수축력·이미징·전사체처럼 단위가 다른 측정을 하나의 축에 올립니다. 재현되지 않는 지표는 지표가 아니라고 보고, 정량화 과정 자체를 연구 대상으로 삼습니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/quant.jpg" title="Label-free image analysis pipeline" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Label-free pipeline: brightfield input, contrast equalisation, then a threshold chosen
  by the data rather than tuned by hand.
</div>

Contractile force, fluorescence imaging and transcriptomic profiles are measured in
units that have nothing in common, and must be placed on a shared axis before they can
be compared across devices, batches and operators. Force is not measured directly — it
is inferred from how far the pillars bend, which makes the calibration itself part of
the result.

We treat the quantification pipeline as an object of study rather than a preprocessing
step. Every threshold is chosen by the data, so the same input gives the same number
tomorrow. A readout that does not reproduce is not a readout.

#### Journal Publications

"Detrimental Effects of Advanced Glycation End-Products (AGEs) on a 3D Skeletal Muscle Model in Microphysiological System."
Kim et al., *Biosensors and Bioelectronics* 2025

"Investigation on the Effect of Cyclic Stretch and Hypoxia on Recovery of Damaged Skeletal Muscle Cells Using Microfluidic System."
Kim et al., *Advanced Materials Technologies* 2021

---

## Inter-organ interaction and drug-induced injury

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">약물은 한 조직에만 작용하지 않습니다. 근육에서 시작된 손상이 신장으로 이어지는 과정을 공배양 소자에서 재현해, 그 연결 자체를 측정 가능하게 만듭니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/interorgan.jpg" title="Muscle and kidney tissue under drug treatment" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Muscle and kidney compartments imaged under drug treatment: injury in one tissue read
  out in the other.
</div>

Drugs do not act on one tissue at a time. Statin-induced rhabdomyolysis begins in
skeletal muscle, and the muscle contents released into circulation injure the kidney.
Neither tissue alone reports that cascade, and neither does a model trained on one.

We reproduce the interaction in a coculture device so that the coupling itself becomes
measurable — and so that a model has something to learn the coupling from.

#### Journal Publications

"Implementation of Drug-Induced Rhabdomyolysis and Acute Kidney Injury in Microphysiological System."
Kim et al., *Advanced Functional Materials* 2026

"Investigation of the Dysfunction Caused by High Glucose, Advanced Glycation End Products, and Interleukin-1 Beta and the Effects of Therapeutic Agents on the Microphysiological Artery Model."
Nam et al., *Advanced Healthcare Materials* 2024

---

## From tissue to a feature matrix

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">이미징·형태·기능·오믹스 네 종류의 데이터를 하나의 특징 행렬로 만듭니다. 학습 데이터와 검증 실험이 같은 실험실에서 나오므로, 예측이 보고에 그치지 않고 반증될 수 있습니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/model.jpg" title="Per-cell segmentation" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Per-cell segmentation from a label-free image. Each object becomes a row of
  measurements.
</div>

The platform produces four kinds of data, and the work is turning them into one table a
model can read.

| Modality | What it captures |
|---|---|
| **Imaging** | tissue architecture, alignment and viability across the chip |
| **Morphometrics** | per-cell shape, size and orientation |
| **Functional** | contractile force, barrier permeability, dose response |
| **Omics** | transcriptomic state, reduced to pathway-level scores |

These become a feature matrix of *samples × features*, which is what a model actually
learns from. Because the training data and the validation experiment come from the same
bench, a prediction here can be falsified rather than merely reported. That is the part
of machine learning for drug discovery that is usually missing.
