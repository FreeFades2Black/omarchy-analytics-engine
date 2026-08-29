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
