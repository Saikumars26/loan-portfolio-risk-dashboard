# Loan Portfolio Risk & Expected Loss Dashboard (Tableau + Python)

A credit risk analytics project using **1.35M+ consumer loans** to quantify default risk, estimate **expected loss**, and build a **risk score** used in an interactive **Tableau Public dashboard**.

## Live Dashboard
- Tableau Public: <PASTE_YOUR_TABLEAU_PUBLIC_LINK_HERE>

## Key Results (What I found)
- Default rate increases sharply by credit grade (A → G): **~6% (A)** to **~50% (G)**.
- Expected loss is concentrated in mid-tier grades, with **Grade C** contributing the highest expected loss (exposure-heavy segment).
- Built a Logistic Regression baseline model with **ROC-AUC ~0.70**.
- Tuned probability thresholds for business use (example: threshold 0.2 improved recall from ~7% to ~63% with precision ~32%).

## Dashboard Preview
![Dashboard](images/dashboard_full.png)

## What’s Inside
### Analytics & Modeling (Python)
- Data cleaning + feature engineering (e.g., FICO midpoint, income-to-loan ratio)
- Default modeling using Logistic Regression
- Risk scoring: `risk_score = default_probability * 100`

### BI Dashboard (Tableau Public)
1. **Default Rate by Grade**
2. **Expected Loss by Grade**
3. **Risk Score Distribution**

## How to Reproduce (Local)
> Note: the original dataset is large and is not committed to GitHub.

1. Create environment + install deps:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
