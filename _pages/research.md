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

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">세포는 배양 접시 위에 눕혀두면 조직이 되지 않습니다. 3차원 기질 안에서 서로 당기고 정렬해야 조직다운 구조가 나옵니다. 기질의 조성과 물성, 배양 중 가하는 기계적 자극이 표현형을 결정합니다. 지금은 골격근과 혈관 조직을 이 방식으로 만들고 있습니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/device.jpg" title="Microfluidic device on the microscope stage" class="img-fluid rounded" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/tissue.jpg" title="Band-shaped 3D muscle formed by cell contractile force" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  The device, and the tissue it makes. Cells pull the hydrogel taut between two
  pillars until it becomes a suspended muscle band.
</div>

Cells plated flat do not become tissue. They need a three-dimensional matrix to pull
against, and the forces they generate are what shape the construct. We use that as the
forming mechanism: hydrogel fills the channel and the cells compact it against anchor
pillars until a suspended tissue band appears.

**Extracellular matrix mechanobiology** is the control knob. Stiffness, viscoelasticity
and mechanical loading set cell phenotype, so the same cells give different tissue
depending on what we build them into. Skeletal muscle and vasculature are where we have
taken this furthest; the design rules are not specific to either.

#### Journal Publications

"Strategic Approaches in Generation of Robust Microphysiological 3D Musculoskeletal Tissue System."
Kim et al., _Advanced Functional Materials_ 2024

"Development of a 3D Vascularized Skeletal Muscle Model Using Bi-Layered Seeding Methods."
Kim et al., _BioChip Journal_ 2025

---

## Screening at a throughput a model can learn from

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">신약 개발이 오래 걸리고 비싼 이유 중 하나는 후보물질을 검증할 수단이 부족하기 때문입니다. 조직 하나에서 약물 조건 수십 개를 한 번에 시험할 수 있으면, 그 검증에 드는 시간과 비용이 줄어듭니다. 동시에 모델이 학습할 만큼의 데이터가 쌓입니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/screening.jpg" title="Drug concentration gradient chip" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  The gradient chip. Two inlets and two outlets produce a linear series of
  concentrations across the well array, checked against simulation.
</div>

Bringing a drug to the clinic is slow and expensive, and a large part of that cost sits
in testing candidates that will not work. Three-dimensional tissue tests them better than
flat culture does, but it is expensive to run at any scale. Our answer is a concentration
gradient chip that turns a single tissue specimen into a screen.

- **24 independent drug districts** from only two inlets and two outlets
- One 4 × 4 mm tissue specimen tested against **96 drug conditions in parallel**
- Well pitch matched to a 384-well plate, so a multichannel pipette works directly
- 300 × 300 µm culture compartments

Two things follow. Candidate compounds can be narrowed down earlier, on human tissue
rather than on cells in a dish. And organ-on-a-chip data becomes large enough to train a
model on, not only to validate one against.

---

## Quantitative readouts of tissue state

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">어떤 실험 결과든 다른 연구실에서 재현되지 않으면 근거가 되지 못합니다. 수축력·이미징·전사체처럼 단위가 다른 측정을 하나의 축에 올리고, 그 과정을 사람이 손으로 조정하지 않게 만드는 일이 먼저입니다. 정량화 과정 자체를 연구 대상으로 삼는 이유입니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/quant.jpg" title="Label-free image analysis pipeline" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  A brightfield image becomes a measurement. Contrast is equalised and the threshold
  is chosen by the data, not tuned by hand.
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
Kim et al., _Biosensors and Bioelectronics_ 2025

"Investigation on the Effect of Cyclic Stretch and Hypoxia on Recovery of Damaged Skeletal Muscle Cells Using Microfluidic System."
Kim et al., _Advanced Materials Technologies_ 2021

---

## Inter-organ interaction and drug-induced injury

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">임상시험에서 약이 실패하는 흔한 이유가 예상치 못한 장기 독성입니다. 한 조직만 보는 시험으로는 이것을 미리 잡아내지 못합니다. 근육에서 시작된 손상이 신장으로 이어지는 과정을 공배양 소자에서 재현해, 조직 사이의 연결 자체를 측정합니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/interorgan.jpg" title="Muscle and kidney tissue under drug treatment" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Muscle and kidney under drug treatment. Injury that starts in one compartment is
  read out in the other.
</div>

Drugs do not act on one tissue at a time. Statin-induced rhabdomyolysis begins in
skeletal muscle, and the muscle contents released into circulation injure the kidney.
Neither tissue alone reports that cascade, and neither does a model trained on one.

We reproduce the interaction in a coculture device so that the coupling itself becomes
measurable — and so that a model has something to learn the coupling from.

#### Journal Publications

"Implementation of Drug-Induced Rhabdomyolysis and Acute Kidney Injury in Microphysiological System."
Kim et al., _Advanced Functional Materials_ 2026

"Investigation of the Dysfunction Caused by High Glucose, Advanced Glycation End Products, and Interleukin-1 Beta and the Effects of Therapeutic Agents on the Microphysiological Artery Model."
Nam et al., _Advanced Healthcare Materials_ 2024

---

## From tissue to a feature matrix

<p class="text-muted" style="font-size:.92rem; margin-top:.4rem">AI가 내놓는 후보는 많지만 그것을 검증할 실험 데이터는 부족합니다. 이미징·형태·기능·오믹스 네 종류의 측정을 하나의 특징 행렬로 만들어 모델이 학습할 수 있는 형태로 바꿉니다. 학습 데이터와 검증 실험이 같은 실험실에서 나오므로, 예측이 틀렸는지를 곧바로 확인할 수 있습니다.</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-9 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/model.jpg" title="Per-cell segmentation" class="img-fluid rounded" %}
  </div>
</div>
<div class="caption">
  Every cell is segmented. Each one becomes a row of measurements.
</div>

The platform produces four kinds of data, and the work is turning them into one table a
model can read.

| Modality          | What it captures                                             |
| ----------------- | ------------------------------------------------------------ |
| **Imaging**       | tissue architecture, alignment and viability across the chip |
| **Morphometrics** | per-cell shape, size and orientation                         |
| **Functional**    | contractile force, barrier permeability, dose response       |
| **Omics**         | transcriptomic state, reduced to pathway-level scores        |

These become a feature matrix of _samples × features_, which is what a model actually
learns from. Because the training data and the validation experiment come from the same
bench, a prediction here can be falsified rather than merely reported. That is the part
of machine learning for drug discovery that is usually missing.
