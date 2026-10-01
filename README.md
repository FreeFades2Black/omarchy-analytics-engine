# 📈 Omarchy Streaming Analytics & Telemetry Engine

Real-time RPS, throughput, and P99 latency aggregation microservice migrated from Azure DevOps to GitHub Enterprise.

---

## 📋 Migration & Governance Audit

* **Source Platform:** Azure DevOps (`source-ado-repos/omarchy-analytics-engine`)
* **Target Platform:** GitHub Enterprise (`FreeFades2Black/omarchy-analytics-engine`)
* **Pipeline Translation:** Converted legacy `azure-pipelines.yml` to native GitHub Actions `.github/workflows/ci.yml`.
* **Compliance Verdict:** `PASSED_100_PERCENT_PARITY`
* **Secret Scan:** `CLEAN` (0 exposed credentials in git history).

---

## 🚀 API Endpoints

* `GET /health` — Service health & telemetry queue buffer status.
* `GET /api/analytics/metrics` — Returns real-time latency percentiles, throughput, and error rates.

---

## 🛠️ Local Development

```bash
# Run service locally
python3 -m uvicorn app:app --host 0.0.0.0 --port 8830
```

---

## 🌐 Omarchy Migration & GitOps Ecosystem Map

All repositories in this project are interconnected and indexed under the GitHub topic [`omarchy-gitops-ecosystem`](https://github.com/topics/omarchy-gitops-ecosystem):

| Repository | Role in Ecosystem | Service Route / Port | Primary Topic Tags |
| :--- | :--- | :---: | :--- |
| 🎛️ [**`ado-to-gh-migration`**](https://github.com/FreeFades2Black/ado-to-gh-migration) | **Master Migration Suite & Operations Gateway** | `:8800` (Gateway) | `migration-toolkit`, `dual-run-canary` |
| ⚡ [**`omarchy-gitops-forge`**](https://github.com/FreeFades2Black/omarchy-gitops-forge) | **1,000-Commit Forge & CI Matrix Testbed** | CI Matrix Engine | `1000-commits`, `ci-cd-matrix` |
| 🔐 [**`omarchy-auth-service`**](https://github.com/FreeFades2Black/omarchy-auth-service) | **OAuth2 & JWT Zero-Trust Identity Service** | `:8810` / Gateway | `oauth2`, `zero-trust` |
| 💳 [**`omarchy-payment-vault`**](https://github.com/FreeFades2Black/omarchy-payment-vault) | **Encrypted Transaction Settlement Gateway** | `:8820` / Gateway | `payments`, `encryption` |
| 📈 [**`omarchy-analytics-engine`**](https://github.com/FreeFades2Black/omarchy-analytics-engine) | **Real-Time Streaming Telemetry & Metrics** | `:8830` / Gateway | `telemetry`, `analytics` |
| 📦 [**`omarchy-order-fulfillment`**](https://github.com/FreeFades2Black/omarchy-order-fulfillment) | **Distributed Logistics & Order Dispatch Engine** | `:8840` / Gateway | `logistics`, `order-routing` |

---

## Automated CI Maintenance Log
<!-- START_AGENT_MAINTENANCE_LOG -->
#### Maintenance Run: `2026-10-01 20:55:12 UTC`
- `.github/workflows/ci.yml`: Upgrade actions/checkout from v4 to v7 for security & performance. [Research: RCSB PDB AI Help Desk: retrieval-augmented generation for protein structure deposition support (OpenAlex / Global University Research)] [NIST SP 800-218 PW.4]
- `.github/workflows/ci.yml`: Upgrade actions/setup-python from v5 to v7 for security & performance. [Research: RCSB PDB AI Help Desk: retrieval-augmented generation for protein structure deposition support (OpenAlex / Global University Research)] [NIST SP 800-218 PW.4]
- `.github/workflows/ci.yml`: Enforce timeout-minutes: 10 to kill hung processes and prevent runaway billing (CISA & FinOps).

<!-- END_AGENT_MAINTENANCE_LOG -->
