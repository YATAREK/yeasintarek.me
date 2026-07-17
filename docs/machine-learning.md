---
hide:
  - toc
---

---
hide:
  - toc
---

# Machine Learning

Applying machine learning to materials discovery — starting with superconductors.

---

## High-Entropy Superconductor Tc Prediction

Predicting the critical temperature (Tc) of high-entropy alloy (HEA)
superconductors from composition alone is an open challenge. Existing tools
predict Tc but ignore a practical question: will the alloy even form a stable
single-phase structure? We built a two-stage ML pipeline that answers both.

**Stage 1 — Phase stability classifier.** An Extra Trees model trained on
11,247 experimentally observed HEA compositions (Peivaste et al., *Sci Rep*
2023) predicts whether a given formula will form a single-phase BCC solid
solution — the structure where nearly all known HES superconductors live.
The classifier achieves 96% accuracy on BCC identification and 83% across
six phase categories (BCC, FCC, BCC+FCC, intermetallic, amorphous, mixed).

**Stage 2 — Tc predictor.** Six regression models (Extra Trees, Random Forest,
Gradient Boosting, XGBoost, SVR, KNN) trained on 66 HES compositions using
138 Magpie composition-derived features via matminer. The best model (Extra
Trees) reaches R² = 0.60 under cross-validation — sufficient for ranking
candidates and guiding experimental priorities.

The combination is the key contribution: the phase gate filters out
compositions unlikely to form a stable single-phase alloy before Tc is
predicted, reducing misleading estimates and focusing attention on
experimentally viable candidates.

[→ Tc Prediction Tool](hes-tc-predictor/index.html){ .md-button }

---

## High-Entropy Superconductor Tc Prediction

High-entropy alloys (HEAs) are a promising class of superconducting materials,
but predicting their critical temperature (Tc) from composition alone remains
challenging. We trained six ML models (Extra Trees, Random Forest, Gradient
Boosting, XGBoost, SVR, and KNN) on a curated dataset of 66 HEA superconductors,
using 138 composition-based features derived from the Magpie descriptor set via
matminer.

The best model (Extra Trees) achieves an R² of 0.60 under cross-validation —
enough to rank candidates and guide experimental priorities, though not a
substitute for measurement.

[→ Tc Prediction Tool](hes-tc-predictor/index.html){ .md-button }

Enter any multi-component alloy formula and get an instant Tc estimate across
all six models, with parity plots and a cryogenic-scale visualisation.
