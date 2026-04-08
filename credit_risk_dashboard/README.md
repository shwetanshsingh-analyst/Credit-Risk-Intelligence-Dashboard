# Credit Risk Intelligence Platform
### AI-Powered Loan Default Prediction System — Capstone Project

![Status](https://img.shields.io/badge/Status-Production--Ready-brightgreen)
![Models](https://img.shields.io/badge/Models-5%20Active-blue)
![Best%20AUC](https://img.shields.io/badge/Best%20ROC--AUC-0.928-orange)

A fully interactive, browser-based dashboard for credit risk assessment built with vanilla HTML, CSS, and JavaScript — no server required.

---

## Live Dashboard Features

| Page | Description |
|------|-------------|
| **Dashboard** | Portfolio KPIs, risk grade distribution, default rate by loan purpose and employment type |
| **Loan Predictor** | Real-time risk scoring with gauge chart, grade assignment (AAA–CCC), and risk factor breakdown |
| **EDA & Analytics** | Feature distributions, correlation matrix heatmap, segment-level default analysis |
| **Time Series** | Historical default rate trends + Prophet 6-month forecast with confidence intervals |
| **Model Performance** | Side-by-side ROC-AUC / F1 / Precision / Recall comparison across all 5 models |
| **NLP Analysis** | Application text sentiment analysis — positive/negative keyword extraction and risk scoring |

---

## Models Implemented

| Model | Type | ROC-AUC | F1-Score |
|-------|------|---------|---------|
| Stacking Ensemble | Meta-Learning | **0.928** | 0.881 |
| XGBoost | Gradient Boosting | 0.913 | 0.862 |
| LSTM + Attention | Deep Learning | 0.891 | 0.843 |
| Random Forest | Ensemble ML | 0.874 | 0.829 |
| NLP Classifier | TF-IDF + TextBlob | 0.831 | 0.788 |

---

## Hosting on GitHub Pages

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it `credit-risk-dashboard` (or any name you prefer)
4. Set visibility to **Public**
5. Click **Create repository**

### Step 2 — Upload the Files

**Option A — GitHub Web Interface (Easiest)**
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag and drop `index.html` and `README.md`
4. Click **Commit changes**

**Option B — Git Command Line**
```bash
git clone https://github.com/YOUR_USERNAME/credit-risk-dashboard.git
cd credit-risk-dashboard
cp /path/to/index.html .
cp /path/to/README.md .
git add .
git commit -m "Add credit risk intelligence platform"
git push origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top navigation)
3. Scroll down to **Pages** in the left sidebar
4. Under **Source**, select **Deploy from a branch**
5. Choose branch: **main** and folder: **/ (root)**
6. Click **Save**

### Step 4 — Access Your Live Site

After 1–2 minutes, your dashboard will be live at:
```
https://YOUR_USERNAME.github.io/credit-risk-dashboard/
```

---

## Local Preview

No installation needed. Simply open `index.html` in any modern browser:
```bash
# macOS
open index.html

# Windows
start index.html

# Linux
xdg-open index.html
```

Or use a local server:
```bash
python -m http.server 8080
# Then open: http://localhost:8080
```

---

## Tech Stack (Frontend)

- **HTML5 / CSS3 / Vanilla JavaScript** — Zero dependencies except Chart.js
- **Chart.js 4.4** — All interactive charts (loaded from CDN)
- **IBM Plex Sans + IBM Plex Mono** — Professional financial typography (Google Fonts)
- **Plotless Gauge** — Custom Canvas 2D API drawing
- **Correlation Matrix** — Custom Canvas 2D heatmap renderer

---

## Python Backend (Full Stack)

The full Python ML pipeline is in the `src/` and `dashboard/` directories:

```bash
pip install -r requirements.txt
streamlit run dashboard/app.py
```

Requires: TensorFlow, XGBoost, Prophet, Streamlit, TextBlob, scikit-learn

---

## Author

Capstone Project — Finance and Artificial Intelligence  
Advanced Machine Learning | Deep Learning | NLP | Time Series
