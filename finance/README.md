# 🏦 Enterprise Multicurrency Chargeback & Fraud Matrix (2.5K)

## Asset Overview
This dataset contains 2,500 synthetic, high-fidelity cross-border e-commerce chargeback events. 

It is engineered specifically for Lead Data Scientists, Risk Engineers, and Fintech startups training machine learning models for anomaly detection, friendly fraud classification, and chargeback win-probability scoring.

## 🔒 Commercial Licensing
This repository contains a limited open-source teaser (50 rows) for local schema validation and testing. 

**[Purchase the full 2,500-Row Enterprise JSONL Dataset via Stripe](https://buy.stripe.com/14A9AV9gz9ce6sEdtrfIs05)**. 

*The full dataset is delivered instantly upon payment confirmation via secure cloud infrastructure.*

## Schema Definition
The dataset is formatted in strict `.jsonl` (JSON Lines). Every row contains:
* `transaction_id`: (String) Synthetic UUID.
* `timestamp_purchase`: (String) ISO 8601 date.
* `timestamp_chargeback_filed`: (String) ISO 8601 date.
* `financials`: (Object) Contains transaction/settlement amounts, currencies, and FX discrepancies.
* `device_fingerprint`: (Object) Contains IP vectors, proxy detection (boolean), and synthetic fraud risk scores (0-100).
* `customer_interaction_log`: (Array) A simulated multi-line support chat transcript regarding the dispute.
* `bank_reason_code_raw`: (String) The raw chargeback classification code.
* `merchant_win_probability`: (Float) A calculated 0.0 to 1.0 probability score.

## Data Sample (Teaser)
```json
{
  "transaction_id": "f8a9d2c1-4b7e-41a3-9c8d-123456789abc",
  "timestamp_purchase": "2026-02-15T14:32:01Z",
  "timestamp_chargeback_filed": "2026-03-05T09:15:44Z",
  "financials": {
    "transaction_amount": 1250.00,
    "transaction_currency": "EUR",
    "settlement_amount": 1345.50,
    "settlement_currency": "USD",
    "fx_loss_gain": -12.50
  },
  "device_fingerprint": {
    "ip_address": "185.10.25.44",
    "proxy_detected": true,
    "fraud_risk_score": 88
  },
  "customer_interaction_log": [
    "Customer: I never authorized this charge on my card.",
    "Agent: I see the transaction was made from a device in France. Were you traveling?",
    "Customer: No, I live in the US and have my physical card with me."
  ],
  "bank_reason_code_raw": "Fraudulent Transaction (Code 10.4)",
  "merchant_win_probability": 0.15
}
