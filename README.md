# 💳 Credit Card Spending Analysis

---

> **"Anyone can build an accurate model. The real question is: do you actually need all that complexity?"**

That question is what this entire project is about.

---

## 🧠 The Idea

I was thinking about how financial institutions rely on increasingly complex ML models to predict customer behavior — more features, more layers, more everything. But complexity has a cost: slower inference, harder to explain to regulators, more expensive to maintain, and more things that can break in production.

So I asked myself: **what if simpler is smarter?**

I built a full spending prediction pipeline on 100,000 synthetic credit card customers, then deliberately tried to *break* the complex model — not by finding its weaknesses, but by proving it was doing way more work than necessary.

Spoiler: I was right. 👀

---

## 🎯 What This Project Does

1. **Generates** a realistic 100K customer dataset with behavioral, demographic, and product features
2. **Explores** what actually drives customer spending (the answer might surprise you)
3. **Trains** three models — Linear Regression, Gradient Boosting, and Random Forest
4. **Challenges** the winning model by asking: *can 5 features do what 13 features do?*
5. **Delivers** a strategic recommendation backed by data — not just "the model works"

---

## 💥 The Result That Got Me

| Model | R² Score | MAE | Features |
|-------|----------|-----|----------|
| Gradient Boosting (Full) | **0.9984** | $906 | 13 |
| Gradient Boosting (Simplified) | **0.9984** | $905 | **5** |

**62% fewer features. Literally identical performance.**

And here's the kicker — one single engineered feature (`spending_velocity = transaction_frequency × avg_transaction_amount`) accounts for **99.5% of the model's decision-making weight**. The other 12 features were essentially along for the ride.

---

## 📊 Deliverables

```
📁 credit-card-spending-analysis/
├── 📓 notebook.ipynb                        ← Full walkthrough, phase by phase
├── 🖼️  eda_analysis.png                     ← 4-panel EDA visualization
├── 🖼️  model_analysis.png                   ← Model comparison + feature importance
└── 📄 strategic_recommendation_report.txt  ← Executive-style write-up
```

---

## 🔍 Key Findings

**🏆 spending_velocity dominates everything**
Transaction frequency × average transaction amount is a single variable that captures almost all of what drives spending. It's elegant, interpretable, and powerful.

**📉 Complexity has a hidden cost**
The 13-feature model requires more data pipelines, more ETL jobs, more monitoring, harder compliance conversations, and slower inference — for zero gain in accuracy.

**✅ The simplified model wins on every business dimension**
- ⚡ ~40–60% faster training & inference
- 🧾 Explainable to Risk & Compliance teams
- 🔧 Simpler to deploy and monitor
- 💰 Lower operational cost

---

## 🛠️ Tech Stack

```python
pandas        # Data wrangling
numpy         # Numeric operations
matplotlib    # Visualizations
seaborn       # Statistical plots
scikit-learn  # ML models & metrics
```

**Models used:**
- `LinearRegression` — baseline
- `GradientBoostingRegressor` — primary model
- `RandomForestRegressor` — comparison

---

## 🚀 Run It Yourself

```bash
git clone https://github.com/yourusername/credit-card-spending-analysis
cd credit-card-spending-analysis
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook
```

Open the notebook and run all cells — everything generates automatically.

---

## 📐 Project Structure (Phase by Phase)

| Phase | What Happens |
|-------|-------------|
| **Phase 1** | Generate 100K synthetic customers with realistic distributions |
| **Phase 2** | EDA — correlations, segment analysis, 4 visualizations |
| **Phase 3** | Train 3 ML models, evaluate on R², MAE, RMSE |
| **Phase 4** | Feature importance analysis + build simplified challenger model |
| **Phase 5** | Model comparison visualizations |
| **Phase 6** | Write executive strategic recommendation report |

---

## 💡 Why I Built This

I'm genuinely fascinated by the gap between *data science* and *strategic analysis*. Building a model that achieves 99% accuracy is table stakes. The harder, more interesting question is whether that model should exist in its current form at all.

This project is my attempt to think like a strategist, not just a data scientist — to ask not just "does it work?" but "is this the right tool, and is it as simple as it could be?"

That mindset — ruthlessly questioning complexity — is what I want to bring to any analytics role I take on.

---

## 📬 Let's Connect

If this project resonates with you or you want to talk about model strategy, ML deployment trade-offs, or anything data — reach out!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://linkedin.com/in/yourprofile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/yourusername)

---
