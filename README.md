<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=250&section=header&text=IntelliQuery&fontSize=90&fontAlignY=38&desc=AI-Powered%20SQL%20Assistant&descAlignY=60&descAlign=50" alt="Header Banner">

<h1>🤖 IntelliQuery</h1>

<p>
  <b>Transforming natural language into complex SQL using the cognitive power of Google Gemini.</b>
</p>

<p>
  <img src="https://img.shields.io/badge/Python-3.7-blue?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.7">
  <img src="https://img.shields.io/badge/Framework-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
  <img src="https://img.shields.io/badge/Database-SQLite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/AI-Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini AI">
</p>

</div>

---

## 🌌 The Vision

**IntelliQuery** is a robust, Streamlit-based cognitive engine designed for Business Analysts and Data Professionals. Upload any structured dataset and query it effortlessly using conversational English. Under the hood, IntelliQuery leverages a highly-resilient REST architecture connected to the **Google Gemini API** to automatically translate your questions into highly accurate SQL queries, execute them, and return human-readable insights.

> **Engineering Note:** This edition is strictly engineered for **Python 3.7 compatibility**. It replaces heavy, modern SDK dependencies with a lightweight, resilient REST architecture utilizing `requests`, complete with automatic retry logic for handling temporary API rate limits or network turbulence.

---

## ⚡ Cognitive Features Matrix

<table align="center">
  <tr>
    <td align="center" width="50%">
      <img src="https://img.icons8.com/nolan/64/database.png" alt="Multi-format"/>
      <h3>Universal Data Ingestion</h3>
      <p>Upload `.csv`, `.xlsx`, `.json`, `.xml`, and raw `.sql` dumps. The engine dynamically flattens and parses the schema.</p>
    </td>
    <td align="center" width="50%">
      <img src="https://img.icons8.com/nolan/64/artificial-intelligence.png" alt="AI Query"/>
      <h3>Zero-Code AI Queries</h3>
      <p>Ask questions in plain English. The AI dynamically translates human intent into flawless SQLite `SELECT` operations.</p>
    </td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://img.icons8.com/nolan/64/bar-chart.png" alt="Insights"/>
      <h3>Actionable Insights</h3>
      <p>Raw SQL rows are confusing. IntelliQuery feeds the data back into the LLM to summarize the numbers into natural language insights.</p>
    </td>
    <td align="center">
      <img src="https://img.icons8.com/nolan/64/shield.png" alt="Resilient"/>
      <h3>Resilient Architecture</h3>
      <p>Built-in geometric backoff and auto-retry mechanisms gracefully handle `429` rate limits and Google API downtime.</p>
    </td>
  </tr>
</table>

---

## 🧠 System Architecture

<div align="center">

```mermaid
graph TD
    classDef user fill:#2d3436,stroke:#74b9ff,stroke-width:2px,color:#fff;
    classDef ai fill:#6c5ce7,stroke:#a29bfe,stroke-width:2px,color:#fff;
    classDef db fill:#00b894,stroke:#55efc4,stroke-width:2px,color:#fff;

    A["📄 User Uploads File <br> <i>CSV, JSON, Excel</i>"]:::user --> B("⚙️ Pandas Engine <br> <i>Normalizes Schema</i>"):::user
    B --> C[("🗄️ In-Memory SQLite <br> <i>Data Stored Locally</i>")]:::db
    
    D["🗣️ User Asks Question <br> <i>'Who sold the most?'</i>"]:::user --> E{"🧠 Gemini Flash API <br> <i>Translates to SQL</i>"}:::ai
    E -->|Generated Query| C
    C -->|Query Results| E
    E --> F["📊 Human-Readable Insight <br> <i>Streamlit UI</i>"]:::user
```

</div>

---

## 🚀 Ignition Sequence (Setup Guide)

<details>
<summary><b>Click here to view installation & deployment instructions</b></summary>
<br>

### Prerequisites
- **Python 3.7** installed on your system.
- A **Google Gemini API Key** from [Google AI Studio](https://aistudio.google.com/).

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TarakShetti/IntelliQuery-Python3.7.git
   cd IntelliQuery-Python3.7
   ```

2. **Initialize Environment:**
   ```bash
   python -m venv venv
   
   # Windows:
   .\venv\Scripts\activate
   
   # macOS/Linux:
   source venv/bin/activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

### Execution

1. **Inject API Key:**
   ```bash
   # Windows (PowerShell)
   $env:GEMINI_API_KEY="your-api-key-here"
   
   # macOS/Linux
   export GEMINI_API_KEY="your-api-key-here"
   ```

2. **Launch Neural UI:**
   ```bash
   streamlit run app.py
   ```
   *Navigate to `http://localhost:8501` to begin.*

</details>

---

<div align="center">
  <p><i>Democratizing Data Analytics. No SQL required.</i></p>
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=100&section=footer" width="100%" alt="Footer Banner">
</div>
