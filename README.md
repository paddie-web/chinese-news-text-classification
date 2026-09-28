# Chinese News Text Classification

This project applies pretrained Chinese language models to a multi-class news text classification task. Given a labeled training dataset and unseen news articles, the models are fine-tuned to predict the category of each news article.

The project focuses on model fine-tuning, performance evaluation, model comparison, and interpretable error analysis.

## Project Overview

Three pretrained Chinese language models were fine-tuned and evaluated under a comparable training setup:

- BERT-base-Chinese
- Chinese-MacBERT-base
- Chinese-RoBERTa-wwm-ext

The main analysis uses **BERT-base-Chinese**, followed by a comparison of the three models.

## Methods

The project includes:

1. Data loading and preprocessing
2. Label encoding and dataset construction
3. Fine-tuning pretrained Transformer models
4. Model evaluation using accuracy, precision, recall, and F1 score
5. Confusion matrix analysis
6. Case-based error analysis
7. LIME-based local interpretability analysis
8. Comparison of training convergence and model performance

## Results

The three models achieved similar performance on the news classification task.

| Model | Accuracy | F1 |
|---|---:|---:|
| BERT-base-Chinese | 95.14% | 95.14% |
| Chinese-MacBERT-base | 94.79% | 94.79% |
| Chinese-RoBERTa-wwm-ext | 94.57% | 94.57% |

The analysis further examines the types of classification errors made by the models. In particular, LIME is used to identify text segments that contributed most strongly to selected misclassifications, providing an interpretable view of the model's decision process.

## Error Analysis

The confusion matrix shows that some semantically related categories are more difficult to distinguish. For example, financial news and stock-market news exhibit relatively frequent confusion.

LIME is then applied to misclassified examples to investigate which textual features contribute to these predictions. This provides a more detailed perspective on the limitations of the classification model beyond aggregate accuracy.

## Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- scikit-learn
- pandas
- NumPy
- Matplotlib
- Seaborn
- LIME

## Repository Contents

- `news_classification.ipynb` — main notebook containing data processing, model fine-tuning, evaluation, and error analysis.
- `README.md` — project overview and documentation.

The original datasets are not included in this repository because they were provided as part of a course project.

## Note

This project was completed as part of a Natural Language Processing course project.
