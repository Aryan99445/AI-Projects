# Sentiment Analysis — Traditional ML vs BERT

Sentiment analysis on the IMDB Movie Reviews dataset comparing three classical machine learning models against DistilBERT. Includes a Gradio dashboard for live predictions from all models.

<br>

## How It Works

Text from movie reviews is first cleaned and preprocessed. For the traditional ML models, a TF-IDF vectorizer converts the text into numerical features which are then fed into three classifiers. For BERT, a pretrained DistilBERT model fine-tuned on sentiment data runs inference directly on the raw text. Results from all four models are compared side by side.

<br>

## Models

| Model | Approach |
|-------|---------|
| Logistic Regression | TF-IDF + linear classifier |
| Naive Bayes | TF-IDF + probabilistic classifier |
| SVM | TF-IDF + support vector classifier |
| DistilBERT | Pretrained transformer — fine-tuned on SST-2 |

<br>

## Features

- Compares traditional ML and transformer based approaches
- Accuracy, precision, recall and confusion matrix for each model
- Bar chart comparing all model accuracies
- Gradio dashboard for live sentiment prediction
- No API key required — dataset and model load automatically

<br>

## Tech Stack

| Tool | Purpose |
|------|---------|
| Scikit-learn | Traditional ML models and TF-IDF |
| HuggingFace Transformers | DistilBERT model |
| HuggingFace Datasets | IMDB dataset |
| Gradio | Interactive prediction dashboard |
| Matplotlib / Seaborn | Visualizations |

<br>

## Dataset

**IMDB Movie Reviews** — 50,000 reviews, evenly split between positive and negative sentiment. Loaded directly from HuggingFace, no download needed.

<br>

## Setup

1. Open the notebook in Google Colab
2. Enable GPU — Runtime → Change runtime type → T4 GPU
3. Run all cells — no API keys needed
4. The Gradio dashboard generates a public shareable link at the end

<br>

## Output

- Classification report and confusion matrix for each model
- Accuracy comparison chart across all 4 models
- Live Gradio dashboard with a public URL valid for 72 hours
