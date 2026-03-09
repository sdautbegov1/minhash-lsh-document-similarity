# MinHash LSH Document Similarity

This repository contains a project on the application of MinHash and Locality-Sensitive Hashing (LSH) for efficient document similarity search and near-duplicate detection.

The project focuses on approximating Jaccard similarity using MinHash signatures and reducing the cost of similarity search through LSH-based candidate generation. The implementation is evaluated against a brute-force approach and shows substantial speed improvements for larger document collections.

## Repository Structure

```text
minhash-lsh-document-similarity/
├── notebook/
│   └── final_minhash_lsh.ipynb
├── docs/
│   └── final_report.pdf
└── README.md
````

## Project Overview

The goal of this project is to examine how MinHash and LSH can be used to efficiently identify similar documents without comparing every document pair directly.

The project covers:

* document representation using shingles
* approximation of Jaccard similarity with MinHash signatures
* candidate generation using Locality-Sensitive Hashing
* similarity search over large document collections
* comparison of LSH-based retrieval and brute-force search

## Methods Used

The main methods and concepts used in this project are:

* shingling
* Jaccard similarity
* MinHash
* Locality-Sensitive Hashing
* candidate-based similarity search
* performance evaluation using runtime and retrieval metrics

## Systems and Data

The experiments are performed on a dataset of English Wikipedia articles loaded in streaming mode. Each record contains a document identifier, title, and full text. The final evaluation uses this dataset because it provides longer and more content-rich documents suitable for similarity analysis.

## Contents

### `notebook/`

This folder contains the Jupyter notebook with the implementation, preprocessing pipeline, MinHash signature generation, LSH indexing, querying procedure, experiments, plots, and result analysis.

### `docs/`

This folder contains the accompanying project report in PDF format.

## Main Topics Covered

The project includes analysis of:

* shingle-based document representation
* MinHash signature construction
* approximation of Jaccard similarity
* LSH banding and bucket formation
* candidate retrieval for query documents
* comparison with brute-force search
* runtime scalability as the number of documents increases
* speedup achieved by LSH over exhaustive similarity computation

## Key Findings

The results show that LSH significantly reduces the number of comparisons by retrieving only a small candidate set instead of scanning the full collection. In the reported experiments, LSH search remains in the range of only a few hundredths of a second, while brute-force search grows to tens of seconds on larger subsets. The observed speedup reaches roughly 150x to 1200x, depending on dataset size.

## How to Use

1. Open the notebook from the `notebook/` folder in Jupyter Notebook, JupyterLab, or Google Colab
2. Run the cells in order
3. Review the generated outputs, plots, and evaluation results
4. Read the PDF report in the `docs/` folder for the theoretical background and discussion

## Notes

This repository was created for academic and educational purposes.

