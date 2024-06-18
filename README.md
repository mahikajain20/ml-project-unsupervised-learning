
# Machine Learning Project: Unsupervised Learning

Author: Mahika Jain 

## Project Overview
In this project, unsupervised learning techniques are applied to a real-world dataset, the "Wholesale Data" dataset, which contains information about various products sold by a grocery store. The project involves four main parts: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.

## Objectives
- Perform exploratory data analysis and pre-processing: Import and clean the datasets, analyze and visualize the relationships between the different variables, handle missing values and outliers, and perform feature engineering as needed.
- Apply unsupervised learning techniques: Use the Wholesale Data dataset to perform k-means clustering, hierarchical clustering, and principal component analysis (PCA) to identify patterns and group similar data points together. Determine the optimal number of clusters and communicate the insights gained through data visualization.

## Tools and Libraries Used
- Python
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Data
The data used in this project is the "Wholesale Data" dataset. This dataset contains information about various products sold by a grocery store. It refers to clients of a wholesale distributor. It includes the annual spending in monetary units (m.u.) on diverse product categories

Source: UCI Wholesale customers Data Set

## Methodology

1. Data Preprocessing - The data was checked for null values and log-transformed as the continous variables were all very right skewed. 
The outliers were adjusted through the log transformation. 

2. Exploratory Data Analysis - The summary statistics of the variables were generated, along with several plots such as histograms, pairplor, correlation heatmap etc. The correlation matrix showed that Milk was significantly correlated with two other columns, Detergents_Paper and Grocery so those two were dropped and the dimesionality of the data was reduced. This was also seen to later improve the clustering of the data. 

3. K-Means Clustering - The elbow method was used to determine the optimal amount of clusters (2) and then the clustering was done on the dataset and visualized. 

4. Hierarchical clustering - a dendrogram was used to determine the optimal number of clusters and then the clustering was performed. (3 clusters)

5. Principal component Analysis - First PCA was performed to see how many components would explain a significant amount of variance in the data, which turned out to be 2. Then this was used to reduce the dimensionality of the data and the feature importances were looked at to see which feature was contibuting to which component. Some visualizations were created such as a scatter plot of the first two principal components colored by hierarchical cluster. This was to show these two techniques were dividing the data. 

6. Model Evaluation - 

## Results


## Future Work

- **More sophisticated clustering techniques**: While KMeans and hierarchical clustering provided interesting insights, more advanced clustering techniques like DBSCAN or Gaussian Mixture Models could be explored to see if they yield more distinct or interpretable clusters.

- **Incorporate additional data**: The current analysis is based solely on the Wholesale Data dataset. Incorporating additional data, such as customer demographics or regional information, could provide more context and lead to richer insights.

- **Time-series analysis**: If the data allows, a time-series analysis could be performed to understand how customer purchasing behavior changes over time.

- **Predictive modeling**: The unsupervised learning techniques used here could be complemented with supervised learning to predict certain outcomes based on the patterns identified. For example, a predictive model could be built to forecast future spending based on the identified clusters.

- **Feature engineering**: Additional feature engineering could be performed to create new variables that might better capture the underlying patterns in the data.

- **Hyperparameter tuning**: The parameters used in the clustering algorithms and PCA were chosen based on standard practices and some experimentation. A more systematic approach to hyperparameter tuning could potentially improve the results.


