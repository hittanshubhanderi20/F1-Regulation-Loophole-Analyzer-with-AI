# 🏁 F1 Regulation Loophole Analyzer with AI
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![LLM: Ollama](https://img.shields.io/badge/LLM-Gemma3%20%7C%20DeepSeek-brightgreen.svg)
![LangChain](https://img.shields.io/badge/LangChain-enabled-purple.svg)
![NLP-Powered](https://img.shields.io/badge/NLP-custom--pipeline-informational.svg)


This project is an AI-powered analyzer designed to uncover **realistic performance loopholes in FIA Formula 1 regulations**. Using local LLMs and NLP techniques, it identifies, scores, and explains potential grey areas in F1 rules across seasons — helping teams or strategists prepare for the 2026 regulatory landscape.

---

## 🚀 What It Does

✅ Parses FIA regulations (technical, sporting, and financial)  
✅ Tracks yearly changes (2021–2025) to highlight regulatory shifts  
✅ Uses LLMs (`gemma3`, `deepseek`) to simulate loophole strategies  
✅ Applies filters for team budget, risk profile, and historic patterns  
✅ Generates ranked loophole forecasts with Deep AI explanations  
✅ Supports automation, checkpointing, and offline execution

---

## 📁 Repository Structure

```

F1-Loophole-Analyzer/
├── f1\_loophole.ipynb                       # 🧪 Full Jupyter pipeline
├── loophole\_engine.py                      # 🧠 Modular version for CLI/batch use
├── tavily\_cache.json                       # 🌐 Cached FIA search content
├── checkpoint\_loopholes.json               # ♻️ Tracks execution progress
├── fia\_loophole\_ranking\_safe\_top.csv    # 📊 Sample output
├── requirements.txt                         # 📦 Project dependencies
└── README.md                                # 📘 Project overview

```

---

## 🧠 Technologies Used

| Component        | Technology                                |
|------------------|--------------------------------------------|
| Language Models  | Ollama (`gemma3:latest`, `deepseek-r1:14b`) |
| NLP & Parsing    | LangChain, PyMuPDF, spaCy, regex           |
| Search Layer     | Tavily Search API                          |
| Execution Logic  | Caching, checkpointing, retry handling     |
| Output & Export  | Pandas, CSV                                |

---

## 📊 Sample Output

| Article    | Loophole Concept                            | Usefulness | Detection Risk | FIA Response     |
|------------|----------------------------------------------|------------|----------------|------------------|
| Article 3.15 | Micro-actuators for adaptive aero control  | High       | Medium         | Likely TD update |
| Article 5.2  | ERS-based tire heating loophole            | Medium     | Low            | TD clarification |
| Article 10.1 | Flexible endplates under side loading      | High       | High           | Scrutiny likely  |

Output is exported as a ranked `.csv` file:
```

fia\_loophole\_ranking\_safe\_top.csv

````

---

## 🛠️ How to Run

### 🔧 1. Install dependencies
```bash
pip install -r requirements.txt
````

### 🔑 2. Set your Tavily API key

```bash
export TAVILY_API_KEY="your-api-key-here"
```

### ▶️ 3. Run Jupyter notebook

```bash
jupyter notebook f1_loophole_formatted.ipynb
```

Or use the Python module:

```bash
python loophole_engine.py
```

---

## 📌 Key Highlights

* Uses **local LLMs via Ollama** for full offline capability
* Differentiates between “safe” vs “risky” loopholes
* Adapts output by **team tier**: top, mid, or low budget
* Integrates **historic loophole detection** (e.g., DAS, F-duct)
* Supports long, batched runs with **safe restarts**
* Generates top loophole summaries and exports `.csv` results

---

## 📜 License

MIT License — free to use, modify, or extend.

---

## 🙋‍♂️ Contact

Built with ❤️ by Hittanshu Bhanderi
Connect via [LinkedIn](https://www.linkedin.com/in/hittanshubhanderi/)
