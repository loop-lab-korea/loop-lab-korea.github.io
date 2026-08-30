---
layout: page
title: RESEARCH
permalink: /research/
nav: true
nav_order: 3
---

Research in LOOP Lab runs as one loop. We build the tissue, pull data from it, and
let that data design the next experiment.

---

## Microphysiological systems for human tissue

<div class="row justify-content-sm-center">
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/tissue.jpg" title="Engineered myobundle" class="img-fluid rounded" %}
  </div>
  <div class="col-sm-6 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/device.jpg" title="Muscle-kidney coculture device" class="img-fluid rounded" %}
  </div>
</div>

Three-dimensional skeletal muscle and vascular tissue are constructed in microfluidic
devices, with myotubes aligned in a central hydrogel channel and perfused from
adjacent media channels. Extracellular matrix composition and cyclic mechanical
loading are the design variables we use to direct tissue phenotype. Single-tissue
devices are extended into muscle–kidney interfaces, so that an injury originating in
one tissue can be observed as it reaches another. No single-tissue assay reports that
class of effect, and so no model trained on one can either.

#### Journal Publications

"Strategic Approaches in Generation of Robust Microphysiological 3D Musculoskeletal Tissue System."
Kim et al., *Advanced Functional Materials* 2024

"Development of a 3D Vascularized Skeletal Muscle Model Using Bi-Layered Seeding Methods."
Kim et al., *BioChip Journal* 2025

---

## Quantitative readouts of tissue state

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/quant.jpg" title="Per-cell quantification" class="img-fluid rounded" %}
  </div>
</div>

Contractile force, barrier permeability, fluorescence imaging and transcriptomic
profiles are measured in units that have nothing in common, and must be placed on a
shared axis before they can be compared across devices, batches and operators. We
treat the quantification pipeline as an object of study rather than a preprocessing
step. A readout that does not reproduce is not a readout, and a model fitted to one
is fitting noise.

#### Journal Publications

"Detrimental Effects of Advanced Glycation End-Products (AGEs) on a 3D Skeletal Muscle Model in Microphysiological System."
Kim et al., *Biosensors and Bioelectronics* 2025

"Investigation on the Effect of Cyclic Stretch and Hypoxia on Recovery of Damaged Skeletal Muscle Cells Using Microfluidic System."
Kim et al., *Advanced Materials Technologies* 2021

---

## Inter-organ interaction and drug-induced injury

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/interorgan.jpg" title="Muscle-kidney axis" class="img-fluid rounded" %}
  </div>
</div>

Drugs do not act on one tissue at a time. Rhabdomyolysis that begins in skeletal
muscle releases myoglobin that injures the kidney, a cascade that cannot be observed
in either tissue alone. We reproduce these interactions in multi-organ devices so
that the coupling itself becomes measurable, and so that a model has something to
learn the coupling from.

#### Journal Publications

"Implementation of Drug-Induced Rhabdomyolysis and Acute Kidney Injury in Microphysiological System."
Kim et al., *Advanced Functional Materials* 2026

"Investigation of the Dysfunction Caused by High Glucose, Advanced Glycation End Products, and Interleukin-1 Beta and the Effects of Therapeutic Agents on the Microphysiological Artery Model."
Nam et al., *Advanced Healthcare Materials* 2024

---

## Screening at a scale that trains a model

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/research/scale.jpg" title="Device footprint" class="img-fluid rounded" %}
  </div>
</div>

A model needs more than a handful of conditions, and a three-dimensional tissue is
expensive to run. Closing that gap is a research problem in itself: miniaturising the
device, automating culture and imaging, and keeping the functional readouts intact as
the format shrinks. The aim is screening throughput in a tissue that still behaves
like tissue. That is the point at which organ-on-a-chip data becomes large enough to
train on, not only to validate against.

---

## Predictive modeling of drug response

Dose–response modelling and machine learning are used to estimate efficacy and
toxicity across conditions that were never run, and those estimates then choose which
conditions we run next. The training data and the validation experiment come from the
same bench, so a prediction here can be falsified rather than merely reported. That is
the part of machine learning for drug discovery that is usually missing.

<sub>Directions the lab is building toward, on the platforms described above.</sub>
