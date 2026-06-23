# clickbait-spoiling-project
MSE641 Final Project

This repository contains code and submissions for the MSE 641 Clickbait Spoiling final project.

The project includes two subtasks:

- Task 1: Spoiler type classification
- Task 2: Spoiler generation

## Milestone 1: Naive Baselines

For Milestone 1, I ran the official naive baselines for both tasks and submitted the results to Kaggle.

### Task 1

The Task 1 naive baseline predicts the same spoiler type for every test instance:

```text
spoilerType = passage
```

The Task 1 baseline submission file is:

```text
task1/prediction_task1.csv
```

## Task 2

The Task 2 naive baseline uses the linked page title as the generated spoiler:

```text
spoiler = targetTitle
```

The Kaggle submission file has the required format:

```text
id,spoiler
```

The Task 2 baseline submission file is:

```text
task2/prediction_task2.csv
```
