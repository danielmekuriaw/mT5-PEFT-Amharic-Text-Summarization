# mT5 PEFT Amharic Text Summarization

## Overview
This repository hosts a series of Jupyter notebooks and a Python script for the fine-tuning and evaluation of the mT5-small model, focusing on Arabic, Amharic, and English languages. The project leverages the IA3 Parameter-Efficient Fine-Tuning (PEFT) technique, to improve the Amharic text summarization capabilities of the mT5 model.

**Link to Final Report:** [Final Report](https://drive.google.com/file/d/1LivrnwkGAJfmCo6kDLTUJNIoy8RlpRF7/view)

**Link to Medium Article:** [Medium Article](https://daniel-mekuriaw16.medium.com/amharic-ia3-peft-4f1067edbd79)

### Contents
- `Amharic_Text_Summarization_Data_Aggregation_and_Cleaning.ipynb`
- `mT5_Arabic_PEFT_Finetuning.ipynb`
- `mT5_English_PEFT_Finetuning.ipynb`
- `mT5_Amharic_PEFT_Finetuning.ipynb`
- `Bounded_Token_Length_mT5_Amharic_PEFT_Finetuning.ipynb`
- `Model_Evaluation.ipynb`
- `training_module.py`

## Data Aggregation and Cleaning
- **Notebook:** `Amharic_Text_Summarization_Data_Aggregation_and_Cleaning.ipynb`
- **Purpose:** Gathers, compiles, cleans and preprocesses Amharic data from various sources for model training.

## Fine-tuning Flows

### Arabic Fine-tuning
- **Notebook:** `mT5_Arabic_PEFT_Finetuning.ipynb`
- **Process:** 
  - First loop: Arabic data training (Arabic-FT).
  - Second loop: Further fine-tuning with Arabic and/or Amharic datasets.
- **Models Produced:**
  - Arabic-FT
  - Arabic-English-FT
  - Arabic-Amharic-FT
  - Improved-Arabic-English-Amharic-FT

### English Fine-tuning
- **Notebook:** `mT5_English_PEFT_Finetuning.ipynb`
- **Process:** 
  - First loop: English data training (English-FT).
  - Second loop: Further fine-tuning with Arabic and/or Amharic datasets.
- **Models Produced:**
  - English-FT
  - English-Arabic-FT
  - English-Amharic-FT
  - Improved-English-Arabic-Amharic-FT

### Amharic Model Fine-tuning
- **Notebooks:** `mT5_Amharic_PEFT_Finetuning.ipynb`, `Bounded_Token_Length_mT5_Amharic_PEFT_Finetuning.ipynb`
- **Features:** 
  - Fine-tuning mT5-small with Amharic-1, Amharic-2, and Amharic-3 datasets.
  - Amharic-2 includes normalization steps in preprocessing.
- **Models Produced:**
  - Initial-Amharic-FT (using Amharic-1)
  - Improved-Amharic-FT (using Amharic-2)
  - Improved-Amharic-FT-2 (using Amharic-3)

## Model Evaluation
- **Notebook:** `Model_Evaluation.ipynb`
- **Purpose:** Quantitative evaluation of fine-tuned models.
- **Metrics Included:** ROUGE-1, ROUGE-2, ROUGE-L, BLEU, Average Precision, Recall, and F1.

## Training Module
- **File:** `training_module.py`
- **Description:** Core training loop function, used across different fine-tuning notebooks.

## Getting Started
1. Clone the repository.
2. Follow the instructions in each notebook for fine-tuning and evaluation. You may have to install the libraries installed by the first cells of all the notebooks within your environment if they are not already installed.
---
