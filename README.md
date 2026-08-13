# hindi-news-headline-generation
Extractive and abstractive headline generation for Hindi broadcast news using NLP and transformer-based models.
# Headline Generation from Spoken Hindi Broadcast News

An NLP-based system for automatically generating headlines from spoken Hindi broadcast news. The project compares extractive and abstractive approaches under resource-constrained conditions and evaluates their performance using ROUGE metrics.

##  Overview

This project explores automatic headline generation from Hindi broadcast news obtained as audio recordings.

The pipeline converts spoken news into Hindi text using Automatic Speech Recognition (ASR), preprocesses the transcripts, generates headlines using both extractive and abstractive NLP techniques, and evaluates the generated headlines using ROUGE.

##  Pipeline

Audio
↓
Audio Segmentation
↓
Google Speech-to-Text
↓
Hindi Transcript
↓
Text Preprocessing
↓
Headline Generation
↓
ROUGE Evaluation

##  Methods Used

### Extractive Methods

- TF-IDF + TextRank
- FastText + TextRank

### Abstractive Methods

- IndicBART
- mT5-Small

##  Technologies

- Python
- Google Colab
- Google Speech-to-Text
- Scikit-learn
- NetworkX
- FastText
- Hugging Face Transformers
- PyTorch
- ROUGE

##  Results

| Method | ROUGE-1 | ROUGE-2 | ROUGE-L |
|---|---:|---:|---:|
| TF-IDF + TextRank | 0.78 | 0.62 | 0.75 |
| FastText + TextRank | 0.65 | 0.48 | 0.61 |
| IndicBART | 0.34 | 0.21 | 0.29 |
| mT5-Small | 0.28 | 0.15 | 0.23 |

### Key Finding

The extractive approaches achieved higher ROUGE scores than the abstractive approaches.

This indicates that, for the available Hindi broadcast dataset and noisy ASR transcripts, extractive methods were more effective under the project's resource constraints.

## Project Structure

```text
hindi-news-headline-generation/
│
├── headline_generation.ipynb
├── README.md
└── results/
