# AI Idea Prioritizer

Rank and visualize your product ideas with **ICE** and **RICE** scoring.  
Built using [Streamlit](https://streamlit.io/), this app helps product managers quickly compare and prioritize ideas based on **Impact**, **Confidence**, **Effort**, and **Reach**.

---

## Features

- Paste multiple ideas (one per line) and instantly compute ICE/RICE scores  
- Adjustable sliders to tweak weighting for each metric  
- Keyword-based heuristics for effort and impact estimation  
- Download prioritized results as a CSV file  
- Clean, interactive web UI built with Streamlit

---

## How It Works

Each idea is scored using customizable formulas:

- **Effort (1–10):** Lower for short, simple ideas with “easy” keywords (e.g., *UI, prompt, template*); higher for “API/integration/platform* ideas.
- **Impact (1–10):** Higher when containing key terms like *conversion, churn, retention, revenue*.
- **Confidence (1–10):** Increases when multiple ideas share overlapping keywords (proxy for validation).
- **Reach (1–10):** Based on broad terms implying wide exposure (*onboarding, billing, notifications*).

Scores are combined using:
- **ICE Score** = `(Impact × Confidence) ÷ Effort`
- **RICE Score** = `(Reach × Impact × Confidence) ÷ Effort`

All weights are adjustable via sliders.

---

## Running Locally

1. **Clone this repository**
   ```bash
   git clone https://github.com/<your-username>/ai-idea-prioritizer.git
   cd ai-idea-prioritizer

2. Create and activate a virtual environment - 
    python3 -m venv .venv
    source .venv/bin/activate  # macOS/Linux
    .venv\Scripts\activate     # Windows

3. Install dependencies - 
    pip install -r requirements.txt

4. Run the app - 
    streamlit run app.py

5. Visit - http://localhost:8501 to use the app.
