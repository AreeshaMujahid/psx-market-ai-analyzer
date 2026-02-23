# 📊 PSX Market AI Analyzer

An AI-powered market intelligence tool that scrapes live stock data from
the Pakistan Stock Exchange (PSX), processes it using Pandas, and
generates structured insights using OpenAI models.

This project demonstrates real-world AI engineering practices including
dynamic web scraping, data normalization, structured analytics, and safe
LLM integration.

------------------------------------------------------------------------

## 🚀 Features

-   🔍 Live data scraping using Playwright
-   📈 Automatic extraction of all PSX stock-sector tables
-   🧹 Intelligent header normalization and schema cleaning
-   📊 Market analytics powered by Pandas
-   🤖 LLM-based explanation engine using OpenAI
-   🖥 Optional Streamlit interface for interactive analysis
-   🔐 Secure API key management using `.env`

------------------------------------------------------------------------

## 🛠 Tech Stack

-   Python 3.12
-   Playwright (Dynamic Web Scraping)
-   Pandas (Data Processing)
-   OpenAI API (LLM Explanation Layer)
-   Streamlit (UI Layer)
-   python-dotenv (Secure configuration)
-   lxml (HTML table parsing)

------------------------------------------------------------------------

## 🏗 Project Architecture

User Query\
⬇\
Playwright Scraper (Live PSX Data)\
⬇\
Data Cleaning & Normalization (Pandas)\
⬇\
Computed Results (No hallucination risk)\
⬇\
OpenAI LLM (Explanation Only)\
⬇\
Structured Market Insights

⚠ Important:\
The LLM does NOT generate stock data.\
It only explains computed results from Python to prevent hallucination.

------------------------------------------------------------------------

## 📂 Project Structure

    psx-market-ai-analyzer/
    │
    ├── app.py              # Main entry (CLI or Streamlit)
    ├── scraper.py          # Playwright scraping logic
    ├── analyzer.py         # Data cleaning + analytics logic
    ├── llm_engine.py       # OpenAI interaction layer
    ├── requirements.txt
    ├── .gitignore
    ├── README.md
    │
    ├── assets/             # Screenshots
    └── psx_output/         # Generated data files

------------------------------------------------------------------------

## ▶️ Installation

### 1️⃣ Clone Repository

    git clone https://github.com/YOUR_USERNAME/psx-market-ai-analyzer.git
    cd psx-market-ai-analyzer

### 2️⃣ Install Dependencies

Using pip:

    pip install -r requirements.txt
    playwright install chromium

Using uv:

    uv pip install -r requirements.txt
    uv run playwright install chromium

### 3️⃣ Set OpenAI API Key

Windows:

    setx OPENAI_API_KEY "your_api_key_here"

Mac/Linux:

    export OPENAI_API_KEY="your_api_key_here"

------------------------------------------------------------------------

## ▶️ Running the Application

CLI Mode:

    python app.py

Streamlit UI Mode:

    streamlit run app.py

------------------------------------------------------------------------

## 📊 Example Queries

-   Market overview
-   Top gainers
-   Top losers
-   Highest volume stocks
-   Snapshot of a specific symbol (e.g., HBL)
-   Volume comparison analysis

------------------------------------------------------------------------

## 🧠 Key Engineering Concepts Demonstrated

-   Dynamic website scraping with headless browsers
-   Handling multi-level HTML headers
-   Schema normalization for inconsistent tables
-   Safe LLM prompt design (anti-hallucination guardrails)
-   Separation of data computation and explanation layers
-   Secure API key management

------------------------------------------------------------------------

## 🔐 Security Considerations

-   `.env` is ignored via `.gitignore`
-   API keys are never committed
-   LLM restricted to computed results only
-   No financial advice provided

------------------------------------------------------------------------

## 📌 Future Improvements

-   Historical data comparison (RAG integration)
-   Sector-level trend visualization
-   PostgreSQL storage layer
-   Deployment to Streamlit Cloud / Render
-   Automated daily market summary bot

------------------------------------------------------------------------

## 📜 Disclaimer

This project is for educational and research purposes only.\
It does not provide financial advice or investment recommendations.
