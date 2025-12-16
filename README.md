# Customer Segmentation Analysis

## Project Overview
This project performs customer segmentation analysis using the Customer Personality Analysis dataset from Kaggle. The goal is to identify distinct customer groups based on purchasing behavior, demographics, and campaign responsiveness to enable targeted marketing strategies.

## Dataset
The analysis uses the "Customer Personality Analysis" dataset from Kaggle, containing 2,240 customers with 29 attributes including demographic information, product purchases, and marketing campaign responses.

## Key Features

### Data Preprocessing
- Handled missing values in income data
- Engineered new features including:
  - Customer tenure (`Customer_For`)
  - Age calculation from birth year
  - Total spending across categories (`Spent`)
  - Family composition features (`Living_With`, `Children`, `Family_Size`, `Is_Parent`)
  - Simplified education categories
- Dropped redundant features like ID, constant columns, and date fields

### Analysis Techniques
1. **Exploratory Data Analysis**: Visual exploration of customer demographics and behavior patterns
2. **Feature Engineering**: Created meaningful derived features for clustering
3. **Dimensionality Reduction**: Applied Principal Component Analysis (PCA)
4. **Customer Segmentation**: Used K-Means clustering with Elbow Method for optimal cluster determination
5. **Visualization**: Pair plots, 3D scatter plots, and cluster visualizations

## Methodology

### 1. Data Preparation
- Loaded and cleaned customer data
- Engineered 6 new features from existing variables
- Removed outliers and irrelevant columns

### 2. Clustering Process
- Standardized numerical features
- Applied PCA for dimensionality reduction
- Determined optimal clusters using the Elbow Method
- Implemented K-Means clustering
- Analyzed and interpreted cluster characteristics

### 3. Feature Engineering Highlights
- `Customer_For`: Days since customer enrollment
- `Spent`: Total amount spent across 6 product categories
- `Living_With`: Simplified relationship status (Partner/Alone)
- `Family_Size`: Total family members
- `Is_Parent`: Binary indicator of parenthood status

## Technical Implementation

### Libraries Used
- **Data Manipulation**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Machine Learning**: scikit-learn (preprocessing, PCA, K-Means)
- **Model Selection**: yellowbrick (KElbowVisualizer)
- **Date Handling**: datetime

### Main Steps in Notebook
1. Import libraries and load data
2. Data cleaning and preprocessing
3. Feature engineering and transformation
4. Exploratory data analysis
5. Feature scaling and PCA
6. Determine optimal clusters
7. Apply K-Means clustering
8. Visualize and analyze results

## Project Structure
```
customer-segmentation/
├── customer-segmentation.ipynb    # Main analysis notebook
├── marketing_campaign.csv         # Dataset (download from Kaggle)
├── README.md                      # This file
└── requirements.txt               # Python dependencies
```

## Getting Started

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Required libraries: pandas, numpy, matplotlib, seaborn, scikit-learn, yellowbrick

### Installation
1. Clone the repository:
```bash
git clone https://github.com/yourusername/customer-segmentation.git
cd customer-segmentation
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the dataset from Kaggle and place it in the project directory

4. Run the Jupyter notebook:
```bash
jupyter notebook customer-segmentation.ipynb
```

## Business Applications
- Targeted marketing campaigns based on customer segments
- Personalized product recommendations
- Customer retention strategies
- Resource allocation optimization
- Campaign effectiveness analysis

## Key Findings
- Identified distinct customer segments with unique behavioral patterns
- High-income segments show different purchasing habits
- Family composition significantly influences spending behavior
- Campaign responsiveness varies across customer groups

## Future Enhancements
- Additional clustering algorithms (DBSCAN, Hierarchical)
- Time-series analysis of customer behavior
- Predictive modeling for customer lifetime value
- Integration with real-time data pipelines
- A/B testing framework for segment-specific campaigns

## References
- Dataset: [Customer Personality Analysis on Kaggle](https://www.kaggle.com/imakash3011/customer-personality-analysis)
- Scikit-learn Documentation



## Contact
For questions or collaboration opportunities, please open an issue in the repository or contact the maintainer directly.
