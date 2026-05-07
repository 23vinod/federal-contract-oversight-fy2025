# Federal Contract Oversight: FY2025 Risk Classification Framework

**MS in Data Analytics | Catholic University of America | Spring 2026**  
**Team:** Akshitha Pitla, Sai Krishna Grandhi, Vinod Kumar Kethavath  
**Advisors:** Dr. Lin-Ching Chang, Matthew Jacobs

---

## Problem
The U.S. federal government awards $700B+ in contracts annually. 
With 600,000+ transactions, manual risk review is infeasible. 
No standardized automated framework exists for identifying high-risk awards at scale.

---

## Approach
- **Dataset:** FY2025 contract data from USASpending.gov — DoD, DHS, HHS (600,862 contracts)
- **Ground Truth:** Novel three-algorithm majority vote — K-Means + Isolation Forest + HDBSCAN
- **Classifiers:** Logistic Regression, Random Forest, XGBoost
- **Explainability:** SHAP TreeExplainer for contract-level feature attribution

---

## Key Results

| Model | Accuracy | Precision | Recall | F1 | ROC AUC |
|---|---|---|---|---|---|
| Logistic Regression | 76.0% | 19.6% | 54.1% | 0.29 | 0.68 |
| Random Forest | 90.6% | 44.4% | 17.6% | 0.25 | 0.75 |
| **XGBoost ★** | **85.4%** | **32.8%** | **59.1%** | **0.42** | **0.7574** |

- **39,161 contracts flagged as High Risk** (8.4% of labeled dataset)
- **Top risk driver:** `contract_financing` type (SHAP = 0.407)

---

## Project Structure
