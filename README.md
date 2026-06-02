[README.md](https://github.com/user-attachments/files/28523193/README.md)

# Legal Machine Translation Failure Analysis

This repository contains a small comparative study of machine translation failures in legal texts. It focuses on three English legal instruments with official Turkish and Italian human translations and corresponding machine translations:

- **CISG** — United Nations Convention on Contracts for the International Sale of Goods
- **ECHR** — European Convention on Human Rights
- **GDPR** — General Data Protection Regulation

The project is designed for an academic paper on semantic and pragmatic failures in legal machine translation.

## Research focus

The analysis examines whether machine translation preserves:

- legal terminology and institutional phraseology;
- semantic precision;
- pragmatic force and normative authority;
- conditionality, modality, evidentiality, and legal restriction;
- conventional legal drafting style in Turkish and Italian.

## Repository structure

```text
legal-mt-failure-analysis/
├── data/
│   └── raw/
│       ├── CISG.xlsx
│       ├── ECHR.xlsx
│       └── GDPR.xlsx
├── docs/
│   └── analysis_report.md
├── notebooks/
│   └── exploratory_analysis.ipynb
├── results/
│   ├── combined_failure_dataset.csv
│   └── failure_summary.csv
├── src/
│   └── analyze_failures.py
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## Dataset description

Each Excel file contains selected legal passages and comparative translation analysis. The main columns are:

- `Location` — article, recital, or provision;
- `Source` — English source text;
- `Turkish HT` — official Turkish human translation;
- `Turkish MT` — machine translation into Turkish;
- `Failure` / `Failure Explanation` — Turkish semantic and pragmatic failure analysis;
- `Italian HT` — official Italian human translation;
- `Italian MT` — machine translation into Italian;
- `Failure.1` / `Failure Explanation.1` — Italian semantic and pragmatic failure analysis.

## How to run

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the analysis script:

```bash
python src/analyze_failures.py
```

The script loads the Excel files, combines them into one dataset, and exports CSV summaries to the `results/` folder.

## Possible research question

> How does machine translation fail to preserve semantic precision and pragmatic/legal force in multilingual legal texts, especially when translating complex legal provisions from English into Turkish and Italian?

## Suggested citation note

When using this repository in an academic paper, cite the official legal instruments separately and describe this dataset as a manually curated comparative analysis of selected legal provisions.
