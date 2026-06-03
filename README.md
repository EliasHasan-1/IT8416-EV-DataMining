# IT8416 Data Mining Project — Washington State EV Classification

**Bahrain Polytechnic | IT8416 Data Mining | 2026**

## Project Overview

This project applies supervised classification techniques to the Washington State 
Electric Vehicle Population dataset to classify vehicles as Battery Electric (BEV) 
or Plug-in Hybrid Electric (PHEV). The goal is to identify the key features that 
distinguish vehicle types and provide data-driven production recommendations for 
EV manufacturers operating in Washington State.

## Dataset

**Washington State Electric Vehicle Population Data**  
Source: [Kaggle](https://www.kaggle.com/datasets/ratikkakkar/electric-vehicle-population-data)  
- 257,635 rows | 17 attributes  
- Target variable: Electric Vehicle Type (BEV / PHEV)  
- Class distribution: 79.6% BEV | 20.4% PHEV

## Tools Used

- **Altair AI Studio (RapidMiner) 2026.1.1** — data cleaning, preprocessing and model building
- **Python (matplotlib)** — data visualisations

## Pipeline Files

| File | Description |
|------|-------------|
| `task3_cleaned_data.rmp` | Data cleaning and preprocessing pipeline |
| `task4_models.rmp` | Model building — Decision Tree, Naive Bayes, Vote Ensemble |

## Models and Results

| Model | Test Accuracy | Validation Accuracy | PHEV Errors (val) |
|-------|--------------|--------------------|--------------------|
| Decision Tree | 99.73% | 99.78% | 1 |
| Naive Bayes | 99.60% | 99.64% | 38 |
| **Vote Ensemble ★** | **99.73%** | **99.79%** | **0** |

**Recommended model: Vote Ensemble** — highest validation accuracy with zero 
PHEV misclassifications on the untouched validation set.

## Key Finding

The Decision Tree root split at **Electric Range > 72.5 miles** is the single 
most important feature separating BEV from PHEV vehicles, confirmed by PCA 
(PC1 explains 99.9% of numeric variance).

## Project Structure

- `task3_cleaned_data.rmp` — Preprocessing pipeline
- `task4_models.rmp` — Classification models  
- `report.docx` — Full project report
- `README.md` — This file

## Video Demonstration

Watch the full project walkthrough on YouTube:  
[IT8416 Data Mining Project — Video Demo](YOUR_YOUTUBE_LINK_HERE)

## Author

Bahrain Polytechnic — IT8416 Data Mining
