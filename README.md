# Pretrained Model Comparison using TOPSIS

This repository contains a comparison of various text summarization models using the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method. The models evaluated include BART, T5, Pegasus, GPT-3, and XLNet. The code takes into account multiple evaluation metrics for each model and ranks them based on a weighted aggregation of these metrics.


## Introduction

This project is focused on comparing multiple pretrained models used for text summarization. The models evaluated in this project are:

- **BART**
- **T5**
- **Pegasus**
- **GPT-3**
- **XLNet**

The comparison is done using various performance metrics, which are then processed using the **TOPSIS** method to provide a ranking of the models.

## Evaluation Metrics

The following metrics are used for evaluating the models:

1. **ROUGE-1**: Measures the overlap of unigrams between the model's generated summary and the reference summary. Higher is better.
2. **ROUGE-2**: Measures the overlap of bigrams between the model's generated summary and the reference summary. Higher is better.
3. **ROUGE-L**: Measures the longest common subsequence (LCS) between the model's generated summary and the reference summary. Higher is better.
4. **Inference Time (sec)**: Measures the time it takes for the model to generate a summary. Lower is better.
5. **Model Size (GB)**: Measures the model's size in gigabytes. Lower is better.

## TOPSIS Methodology

The **TOPSIS** method is used to rank the models based on their performance across these metrics. The steps involved in the TOPSIS methodology are as follows:

1. **Normalize the Data**: Each evaluation metric is normalized such that higher values for positive metrics (e.g., ROUGE scores) are treated as better, and lower values for negative metrics (e.g., inference time and model size) are treated as better.
   
2. **Weight the Metrics**: Each metric is assigned a weight based on its importance. In this case:
   - ROUGE metrics: 30% each
   - Inference time and model size: 10% each

3. **Calculate the Ideal and Negative Ideal Solutions**: 
   - The **ideal solution** corresponds to the maximum value for each normalized metric (best possible values).
   - The **negative ideal solution** corresponds to the minimum value for each normalized metric (worst possible values).

4. **Calculate the Separation Measures**: Calculate the Euclidean distance of each model from the ideal and negative ideal solutions.

5. **Calculate the TOPSIS Scores**: The final **TOPSIS score** for each model is calculated as the ratio of the distance to the negative ideal solution divided by the total distance to both the ideal and negative ideal solutions.

6. **Rank the Models**: The models are ranked based on their **TOPSIS scores**, where a higher score indicates better performance.

## Visualization

The code generates two types of visualizations:

1. **Bar chart of Evaluation Metrics**: A grouped bar chart is created for each model, where each bar represents one of the evaluation metrics (ROUGE-1, ROUGE-2, ROUGE-L, Inference Time, and Model Size).

2. **TOPSIS Score Comparison**: A bar chart is generated to visualize the **TOPSIS scores** for each model. The models are sorted based on their TOPSIS scores.

## Results

The models are ranked based on their **TOPSIS scores**, and the ranking is printed and visualized.

## Usage

 Clone the repository:
   ```bash
   git clone https://github.com/Sarikaa9/Pretrained_model_comparison_using_topsis.git



