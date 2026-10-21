# AIDAMS Lab 4: An LLM Extraction You Can Trust

Course: Research and Emerging Topics in Data Science (IDSI 51003), AIDAMS.

Treats an LLM as a measurement instrument: extract steel-company emissions data from report text, score it against gold labels, put intervals on accuracy, test self-consistency (majority vote) and a mini-RAG retrieval step.

## Group

Alix Bauret, Camille Metz, Lara Normand, Amine Benbachir Hassani, Tiphaine De Saint Aignan

## Contents

| File | What it is |
|---|---|
| `lab4.ipynb` | Completed notebook, all cells run (outputs visible) |
| `data/excerpts.json` | 20 fictional report excerpts |
| `data/gold_labels.json` | Hand-made gold labels |
| `data/recorded_responses.json` | Pre-recorded LLM answers (1 greedy + 5 sampled per excerpt) |
| `data/aurelia_report_chunks.json` | 16 report chunks and 6 queries for the retrieval part |
| `requirements.txt` | Python dependencies |

## How to run

No API key is needed: the LLM answers are recorded (`BACKEND = "recorded"`).

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter lab lab4.ipynb           # then Kernel -> Restart & Run All
```

Run the notebook from the repository root so that the relative `data/` path resolves.

The optional boxes (A2 live LLM run, D2 dense embeddings) were skipped.
