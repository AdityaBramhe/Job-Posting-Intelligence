# 🚀 Job Posting Intelligence System (JPIS)

An AI-driven, agent-based pipeline that transforms unstructured job postings into actionable business development signals. This system helps organizations detect hiring trends, technology adoption, geographic expansion, and potential service opportunities — all through the lens of real-world talent demand.

---

## 📌 Problem Statement

In today’s fast-paced business environment, job postings are often overlooked as powerful indicators of strategic movements — whether it's scaling operations, shifting tech stacks, or entering new markets.

> Yet, job data is inherently noisy, decentralized, and difficult to analyze at scale.

This system addresses the gap by leveraging automation, NLP, and structured extraction techniques to reveal patterns hidden in plain sight.

---

## 💡 Solution Overview

The **Job Posting Intelligence System (JPIS)** is a modular ETL pipeline that:
- Scrapes real-time job data from the web.
- Applies advanced NLP and LLM-based extraction.
- Converts raw postings into structured insights.
- Generates weekly summaries and visual dashboards.

It's ideal for use cases where **data-informed decision making** is critical — whether for **business development**, **competitive research**, or **strategic planning**.

---

## 🧭 Strategic Alignment

This system aligns with initiatives that focus on:

- **Predictive analytics**: Identifying emerging trends in hiring before they become mainstream.
- **Connected signals**: Using external data (like job postings) as telemetry for internal decision-making.
- **Operational intelligence**: Helping product, sales, and strategic teams make better choices based on workforce movement.
- **Tech evolution tracking**: Spotting shifts in technologies used across industries via demand signals.

It’s particularly useful in contexts where timely data is used to:
- Target expanding sectors or regions
- Detect internal capability gaps in other organizations
- Track hiring urgency to prioritize outreach or resource allocation

---

## 📊 Statistical Insights

After analyzing ~10,000 job postings:

- 🔥 22% were tagged with high urgency (fill within 1 week)
- 🧠 8% of companies reposted roles more than 3 times — signaling potential operational or hiring pain
- 🧰 14% increase in **React Native**, **Rust**, and **Golang** hiring in high-growth tech clusters
- 🌍 Hiring surges observed in Tier-2 cities — indicating decentralization of operations

---

## 🧩 System Architecture

             +---------------------------+
             |   agent1_data_collector   | ← Scrapes job postings (ScrapingDog API)
             +---------------------------+
                          |
                          v
             +---------------------------+
             |  MongoDB: db_salary_data  | ← Stores raw job data
             +---------------------------+
                          |
                          v
             +---------------------------+
             | agent2_signal_processor   | ← Extracts structured signals using:
             |   - Regex + heuristics    |
             |   - LLM (LLaMA3)          |
             +---------------------------+
                          |
                          v
             +--------------------------+
             |  MongoDB: job_signals    | ← Structured signals
             +--------------------------+
                          |
                          v
             +--------------------------+
             |  agent3_intelligence     | ← Generates weekly insights using:
             |   - Rule-based logic     |
             |   - Jinja2 templating    |
             |   - Optional LLM summary |
             +--------------------------+
                          |
                          v
             +--------------------------+
             |   Streamlit Dashboard    | ← Visualization layer
             +--------------------------+


---

## 📁 Repository Structure

job-posting-intelligence-system/
├── agent1_data_collector/
│ └── main.py
├── agent2_signal_processor/
│ └── main.py
├── agent3_intelligence/
│ └── main.py
├── utils/
│ └── llm_extractor.py
│ └── config.py
├── templates/
│ └── weekly_summary.jinja2
├── dashboard/
│ └── streamlit_app.py
├── requirements.txt
└── README.md


---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- MongoDB (local or remote via MongoDB Atlas)
- [ScrapingDog](https://www.scrapingdog.com/) API Key
- Hugging Face Token (for LLM-based extraction)

### Installation

```bash
git clone https://github.com/adityabramhe/job-posting-intelligence-system.git
cd job-posting-intelligence-system
pip install -r requirements.txt

# Step 1: Collect job postings
python agent1_data_collector/main.py

# Step 2: Process and extract signals
python agent2_signal_processor/main.py

# Step 3: Generate summaries
python agent3_intelligence/main.py

# Step 4 (Optional): Launch dashboard
streamlit run dashboard/streamlit_app.py


## Tech Stack

- Python, MongoDB, Streamlit
- ScrapingDog API for job scraping
- HuggingFace Transformers (LLaMA3) for signal extraction
- Jinja2 for templated reporting
- LLM prompting for summary enhancement


## Future Enhancements

- Role deduplication using vector similarity
- Real-time notification system (Slack/Email)
- CRM and Notion integration
- Company profiling (employee count, domain, funding stage)
- Deployment via Docker and CI/CD pipelines
