# Student Question Answering from Course Materials

This project builds a retrieval-augmented generation (RAG) system for answering questions from course materials.

It compares three retrieval methods (TF-IDF, BM25, and dense retrieval) and several answer generators: Qwen3-8B, `google/mt5-base`, and `bigscience/mt0-small`.

## Authors

- Anja Čolić — [`anjaanjaa10`](https://github.com/anjaanjaa10), index: `1059/2024`
- Jelena Ivanović — [`jecikaaaa`](https://github.com/jecikaaaa), index: `1133/2025`
- Julijana Jevtić — [`jjulijana`](https://github.com/jjulijana), index: `1131/2025`

## Literature

The project is inspired by the RAG approach described in:

Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. “Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks” [arXiv:2005.11401](https://arxiv.org/html/2005.11401v4), 2021.

## Used materials and data

The system uses Serbian course material for the subject **Verifikacija softvera** (Software Verification). The material is extracted into page records and divided into text chunks for retrieval. The question set contains questions with corresponding answers and source references where available.

The data is organized as follows:

- `data/processed/pages/`: extracted course-material pages.
- `data/processed/pages.jsonl`: page records with source metadata and text.
- `data/processed/chunks.jsonl`: chunked course material used as retrieval documents.
- `data/processed/chunks_preprocessed.jsonl`: normalized chunks used by retrieval methods.
- `data/questions/`: questions and annotated answers used to develop and evaluate the system.
- `data/splits/`: training, validation, and test question splits.
- `data/retrieval/`: saved top-10 results for TF-IDF, BM25, and dense retrieval.
- `data/generation/`: generated answers and metadata for the mT5 and Qwen experiments.
- `data/evaluation/`: aggregate and per-question evaluation metrics.
- `artifacts/`: trained sequence-to-sequence checkpoints, RAG configurations, and generated predictions.



## Project layout


The notebooks are intended to be run in this order:

- `01_pdfExtraction.ipynb`: extracts source material into pages.
- `02_chunking.ipynb`: creates chunk records from extracted pages.
- `03_proccessingSplitting.ipynb`: preprocessing and train/validation/test split creation.
- `04_tf_idf_retrieval.ipynb`: TF-IDF indexing, retrieval, and evaluation.
- `05_bm25_retrieval.ipynb`: BM25 indexing, retrieval, and evaluation.
- `06_dense_retrieval.ipynb`: dense indexing, retrieval, and evaluation.
- `07a_mt5_gold_rag.ipynb`: fine-tunes and evaluates a `google/mt5-base` RAG generator.
- `07b_mt0_small_gold_rag.ipynb`: fine-tunes and evaluates a `bigscience/mt0-small` RAG generator.
- `08_qwen_rag.ipynb`: generates answers with `Qwen/Qwen3-8B` using retrieved context.
- `09_evaluationQwen.ipynb`: evaluates Qwen validation answers.
- `09_evaluationQwen_test.ipynb`: evaluates Qwen test answers, including semantic metrics.
- `10_evaluation_mt5_gold.ipynb`: evaluates the mT5 generated answers.
- `10_mt0_small_evaluation.ipynb`: evaluates the mT0-small generated answers.
- `11_final_comparison.ipynb`: combines final test-set metrics.

The retrieval notebooks save reusable indexes and top-10 results under `data/retrieval/`. The generation notebooks use those results and save predictions under `data/generation/` or `artifacts/`. Evaluation notebooks write CSV and JSON metadata under `data/evaluation/`.

The dense retriever uses `intfloat/multilingual-e5-base`. The generator notebooks download their base models from Hugging Face, so model downloads and sufficient disk space are required.

## Setup with a virtual environment

From the project root on Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m ipykernel install --user --name <name> --display-name "Python (<name>)"
```

Select the created `Python (<name>)` kernel in VS Code before running a notebook. The dense retrieval and evaluation notebooks require the `sentence-transformers` and `faiss-cpu` packages. The Qwen notebook is intended for a CUDA-capable environment and uses `bitsandbytes` for quantized loading.

`07a_mt5_gold_rag.ipynb` and `08_qwen_rag.ipynb` contain Google Colab drive integration. When running them outside Colab, remove or replace the `google.colab` drive-mount cells and update the project paths to local paths.

To leave the environment:

```bash
deactivate
```

## Running the pipeline

When starting from raw course material, run notebooks `01` through `06` in order. Then run the generator notebook for the model you want to evaluate, followed by its evaluation notebook:

1. `01_pdfExtraction.ipynb` creates the extracted pages.
2. `02_chunking.ipynb` creates `data/processed/chunks.jsonl`.
3. `03_proccessingSplitting.ipynb` creates the preprocessed chunks and dataset splits.
4. `04_tf_idf_retrieval.ipynb`, `05_bm25_retrieval.ipynb`, and `06_dense_retrieval.ipynb` create retrieval indexes and results.
5. Run `07a` or `07b` for sequence-to-sequence generation, or `08` for Qwen generation.
6. Run `09_evaluationQwen.ipynb`, `09_evaluationQwen_test.ipynb`, or `10_evaluation_mt5_gold.ipynb` for the corresponding evaluation.

The retrieval and evaluation notebooks can also be run against the existing files under `data/` without repeating extraction and preprocessing.

## Reproducibility

The split notebook uses `random_state=42`.
