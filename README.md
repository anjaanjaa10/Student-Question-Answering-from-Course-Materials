# Student Question Answering from Course Materials

This project builds a retrieval-augmented generation (RAG) system for answering questions from course materials. 

We will compare three retrieval methods (TF-IDF, BM25, and dense retrieval) and two answer generators: the Qwen3-8B large language model and a google/mt5-base sequence-to-sequence model. 

## Authors

- Anja Čolić — [`anjaanjaa10`](https://github.com/anjaanjaa10), index: `1059/2024`
- Jelena Ivanović — [`jecikaaaa`](https://github.com/jecikaaaa), index: `1133/2025`
- Julijana Jevtić — [`jjulijana`](https://github.com/jjulijana), index: `1131/2025`

## Literature

The project is inspired by the RAG approach described in:

Patrick Lewis, Ethan Perez, Aleksandra Piktus, Fabio Petroni, Vladimir Karpukhin, Naman Goyal, Heinrich Küttler, Mike Lewis, Wen-tau Yih, Tim Rocktäschel, Sebastian Riedel, and Douwe Kiela. “Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks” [arXiv:2005.11401](https://arxiv.org/html/2005.11401v4), 2021.

## Used materials and data

The system uses Serbian course material for the subject **Verifikacija softvera** (Software Verification). The material is extracted into 188 page records and divided into 344 text chunks for retrieval. The question set contains 143 questions with corresponding answers and source references where available.

The data is organized as follows:

- `data/processed/pages/`: extracted course-material pages.
- `data/processed/pages.jsonl`: page records with source metadata and text.
- `data/processed/chunks.jsonl`: chunked course material used as retrieval documents.
- `data/processed/chunks_preprocessed.jsonl`: normalized chunks used by retrieval methods.
- `data/questions/`: questions and annotated answers used to develop and evaluate the system.
- `data/splits/`: training, validation, and test question splits.



## Project layout


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