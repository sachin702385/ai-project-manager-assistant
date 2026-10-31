# 📋 AI Project Manager Assistant

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.32%2B-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![SQLite](https://img.shields.io/badge/SQLite-local_persistence-003B57?logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![GitHub](https://img.shields.io/badge/GitHub-sachin702385-181717?logo=github&logoColor=white)](https://github.com/sachin702385)

Transform a rough project idea into a **complete, structured project-management package** — instantly, offline, and with no API key required.

Built with **Python + Streamlit**, this local web app takes simple inputs and generates **fourteen professional PM artifacts**, scores project risk, computes a **Green/Yellow/Red health indicator**, saves everything to a local **SQLite** database, and surfaces a **portfolio dashboard** with charts. Export any package to **Markdown or CSV**.

---

## ✨ Features

- **Input to Output:** Converts project vision into 14 structured PM deliverables.
- **Risk Scoring Model:** Each risk is scored on **Probability × Impact (1–25)** and mapped to a **Low / Medium / High / Critical** level.
- **Project Health Indicator:** Explainable **🟢 Green / 🟡 Yellow / 🔴 Red** status derived from risk scores and completion metrics.
- **Portfolio Dashboard:** High-level overview of project counts, open action items, high/critical risks, and visual health distribution charts.
- **Dual Generation Engine:** Runs completely offline in standard mock mode by default, or connects to external LLMs via environment API keys.
- **Multi-Provider Support:** Pluggable architecture ready for OpenAI, Anthropic, or Google Gemini models.
- **Local Persistence & Export:** Stores structured data locally in SQLite (`data/projects.db`) with one-click export to Markdown and CSV formats.

### Generated Deliverables
1. Project Charter
2. Scope Statement
3. Key Milestones
4. Work Breakdown Structure (WBS)
5. RAID Log
6. Scored Risk Register
7. Action Item Tracker
8. RACI Matrix
9. Stakeholder Communication Plan
10. Executive Status Summary
11. Executive One-Page Summary
12. Kickoff Meeting Agenda
13. Lessons Learned Retrospective
14. Resume Achievement Summary

---

## 🗂️ Project Structure

```text
ai-project-manager-assistant/
├── app.py                # Streamlit UI (Dashboard, Create, History)
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
├── data/
│   └── projects.db       # SQLite local database
├── outputs/              # Exported Markdown & CSV files
└── src/
    ├── ai_engine.py      # Artifact generation logic (Mock & LLM)
    ├── analytics.py      # Risk scoring & health diagnostics
    ├── providers.py      # LLM provider integrations
    ├── db.py             # SQLite persistence layer
    ├── exporters.py      # File export handlers
    ├── templates.py      # Artifact templates & schema definitions
    └── utils.py          # Helper utilities