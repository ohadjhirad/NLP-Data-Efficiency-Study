# How Much Data Is Enough? Finding the Cost-Effectiveness Threshold

This repository contains the code, data analysis, and visualizations for my empirical study on data efficiency in Transformer fine-tuning. 

The project investigates the "Diminishing Returns" of scaling training data using **DistilBERT** on the **MNLI dataset**.

## 📊 Key Findings
* **The 20% Rule:** Our experiment shows that 20% of the training data is enough to reach ~94% of the model's peak performance.
* **Diminishing ROI:** Beyond the 20% threshold, training time continues to scale linearly while marginal accuracy gains drop by over 80%.
* **Optimal Stopping Point:** Identifies the "Elbow" of the learning curve to save GPU hours and labeling costs.

## 📁 Project Structure
* `training_size_exp.ipynb`: The main Jupyter Notebook containing the training loops and evaluation logic.
* `experiment_results.csv`: Raw data from 11 different training iterations.
* `images/`: High-resolution plots used in the TDS article.

## 🚀 Methodology
We used **DistilBERT-base-uncased** and fine-tuned it on incremental subsets of the MNLI dataset (from 0% to 80% in 5-10% steps). All experiments were conducted with a fixed test set to ensure consistent evaluation.
---
*Created by Ohad Jhirad*
