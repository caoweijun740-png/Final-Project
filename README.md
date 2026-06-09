# Final Project Analysis

This project contains an R script for conducting a statistical analysis of biomedical and outcome-related data. The analysis focuses on exploring associations between unused biomarker variables and a binary outcome variable.

## Project Overview

The script performs a complete data analysis workflow, including data loading, cleaning, merging, statistical testing, regression modeling, correlation analysis, dimensionality reduction, clustering, validation, and visualization.

The analysis uses only base R, `stats`, and `graphics`, so no additional R packages need to be installed.

## Required Files

Place the R script in the same folder as the following CSV files:

* `imputed_data.csv`
* `factor_data.csv`
* `distribution.csv`

The script will automatically search for these files in the working directory, Downloads folder, or Desktop.

## Main Analysis Steps

The workflow includes:

* Loading and cleaning CSV data
* Merging imputed data with factor data by `record_id`
* Removing missing outcome values
* Comparing biomarker values between outcome groups
* Running Wilcoxon rank-sum tests
* Performing univariate logistic regression
* Adjusting p-values using FDR correction
* Building adjusted logistic regression models
* Creating a multivariable stepwise logistic regression model
* Calculating Spearman correlations
* Testing categorical factors with chi-square tests
* Running PCA on standardized biomarker variables
* Performing K-means clustering
* Evaluating model performance using train-test AUC
* Analyzing distribution data with the Kruskal-Wallis test
* Generating figures for interpretation

## Output

After running the script, results will be saved in a folder named:

```text
final_project_output
```

This folder includes CSV result files, model summaries, validation results, and a `figures` folder containing generated plots.

Main output files include:

* `numeric_tests.csv`
* `adjusted_logistic.csv`
* `multivariable_stepwise_model.txt`
* `spearman_correlation.csv`
* `point_biserial.csv`
* `factor_tests.csv`
* `pca_loadings.csv`
* `kmeans_clusters.csv`
* `validation_auc.csv`

Generated figures include:

* FDR-adjusted p-value plot
* Boxplots of top biomarkers
* Spearman correlation heatmap
* PCA plot by outcome
* K-means clustering plot
* Distribution histograms

## How to Run

Open the R script in RStudio and click **Source**, or run the script from the R console.

Make sure the required CSV files are located in the same folder as the script before running it.

## Notes

This project was designed to be simple and reproducible. Since it only uses base R functions, it can be run on most R installations without installing extra packages.
