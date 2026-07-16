---
hide:
  - toc
---

# Machine Learning

Applying machine learning to materials discovery — starting with superconductors.

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

**[→ Tc Prediction Tool](hes-tc-predictor/index.html)**{ .md-button .md-button--primary }

Enter any multi-component alloy formula and get an instant Tc estimate across
all six models, with parity plots and a cryogenic-scale visualisation.
