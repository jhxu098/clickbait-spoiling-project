# Clickbait Spoiling Project

Final project for **MSE 641: Text Analytics** at the University of Waterloo.

This repository contains the notebooks and Kaggle submission files for two clickbait-spoiling tasks:

- **Task 1:** Predicting Spoiler Type
- **Task 2:** Generating Spoilers

## Project Overview

Clickbait posts leave out important information to make readers open the linked article. This project focuses on predicting the type of spoiler needed and generating a spoiler from the article.

### Task 1: Predicting Spoiler Type

The goal is to predict one of three spoiler types:

- `phrase`
- `passage`
- `multi`

The final model uses **RoBERTa-base** with the clickbait post and article paragraphs.

**Best public Kaggle score: 0.78270**  
**Submission date: July 17, 2026**

### Task 2: Generating Spoilers

The goal is to generate a spoiler from the linked article.

The final approach uses:

1. spoiler-type prediction;
2. extractive question answering;
3. passage candidate generation;
4. RoBERTa cross-encoder reranking;
5. confidence and quality checks.

The final method keeps the previous QA prediction unless the new passage candidate passes several checks.

**Best public Kaggle score: 0.46217**  
**Submission date: July 25, 2026**

The final method improved the previous public score of `0.45453` while changing only 13 of the 400 test predictions.

## Repository Structure

```text
clickbait-spoiling-project/
├── README.md
├── task1/
│   ├── baseline/
│   │   ├── task1-naive-baseline.ipynb
│   │   └── prediction_task1.csv
│   ├── experiments/
│   │   └── mse641-task1-final-project.ipynb
│   ├── task1-final-model.ipynb
│   └── submission_roberta_post_article.csv
│
└── task2/
    ├── baseline/
    │   ├── task2-naive-baseline.ipynb
    │   └── prediction_task2.csv
    ├── experiments/
    │   ├── task2-experiments.ipynb
    │   └── task_2_model_0724_best.ipynb
    ├── task2-final0725.ipynb
    └── submission_crossencoder_agreement025_quality_v1.csv
```
## Notes

The competition datasets and trained model checkpoints are not included in this repository.

Some Task 2 experiments use intermediate files and model assets saved during Kaggle development, so rerunning the final notebook from the beginning may require retraining models or recreating those files.
