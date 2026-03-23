# LLM Evaluation & Benchmarking Dashboard

## Problem Statement
Choosing the right LLM for a production application requires systematic evaluation
across accuracy, latency, and reliability dimensions. This project builds an automated
evaluation framework comparing two LLaMA models across 5 task categories.

## Models Compared
| Model | Size | Provider |
|---|---|---|
| LLaMA 3.1 8B | 8B params | Groq API |
| LLaMA 3.3 70B | 70B params | Groq API |

## Evaluation Categories
- Factual Knowledge
- Reasoning
- Summarization
- Coding
- Hallucination Check

## Results
| Model | Accuracy | Avg Latency |
|---|---|---|
| LLaMA 3.1 8B | 53.3% | 0.30s |
| LLaMA 3.3 70B | 66.7% | 0.52s |

## Key Findings
- LLaMA 3.3 70B is 13.4% more accurate but 73% slower
- Both models excel at Coding and Factual Knowledge (100%)
- Hallucination detection is the weakest category for both models
- Recommendation: Use 8B for latency-sensitive apps, 70B for accuracy-critical tasks

## Tech Stack
Python | LangChain | Groq API | Pandas | Matplotlib

## How to Run
```bash
# Install dependencies
pip install -r requirements.txt

# Add your Groq API key to .env
GROQ_API_KEY=your_key_here

# Launch Jupyter
jupyter notebook notebooks/llm_evaluation.ipynb
```

## Project Structure
```
llm-evaluation-dashboard/
├── notebooks/
│   └── llm_evaluation.ipynb
├── results/
│   ├── evaluation_charts.png
│   └── evaluation_results.json
├── .gitignore
├── requirements.txt
└── README.md
```
