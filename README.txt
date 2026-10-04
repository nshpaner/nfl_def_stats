# DSC 100 Final Project: How Takeaways Impact Expected Points Contributed by Defense

Author: Nick Shpaner

Date: 12/11/25

# Overview

This repository contains an empirical analysis exploring the relationship between defensive takeaways (TO) and Expected Points Contributed (EXP) using 2024 NFL defensive statistics across all 32 teams. The project investigates whether higher takeaway counts reliably lead to increased defensive scoring value relative to league average.

Data was extracted from Pro Football Reference's "2024 NFL Opposition & Defensive Statistics" table via CSV text formatting.

	Pro Football Reference. (2024). 2024 NFL Opponent Drive and Defense Statistics.
	https://www.pro-football-reference.com/years/2024/opp.htm


# Main Findings & Modeling Approach

The conducted analysis applies a variety of statistical and machine learning approaches to evaluate how each predictor impacts a team's overall defensive impact:

## EDA and Visualization: Evaluates linearity, directional trends, and potential outliers in takeaway metrics

## Simple Linear Regression: Measures the direct relationship between total takeaways (TO) and defensive expected points (EXP)

## Train/Test Split Evaluation: Assesses model performance and generalization capability on unseen test data using Mean Squared Error (MSE) and R^2

## Multiple Linear Regression: Controls for additional defensive metrics. 

These metrics are as follows:

	Points Allowed (PA)
	Total Yards Allowed (Yds)
	Penalties (Pen)
	First Downs Allowed (1stD)

This is done to isolate the net impact of takeaways.

## Ridge Regression with Cross-Validation: Utilizes L2 regularization and 5-fold cross-validation to mitigate potential multicollinearity among defensive variables and improve the overall predictive stability of the multiple linear regression model

Dependencies & Requirements

To run the notebook and reproduce the models, make sure you have Python 3.12.3, or newer, installed along with the libraries provided in requirements.txt

Repository Structure
* nfl_def_stats.ipynb: The main Jupyter notebook that contains the complete data ingestion, cleaning pipeline, exploratory analysis, and model evaluations.

* nfl_def_stats_codebook.xlsx: A codebook that outlines each of the variables in the dataset, listing their name, description, data type, and formatting notes

* requirements.txt: List of Python packages (with their corresponding versions) needed to run the analysis in the notebook
	Install in code+nb: pip install ipykernel -r ../requirements.txt

# Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/nshpaner/nfl_def_stats.git](https://github.com/nshpaner/nfl_def_stats.git)
   cd nfl_def_stats