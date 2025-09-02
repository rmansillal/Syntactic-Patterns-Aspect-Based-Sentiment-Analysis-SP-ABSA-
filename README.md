# Beyond Benchmarks: Interpretable Aspect-Based Sentiment Analysis (SP-ABSA)

[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

This repository contains the official implementation for the research paper, "Beyond Benchmarks: Interpretable Aspect-Based Sentiment Analysis for Actionable Insights from Customer Reviews".

SP-ABSA is a transparent, lexicon-driven framework designed to extract sentiment triplets (`[Aspect, Attribute, Sentiment]`) from customer reviews. It prioritises interpretability, traceability, and actionable intelligence over raw benchmark scores, making it ideal for business applications where understanding the "why" behind an insight is crucial.

## Key Features

-   **End-to-End Interpretability**: Every step, from aspect extraction to sentiment scoring, is based on auditable linguistic rules and transparent lexicons.
-   **Unsupervised Aspect Lexicon Creation**: Automatically identifies and clusters domain-specific aspect terms from a raw corpus, making the system highly adaptable to new domains.
-   **Syntactic Pattern Matching**: Uses a curated set of high-precision syntactic dependency patterns to ensure structurally sound and reliable triplet extraction.
-   **Actionable Visualisations**: Includes code to generate strategic visualisations like the Aspect Priority Matrix and Insight Graphs to transform raw data into business intelligence.

## System Architecture

The framework is structured as a two-stage process: an offline, corpus-level lexicon creation stage and an efficient, per-sentence online extraction pipeline.

![SP-ABSA Framework Diagram](assets/framework_diagram.png)

## Getting Started

Follow these steps to set up the environment and run the analysis.

### 1. Clone the Repository

```bash
git clone https://github.com/rmansillal/Syntactic-Patterns-Aspect-Based-Sentiment-Analysis-SP-ABSA-.git
cd Syntactic-Patterns-Aspect-Based-Sentiment-Analysis-SP-ABSA-
```

### 2. Set Up a Virtual Environment (Recommended)

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3. Install Dependencies

Install all the required Python libraries using the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### 4. Download spaCy Model

The framework uses spaCy's large English model, which includes word vectors necessary for the lexicon creation process.

```bash
python -m spacy download en_core_web_lg
```

## Usage

The entire implementation, from data loading to evaluation and visualisation, is contained in the **`SP_ABSA_Implementation.ipynb`** Jupyter Notebook.

1.  Ensure the `train_triplets.txt` dataset is in the root directory.
2.  Launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    ```
3.  Open `SP_ABSA_Implementation.ipynb` and run the cells sequentially to reproduce the results and visualisations from the paper.

## Project Structure

```
.
├── SP_ABSA_Implementation.ipynb  # Main Jupyter Notebook with all code
├── train_triplets.txt            # Training and evaluation dataset
├── paper/
│   └── SP_ABSA_Paper.pdf           # The research paper
├── assets/
│   └── framework_diagram.png     # Diagram used in the README
├── requirements.txt              # Python dependencies
├── .gitignore                    # Files to be ignored by Git
└── README.md                     # You are here!
```

