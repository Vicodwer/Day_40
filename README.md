# Week 07 · Friday — ShopSense Sentiment Analysis

**PG Diploma · AI-ML & Agentic AI Engineering · IIT Gandhinagar**

---

## What this notebook does

Covers all seven sub-steps of the Friday Synthesis Day assignment:

| Sub-step | Topic | Difficulty |
|---|---|---|
| 1 | Class distribution — why accuracy is misleading | 🟢 Easy |
| 2 | Classifier evaluation with appropriate metrics + stakeholder summary | 🟢 Easy |
| 3 | Quantitative constraint evaluation (new categories / code-mix / latency) | 🟡 Medium |
| 4 | Cost model + daily projected misclassification cost + recommendation | 🟡 Medium |
| 5 | One-page technical brief + production monitoring specification | 🟡 Medium |
| 6 | Broken pipeline reproduction, root-cause diagnosis, and fix | 🔴 Hard |
| 7 | Business cost of the broken pipeline + vulnerability audit | 🔴 Hard |

---

## How to run

### Prerequisites

```
Python 3.10+
```

Install dependencies (all standard):

```bash
pip install pandas numpy scikit-learn matplotlib seaborn notebook
```

### Dataset

Place `product_reviews.csv` **in the same folder** as this notebook  
(`week-07/friday/product_reviews.csv`).

The notebook auto-detects common column names from the Kaggle Brazilian  
e-commerce dataset as well as the LMS-provided checkpoint variant.  
Required columns (any of these names are accepted):

| Field | Accepted column names |
|---|---|
| Star rating (1–5) | `review_score`, `score`, `rating`, `star_rating` |
| Review text | `review_comment_message`, `review_text`, `comment`, `text`, `review` |

### Run

```bash
cd week-07/friday
jupyter notebook sentiment_analysis.ipynb
```

Then **Kernel → Restart & Run All**.

The notebook runs end-to-end without manual intervention.  
All file paths are relative — no hardcoded local paths.

---

## Output files generated

| File | Contents |
|---|---|
| `class_distribution.png` | Bar + pie chart of sentiment class shares |
| `confusion_matrix_*.png` | Per-model confusion matrices |
| `constraint_comparison.png` | Constraint robustness chart (Sub-step 3) |
| `daily_cost_comparison.png` | Projected daily cost per model (Sub-step 4) |
| `technical_brief.txt` | Exportable one-page brief (Sub-step 5) |
| `before_after_pipeline.png` | Broken vs fixed pipeline metrics (Sub-step 6) |
| `cost_broken_vs_recommended.png` | Cost comparison chart (Sub-step 7) |

---

## Repo structure

```
week-07/
└── friday/
    ├── sentiment_analysis.ipynb   ← main notebook
    ├── product_reviews.csv        ← dataset (not committed — add to .gitignore)
    ├── README.md                  ← this file
    └── prompts.md                 ← AI usage log with critique
```

---

## Python version & key packages

| Package | Version tested |
|---|---|
| Python | 3.10 |
| pandas | ≥ 1.5 |
| numpy | ≥ 1.23 |
| scikit-learn | ≥ 1.2 |
| matplotlib | ≥ 3.6 |
| seaborn | ≥ 0.12 |
| notebook / jupyterlab | any recent |

---

## .gitignore additions recommended

```
product_reviews.csv
*.csv
__pycache__/
.ipynb_checkpoints/
*.env
```
