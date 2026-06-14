# Customer Insight & Segmentation Studio

A Streamlit-based web application for customer segmentation using K-means clustering. This tool analyzes customer data and identifies meaningful customer segments for business insights.

## Features

- **Dataset Upload**: Support for custom CSV datasets with flexible column selection
- **Data Analysis**: Automated summary statistics, missing value detection, and correlation analysis
- **Categorical Encoding**: Automatic encoding of string/categorical columns for machine learning
- **Elbow Method**: Find the optimal number of clusters (k) using the elbow method
- **K-means Clustering**: Perform customer segmentation with customizable feature selection
- **Cluster Visualization**: 2D scatter plots to visualize customer segments
- **Cluster Insights**: View cluster statistics and customer profile descriptions
- **Prediction**: Predict cluster assignment for new customer data

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Niveditha-MG/customer-segmentation.git
cd customer-segmentation
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

1. Run the Streamlit app:
```bash
streamlit run app.py
```

2. Open your browser to:
   - Local: `http://localhost:8501`
   - Network: `http://<your-ip>:8501`

3. Upload a CSV dataset containing customer information

4. Select features for segmentation (at least 2 required)

5. The app will automatically:
   - Encode categorical columns
   - Find the optimal number of clusters
   - Perform K-means clustering
   - Display visualizations and insights

## Dataset Format

Your CSV should include customer data columns such as:
- Numeric columns: Age, Annual Income, Spending Score, etc.
- Categorical columns: Gender, Region, etc.

**Included Dataset**: `Mall_Customers.csv`
- 200 customer records
- Columns: CustomerID, Gender, Age, Annual Income (k$), Spending Score (1-100)

## Technologies Used

- **Python 3.14**
- **Streamlit**: Web app framework
- **Scikit-learn**: Machine learning (K-means, LabelEncoder, StandardScaler)
- **Pandas**: Data manipulation
- **Matplotlib**: Data visualization
- **Kneed**: Elbow detection

## Project Structure

```
customer-segmentation/
├── app.py                    # Main Streamlit application
├── Mall_Customers.csv        # Sample customer dataset
├── requirements.txt          # Python dependencies
└── README.md                 # This file
```

## How It Works

1. **Data Preprocessing**: Categorical columns are encoded to numeric values; all features are standardized
2. **Cluster Optimization**: Tests k values from 2-10 and selects the best k using silhouette score
3. **Segmentation**: Applies K-means clustering to identify customer groups
4. **Analysis**: Generates cluster profiles with mean values per segment
5. **Prediction**: Allows new customers to be assigned to existing clusters

## Requirements

See `requirements.txt` for the complete list:
- pandas>=3.0.0
- streamlit>=1.58.0
- scikit-learn>=1.9.0
- kneed>=0.8.6
- matplotlib>=3.11.0

## License

MIT License

## Author

Niveditha-MG

## Contact

For questions or issues, please visit: https://github.com/Niveditha-MG/customer-segmentation
