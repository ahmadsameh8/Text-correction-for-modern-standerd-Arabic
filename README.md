# Text-correction-for-modern-standerd-Arabic

This repository contains Notebooks for finetuning Arat5v2 model capable of correcting errors in  modern standard arabic texts.


## Table of Contents

1. [Data Extraction Pipeline](#1-data-extraction-pipeline)
2. [Preprocessing and Data Preparation](#2-preprocessing-and-data-preparation)
3. [Fine-Tuning AraT5 for Text Correction](#3-fine-tuning-arat5-for-text-correction)

---


## 1. Data Extraction Pipeline

**File:** `DataExtraction.ipynb`

### Overview
This Notebook implements a pipeline for extracting and structuring information from unstructured data. The focus is on making data easily accessible for analytics and further processing.

### Key Features
- Parses and structures extracted information into predefined formats.

### Usage
Run the notebook to process your documents and generate structured outputs. Modify the input paths.

---

## 2. Preprocessing and Data Preparation

**File:** `preprocessingAndGettingDataReady.ipynb`

### Overview
This project involves preparing and processing raw datasets for language model fine-tuning pipeline. Key steps include:

- Cleans text by removing English characters, mentions, URLs, and hashtags (except those with trailing characters), while preserving whitespace.
- standardize Arabic words.
- Remove longation.
- Remove diacritical marks.
- Converting the dataset to a hugging face Object
- Splitting data into training, validation, and testing subsets.
- Pushing the dataset to Huggingface

### Key Features
- Implements robust preprocessing methods.
- Utilizes pandas and NumPy for efficient data handling.
- Ensures readiness for model training and evaluation.

### Usage
Run the notebook to preprocess the dataset and save the prepared data for later finetuning.

---

## 3. Fine-Tuning AraT5 for Text Correction

**File:** `fineTuningArat5ForTextCorrection.ipynb`

### Overview
This Notebook fine-tunes the AraT5 model for text correction, targeting Modern standard Arabic text. The notebook includes steps for dataset preparation, model configuration, and training.

### Key Features
- Leverages Hugging Face's Transformers library.
- Handles seq2seqtrainer for supervised finetuning with various hyperparameters.
- Push model weights to Huggingface

### Usage
- Configure the training parameters and dataset paths in the notebook.
- Run the notebook to fine-tune the AraT5 model and push model weights to Huggingface.

