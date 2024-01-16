# Document Reader

This document reader is a tool for extracting text from images and classifying them into specific categories such as email, resume, or scientific publication. It utilizes Optical Character Recognition (OCR) with Pytesseract and employs neural networks for classification.

## Table of Contents

- [Dependencies](#dependencies)
- [Usage](#usage)
- [Training](#training)
  - [Model Versions](#model-versions)
- [Evaluation](#evaluation)

## Dependencies

Make sure you have the following dependencies installed:

- Python 3.11.5
- TensorFlow
- Pytesseract
- Pillow
- EasyOCR
- Matplotlib
- WordCloud
- Scikit-learn
- NLTK
- Unidecode

# Document Reader Usage

To use the document reader, follow these steps:

1.**Install the required dependencies.**
2.**Ensure Tesseract OCR is installed and set the correct path.**
3.**Run the `document_reader.py` script.**

# Training

The neural network models are trained using different hyperparameter combinations. Three model versions (V1, V2, V3) are considered, each with variations in architecture and regularization techniques.

## Model Versions

### V1

- **Architecture:** LSTM layers with dropout
- **Hyperparameters:** Adam optimizer, varying dropout rates, batch sizes

### V2

- **Architecture:** LSTM layers with an additional dense layer
- **Hyperparameters:** Adam optimizer, varying dropout rates, batch sizes

### V3

- **Architecture:** LSTM layers with kernel regularization
- **Hyperparameters:** Adam optimizer, varying dropout rates, batch sizes

Training results and hyperparameter tuning details are available in the notebook.

# Evaluation

The best models for each version are saved and can be loaded for predictions. New data can be processed through the models to predict the category of the text.
