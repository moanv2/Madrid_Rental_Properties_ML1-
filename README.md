# Madrid Rental Market Analysis

Group 5 assignment for Machine Learning I (MBDS) at IE University.

The project analyzes 2,089 rental property listings scraped from idealista.com in Madrid. The goal is to segment the market into meaningful groups and then build a supervised model on a chosen segment.

## Dataset

The file `Houses_for_rent_in_Madrid.xlsx` contains 15 columns:

| Column | Description |
|---|---|
| Id | Unique listing identifier |
| District | Madrid district (20 total) |
| Address | Street name |
| Number | Street number |
| Area | Neighborhood within the district |
| Rent | Monthly rent in euros |
| Bedrooms | Number of bedrooms |
| Sq.Mt | Size in square meters |
| Floor | Floor number |
| Outer | 1 if exterior facing, 0 otherwise |
| Elevator | 1 if building has elevator, 0 otherwise |
| Penthouse | 1 if penthouse, 0 otherwise |
| Cottage | 1 if cottage, 0 otherwise |
| Duplex | 1 if duplex, 0 otherwise |
| Semidetached | 1 if semidetached, 0 otherwise |

## Project Structure

### Phase 1: Segmentation

Data audit, cleaning, and preparation. This includes handling missing values, fixing data entry errors, removing outliers using IQR, and standardizing features.

Feature selection for clustering using variance analysis and correlation checks.

K Means clustering over a range of K values (2 through 7), validated with the Elbow Method and Silhouette Score.

Cluster profiling with descriptive statistics, district distribution, and visualizations. Each cluster is assigned a business label.

One or two clusters are selected for Phase 2 based on sample size, rent variance, and business relevance.

### Phase 2: Supervised Model

One of the following:

**Option A: Linear Regression**
Build a model to predict monthly rent within the chosen segment. Useful for estimating fair rental prices and identifying underpriced listings.

**Option B: Logistic Regression**
Build a classification model to predict whether a property rents at or above 1,800 euros per month. Useful for understanding what drives premium pricing.

## Setup

### Requirements

Python 3.8 or higher.

### Install Dependencies

```
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl scipy
```

## Team

Andrea Alarcon Valles, Antonio Abad Ballbe, Jo Al Ahmar, Vlad-Matei Marinescu & Diego Alfaro Gomez | Machine Learning I, MBDS, IE University, 2026.
