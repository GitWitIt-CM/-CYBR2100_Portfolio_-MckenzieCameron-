# AI Use in Security Operations

## Policy Snippet (final)  
**Scope & purpose:** This system covers email phishing alerts, anomaly detection, and login/access monitoring. Its goal is to flag unusual or risky activity quickly while keeping the process fair and explainable.  

**Transparency & notice:** Every alert will include a short reason code (e.g., “suspicious link” or “unfamiliar login”) so users know why something was flagged.  

**Human-in-the-loop:** For high-risk or unclear cases, the security team will review and can override automated decisions.  

**Appeals path:** Any user can appeal a decision using a simple form. Appeals will be resolved within one hour for routine issues and within 24 hours for high-risk blocks.  

**Data handling:** The system only collects the minimum needed data (like headers and URLs). Message bodies are redacted, and logs are retained no longer than 180 days for blocked items and 30 days for allowed traffic.  

**Metrics & review cadence:** We will track false positive and false negative rates by subgroup, publish metrics quarterly, and retrain models as needed to stay accurate and fair.  

---

## Controls & Metrics  
1. **False Positive Rate (FPR):** ≤0.8% overall and ≤1.1% for any subgroup, reviewed monthly.  
2. **False Negative Rate (FNR):** ≤8% (recall ≥92%), tracked monthly.  
3. **Appeals resolution time:** ≤1 hour for normal issues; ≤24 hours for high-risk cases.  
4. **Override rate:** Track % of alerts escalated to human analysts; reviewed quarterly.  
5. **Retraining cadence:** Retrain models if subgroup ΔFPR >0.3 percentage points or if FPR shifts >0.3 pp per quarter.  

---

## Justification  
These controls address risks identified in Chapter 11 of *Ethics in Technology* (Weber, 2025). Bias is reduced by subgroup audits, while automation bias is mitigated through human-in-the-loop overrides. Transparency and appeals uphold user rights, while data minimization limits unnecessary collection. Metrics like FPR/FNR ensure measurable performance, and quarterly review aligns with the NIST AI Risk Management Framework’s requirement to govern, measure, and manage AI systems responsibly.  

---

## Evidence Links  
 Weber, E. (2025). _Ethics in technology_.
 National Institute of Standards and Technology. (2023). _AI Risk Management Framework _(AI RMF 1.0). https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf 

---

## Reflection  
One trade-off I would revisit is the strict FPR threshold. While 0.8% seems reasonable, even small percentages generate many false alerts in large email systems, which can strain analyst time. Loosening the threshold slightly could reduce wasted review effort but risks missing real threats. Balancing analyst workload with security effectiveness remains a challenge. In future drafts, I would explore cost-sensitive evaluation to weigh the harm of false negatives against the noise of false positives.  

---

## AI Use Note  
I used ChatGPT to help connect risk concepts (bias, automation bias) to measurable controls.

