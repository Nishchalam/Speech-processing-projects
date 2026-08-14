# Multilingual Speech Language Identification

A speech language identification project developed as part of the IIT Madras Speech Processing course (EE6130). The project investigates pretrained self-supervised speech representations and their effectiveness for language classification.

## Objective

The project explores:
- Feature representations from different stages of pretrained Wav2Vec 2.0 models.
- Comparison of Wav2Vec 2.0 and HuBERT representations.
- Improving a CNN-based language identification classifier.
- Extending the task from three to five languages.

## Approach

The VoxPopuli multilingual speech dataset was used to construct language identification datasets.

### Languages

- English
- Spanish
- Romanian
- German
- Polish

The speech representations were extracted using pretrained:
- Wav2Vec 2.0
- HuBERT

The extracted representations were then used as inputs to a CNN-based classifier.

## Experiments

The experiments investigated:
1. Wav2Vec 2.0 representations from pretrained speech models.
2. HuBERT representations and comparison with Wav2Vec 2.0.
3. Increasing CNN model complexity.
4. Language identification with three languages.
5. Extension to five languages and analysis of classification performance.

## Technologies

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Wav2Vec 2.0
- HuBERT
- CNN
- VoxPopuli

## Repository Contents

- `Assignment1_EE6130.ipynb` — implementation and experiments
- `EE24S004_Assignment1_EE6130.pdf` — detailed assignment report

## Context

This project was completed as part of the Speech Processing coursework at IIT Madras.
