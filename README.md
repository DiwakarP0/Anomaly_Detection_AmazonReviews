# Anomaly Detection in Amazon Reviews

## Overview

This project is centered on **anomaly detection** in Amazon product reviews, specifically for beauty products. The workflow involves analyzing review data to identify outliers and potential fake or suspicious reviews using statistical and machine learning methods. Insights are derived from multiple visualizations and correlations between features such as *price*, *sentiment*, *rating*, and anomaly scores.

## Features

- Preprocessing and analysis of Amazon beauty product reviews ([merged_All_Beauty_processed.csv])
- Detection of anomalous reviews based on optimized statistical methods
- Visualization of feature relationships and distributions:
  - Scatter plot: price vs. anomaly flag
  - Sentiment score distribution
  - Correlation heatmap among rating, sentiment, anomaly, and price
  - Boxplot of sentiment scores across rating levels

## Repository Structure

| File/Folder                      | Description                          |
|-----------------------------------|--------------------------------------|
| `merged_All_Beauty_processed.csv` | Preprocessed beauty product reviews  |
| `analysis.py`                    | Main analysis and anomaly detection  |
| `output/`                        | Generated outputs and figures        |
| `images/`                        | Visualizations (scatter, histograms, etc.) |
| `Report.pdf`                     | Detailed project report              |
| `README.md`                      | Project documentation                |

## Visualizations

- **Scatter Plot: Price vs. Optimized Anomaly**  
  Shows how anomalous reviews are distributed across product prices.

- **Sentiment Distribution**  
  Histogram of sentiment scores across all reviews, highlighting the central tendency and spread.

- **Correlation Heatmap**  
  Displays pairwise correlation between numerical features, showing relations (e.g., weak correlation between rating and anomaly).

- **Boxplot of Sentiment Scores Across Ratings**  
  Illustrates the variability in sentiment for each rating level.

## Methods

1. **Data Preprocessing**  
   - Load CSV data and clean fields (e.g., text normalization, removal of noise)
   - Feature extraction: sentiment analysis, ratings, price, etc.

2. **Anomaly Detection**  
   - Apply machine learning/statistical anomaly scoring (custom or scikit-learn based)
   - Optimize threshold for flagging outliers

3. **Visualization and Analysis**  
   - Generate key plots to interpret relationships and outlier patterns

## Getting Started

### Requirements

- Python 3.6+
- pandas, numpy, matplotlib, seaborn
- scikit-learn (optional, for ML-based anomaly detection)

### Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/DiwakarP0/Anomaly_Detection_AmazonReviews
    cd Anomaly_Detection_AmazonReviews
    ```
2. (Optional) If a requirements file is provided:
    ```bash
    pip install -r requirements.txt
    ```
3. Run the main script:
    ```bash
    python analysis.py
    ```
   This will generate output figures and anomaly flags.

## Results & Insights

- Most anomalous reviews are concentrated at lower price points; expensive products have fewer flagged outliers.
- The majority of reviews cluster around neutral sentiment scores, with a sharp central peak.
- Feature correlations are generally weak (see heatmap), indicating low linear dependence.
- Sentiment scores are distributed similarly across all ratings, with wide variance in extreme ratings.

## Contributing

Contributions are welcome! Fork the repo and open pull requests for ideas, improvements, or bug fixes.

## Acknowledgments

Thanks to academic and industry resources that inspired this work, along with open-source anomaly detection guides and Amazon product review analysis studies.
