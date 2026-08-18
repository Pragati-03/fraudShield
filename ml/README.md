# Machine Learning

This folder will hold the FraudShield anomaly detection and classification components.

**Status:** Not yet implemented. No model has been trained. No datasets, notebooks, or accuracy figures exist yet — this is planned Phase 2/3 work.

## Planned Stack
- Scikit-learn
- XGBoost

## Planned Scope
- Feature engineering on transaction and behavioral signals
- Merchant-specific behavioral baselines
- Anomaly detection for deviations from a merchant's normal transaction pattern
- Supervised classification for known fraud patterns
- Contribution to the Explainable AI layer (surfacing which factors drove a given risk score)
- Evaluation: precision/recall analysis and false-positive review (Phase 4)

No claims of model accuracy, training status, or production readiness are made until this work is actually completed and evaluated.

See the [Phase 1 Proposal](../docs/Phase1_Proposal.pdf) for how this layer fits into the overall architecture.
