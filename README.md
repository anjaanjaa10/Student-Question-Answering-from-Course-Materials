# Student Question Answering from Course Materials

This project builds a retrieval-augmented generation (RAG) system for answering questions from course materials. 

We will compare three retrieval methods (TF-IDF, BM25, and dense retrieval) and two answer generators: the Qwen3-8B large language model and a google/mt5-base sequence-to-sequence model. 

## Project layout

`data/questions/`: contains questions and answers for testing.

`data/processed/`: contains proccessed pages of materials and chunks.

`data/splits/`: contains train/test/validation split.

Notebooks:
- `01_pdfExtraction.ipynb`: extracts source material into pages.
- `02_chunking.ipynb`: creates chunk records from extracted pages.
- `03_proccessingSplitting.ipynb`: preprocessing and train/validation/test split creation.
- `04_tf_idf_retrieval.ipynb`: TF-IDF indexing, retrieval, and evaluation.
- `05_bm25_retrieval.ipynb`: BM25 indexing, retrieval, and evaluation.
- `06_dense_retrieval.ipynb`: dense indexing, retrieval, and evaluation.

Planned generation components: llm and a sequence-to-sequence model.

Planned evaluation.



## Setup with a virtual environment

From the project root on Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name <name> --display-name "Python (<name>)"
```

To leave the environment:

```bash
deactivate
```

## Running the pipeline

Run the notebooks in this order when starting from raw course material:

1. Run `01_pdfExtraction.ipynb` to create the extracted pages.
2. Run `02_chunking.ipynb` to create `data/processed/chunks.jsonl`.
3. Run the preprocessing and split cells in `03_proccessingSplitting.ipynb` to create `chunks_preprocessed.jsonl` and the dataset splits.

## Reproducibility

The split notebook uses `random_state=42`.