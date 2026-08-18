# FraudShield
### Real-Time Fraud Intelligence & Prevention for Small Merchants

![Status](https://img.shields.io/badge/status-Phase%201%20%E2%80%94%20Idea%20%2F%20Architecture-2A5CE0)
![Hackathon](https://img.shields.io/badge/OMNIKON-National%20Hackathon%202026-0F1E36)
![Track](https://img.shields.io/badge/track-FinTech-1F3A63)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## Overview

FraudShield is a proposed hackathon solution for **Omni_FinTech_3**, submitted as part of the **OMNIKON National Hackathon 2026, Phase 1**.

It is designed to help small merchants detect suspicious digital-payment transactions in real time and make informed decisions through explainable risk scoring and recommended actions — without needing a dedicated fraud or security team.

> **FraudShield does not just flag a transaction — it tells the merchant why it is risky and what to do next.**

**Please note:**
- This repository is for the **OMNIKON National Hackathon 2026 — Phase 1 submission**.
- It represents the **proposed architecture, product design, and implementation roadmap** for FraudShield.
- It is **not** being presented as a fully deployed production system.
- No claims of measured model accuracy, live deployment, or real merchant usage are made anywhere in this repository.

---

## Problem Statement

**Problem Statement ID:** `Omni_FinTech_3`
**Title:** Real-Time Fraud Detection for Small Merchants

Small merchants increasingly rely on digital payments but often lack the fraud-monitoring capabilities available to larger businesses. Key challenges:

- **Slow identification** of suspicious transactions in real time
- **No dedicated fraud or security team** to monitor activity
- **Noisy, static rule-based alerts** that merchants learn to ignore
- **Lack of explainability** — a binary "fraud / not fraud" label gives no actionable context
- **Financial impact** of delayed detection, which can directly hurt a thin-margin small business

---

## Proposed Solution

FraudShield is built around a simple, repeatable loop:

**Detect → Explain → Act → Learn**

### Detect
Analyze every transaction in real time using transaction-level and behavioral signals.

### Explain
Show the specific factors contributing to the risk score, instead of a raw fraud/not-fraud label.

### Act
Recommend one clear next step:
- Approve
- Review
- Verify
- Block

### Learn
Use merchant feedback ("Fraud" / "Legitimate" / "Reviewed") to refine detection and build merchant-specific behavioral baselines over time.

---

## Key Features

1. **Real-Time Transaction Monitoring** — continuously watches transactions and flags suspicious activity with minimal delay
2. **Dynamic 0–100 Fraud Risk Score** — one understandable score per transaction
3. **Explainable Fraud Alerts** — surfaces the contributing risk factors behind every alert
4. **Merchant Behavioral Baseline** — learns each merchant's normal transaction pattern
5. **Smart Action Recommendations** — Approve / Review / Verify / Block based on risk tier
6. **Feedback-Driven Improvement** — merchant feedback continuously refines detection
7. **Fraud Analytics Dashboard** — transaction volume, flagged transactions, risk distribution, and trends

---

## System Architecture

```
Digital Payment / Transaction Source
        ↓
Real-Time Data Ingestion API
        ↓
Transaction Validation & Feature Engineering
        ↓
Rule-Based Detection Engine  +  ML Fraud Detection Engine
        ↓
Risk Scoring Engine
        ↓
Explainable AI Layer
        ↓
Decision Engine
        ↓
Merchant Dashboard + Real-Time Alerts
        ↓
Merchant Feedback → Feedback / Learning Layer → Model & Risk Profile Improvement
```

A full diagram is available at [`docs/system-architecture.png`](docs/system-architecture.png).

**Why both rule-based and ML detection?**
- **Rules** provide fast, transparent detection of known fraud patterns and require no training data.
- **ML** helps identify subtler behavioral anomalies and fraud patterns that evolve over time.

Shared platform foundations across every layer: PostgreSQL/Supabase, authentication & access control, a real-time API layer, monitoring & logging, and encrypted data handling.

---

## Technology Stack

| Layer | Technology | Purpose |
|---|---|---|
| Frontend | React.js + Tailwind CSS | Merchant dashboard and alert interface |
| Backend | FastAPI + Python | Transaction ingestion and scoring services |
| Machine Learning | Scikit-learn / XGBoost | Anomaly detection + supervised classification |
| Database | PostgreSQL / Supabase | Transactions, risk profiles, feedback |
| Real-Time | WebSockets | Live event processing and alert delivery |
| Visualization | Recharts / Chart.js | Analytics dashboard and trend charts |
| Security | JWT + RBAC | Encrypted data, role-based access, secure APIs |
| Deployment | Vercel + Render / Supabase | Practical, low-ops cloud deployment |

Every technology above was chosen for a specific purpose in the architecture — no unnecessary libraries are included.

---

## Implementation Roadmap

### Phase 1 — Foundation
- Merchant authentication & profiles
- Transaction ingestion API
- PostgreSQL / Supabase database
- Initial rule-based detection
- Basic merchant dashboard

### Phase 2 — Intelligence
- Transaction feature engineering
- Merchant behavioral baselines
- ML anomaly detection / classification
- Dynamic 0–100 risk scoring

### Phase 3 — Prevention
- Explainable fraud alerts
- Real-time notifications
- Approve / Review / Verify / Block workflow
- Merchant feedback loop

### Phase 4 — Validation & Deployment
- Precision / recall evaluation
- False-positive analysis
- Security & performance testing
- Cloud deployment & scalability

---

## Repository Status

**Phase 1 — Idea / Architecture Stage**

This repository currently contains the product proposal, architecture, and implementation plan submitted for Phase 1. It does **not** contain:
- A trained machine learning model
- A production deployment
- Measured accuracy, precision, or recall figures
- Real merchant users or transaction data
- Any guarantee of fraud prevention

---

## Future Development

Planned work beyond Phase 1 includes:

- Implementing the transaction ingestion pipeline
- Building the rule-based detection engine
- Training and evaluating ML models for anomaly detection
- Developing the merchant dashboard
- Adding explainable alerts and the risk-scoring UI
- Implementing the feedback-driven improvement loop
- Security and performance testing
- Cloud deployment

---

## Documentation

- 📄 [Phase 1 Proposal (PDF)](docs/Phase1_Proposal.pdf)
- 🗺️ [System Architecture Diagram](docs/system-architecture.png)
- [`frontend/`](frontend/README.md) · [`backend/`](backend/README.md) · [`ml/`](ml/README.md) · [`screenshots/`](screenshots/README.md)

---

## Team

| Name | Role | GitHub |
|---|---|---|
| _Add name_ | _Add role_ | _Add handle_ |
| _Add name_ | _Add role_ | _Add handle_ |
| _Add name_ | _Add role_ | _Add handle_ |

---

<sub>Submitted for OMNIKON National Hackathon 2026 · Problem Statement Omni_FinTech_3 · Phase 1</sub>
