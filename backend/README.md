# Backend

This folder will hold the FraudShield transaction ingestion, scoring, and API services.

**Status:** Not yet implemented — Phase 1 architecture and design stage only.

## Planned Stack
- FastAPI + Python
- PostgreSQL / Supabase
- WebSockets for real-time event delivery
- JWT authentication + role-based access control (RBAC)

## Planned Scope
- Real-time data ingestion API for incoming transactions
- Transaction validation & feature engineering pipeline
- Rule-based detection engine (velocity checks, amount thresholds, repeated failures, unusual timing, device/session anomalies)
- Risk Scoring Engine (combines rule-based + ML signals into a single 0–100 score)
- Decision Engine (routes transactions to Approve / Review / Block by risk tier)
- Merchant feedback endpoints feeding the learning loop
- Secure, encrypted handling of transaction and merchant data

See the [Phase 1 Proposal](../docs/Phase1_Proposal.pdf) and [system architecture](../docs/system-architecture.png) for the full design.
