# Capstone Project 1: Analysis of Adult Body Measurements (NHANES)

Exploratory data analysis of adult body measurements using **NumPy matrices** (multidimensional data), carried out as part of the Corizo Data Science capstone programme.

## Overview

This project analyses two excerpts of the U.S. National Health and Nutrition Examination Survey (NHANES, 2017 to March 2020), containing body measurements of adult males and females. The analysis is delivered as a single Jupyter notebook structured as a report, with an explanation before each code cell and a discussion of the results after it.

## Dataset

Source: [gagolews/teaching-data](https://github.com/gagolews/teaching-data/tree/master/marek)

| File | Rows | Description |
|---|---|---|
| `nhanes_adult_male_bmx_2020.csv` | 4,081 | Adult male participants |
| `nhanes_adult_female_bmx_2020.csv` | 4,221 | Adult female participants |

Each file has seven columns: weight (kg), standing height (cm), upper arm length (cm), upper leg length (cm), arm circumference (cm), hip circumference (cm) and waist circumference (cm). There are no missing values.

The notebook downloads the files automatically if they are not present in the working directory.

## Contents of the Notebook

1. Data loading into NumPy matrices `male` and `female`
2. Histograms of male and female weight (shared x-axis limits)
3. Box plot comparing male and female weight
4. Numerical summaries: location, dispersion and shape
5. Body mass index (BMI) for females and standardisation (z-scores) into `zfemale`
6. Scatterplot matrix (pairplot) with Pearson and Spearman correlations
7. Waist-to-height ratio (WHtR) and waist-to-hip ratio (WHR) for both sexes
8. Box plot of the four ratio distributions
9. Advantages and disadvantages of BMI, WHtR and WHR
10. Standardised measurements of the five lowest and five highest BMI cases
11. Conclusions

## Key Findings

- Body weight is right-skewed in both sexes. Males are heavier on average (about 88.4 kg vs. 77.4 kg), while the absolute spread is almost identical.
- In females, weight, waist circumference, hip circumference and BMI are strongly correlated (Pearson r of about 0.90 to 0.95), whereas BMI is practically uncorrelated with height (r of about 0.03).
- Females show a higher WHtR, while males show a higher WHR, so the choice of index affects conclusions about sex differences.
- The most extreme BMI values are driven by body mass and girth, not by height.

## Requirements

- Python 3.9 or later
- numpy
- pandas
- scipy
- matplotlib
- seaborn
- jupyter (or JupyterLab)

Install the dependencies with:

```bash
pip install numpy pandas scipy matplotlib seaborn jupyter
```

## How to Run

```bash
git clone https://github.com/<your-username>/<your-repository>.git
cd <your-repository>
jupyter notebook Capstone_1_NHANES.ipynb
```

Then select **Run → Run All Cells**. Alternatively, upload the notebook to Google Colab; no further setup is needed.

## Repository Structure

```
.
├── Capstone_1_NHANES.ipynb   # Main report (executed notebook with outputs)
└── README.md
```

## Author

**Your Name**
M.Sc. Information Technology

## Acknowledgements

Data: U.S. Centers for Disease Control and Prevention, National Health and Nutrition Examination Survey, as prepared by Marek Gagolewski.
