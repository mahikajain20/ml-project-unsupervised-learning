
# Machine Learning Project: Unsupervised Learning

Author: Mahika Jain 

Time: 1 hr 45 mins 

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
s
2. Exploratory Data Analysis - The summary statistics of the variables were generated, along with several plots such as histograms, pairplor, correlation heatmap etc. The correlation matrix showed that Milk was significantly correlated with two other columns, Detergents_Paper and Grocery so those two were dropped and the dimesionality of the data was reduced. This was also seen to later improve the clustering of the data. 

3. K-Means Clustering - The elbow method was used to determine the optimal amount of clusters (2) and then the clustering was done on the dataset and visualized. 

4. Hierarchical clustering - a dendrogram was used to determine the optimal number of clusters and then the clustering was performed. (3 clusters)

5. Principal component Analysis - First PCA was performed to see how many components would explain a significant amount of variance in the data, which turned out to be 2. Then this was used to reduce the dimensionality of the data and the feature importances were looked at to see which feature was contibuting to which component. Some visualizations were created such as a scatter plot of the first two principal components colored by hierarchical cluster. This was to show these two techniques were dividing the data. 

6. Model Evaluation - The performance of these models was evaluated using visual inspection, silhouette scores, the elbow method for K-Means, and dendrograms for Hierarchical Clustering. After evaluation, the characteristics of each cluster were analyzed to understand their representation in the context of the data.

## Results

EDA- Right skewed distrubutions, Fresh has the highest amount of annual spending, Grocery and Milk and Detergents_Paper and Milk have a very high correlation coefficient.

KMeans- 2 clusters were shown to be optimal for this data using the elbow method. The centroids were placed clearly in the centres.

Hierarchical Clustering - The dengrogram revealed three clusters, which separated the data more based on Fresh grocery spending. 

PCA- Two components were used in PCA to reduce the dimensionality of the data. They cumulatively explained 65% of the variation. The first principal component (PC1) is strongly influenced by the 'Fresh', 'Frozen', and 'Delicassen' features. This suggests that these three types of products vary together. The second principal component (PC2) is mostly a measure of the 'Milk' and 'Delicassen' features, with 'Fresh' having a negative influence.

## Business Insights

The company can use the clusters to target customers with specific products. 
For example, customers in cluster 1 can be targeted with fresh products, while customers in cluster 2 can be targeted with milk products.

- **EDA**: The data shows that spending is right-skewed, meaning most customers spend a small amount but a few spend a lot. 
The 'Fresh' category has the highest annual spending, indicating it is a key product category for our customers. 
We also found high correlations between 'Grocery' and 'Milk', and 'Detergents_Paper' and 'Milk', suggesting that customers who buy a lot of one tend to buy a lot of the other.

- **KMeans Clustering**: The KMeans algorithm identified two distinct customer segments. 
Understanding the characteristics of these segments can help us tailor our marketing and sales strategies to better meet the needs of different types of customers.

- **Hierarchical Clustering**: Hierarchical clustering revealed three customer segments, with the key differentiator being spending on 'Fresh' groceries. 
This suggests that 'Fresh' groceries are a significant factor in customer purchasing behavior, and we may want to consider strategies to cater to customers who prioritize fresh produce.

- **PCA**: PCA reduced the dimensionality of our data to two principal components, which together explain 65% of the variation in customer spending. 
The first component is strongly influenced by 'Fresh', 'Frozen', and 'Delicassen' spending, suggesting a segment of customers who prioritize these product categories. 
The second component is largely a measure of 'Milk' and 'Delicassen' spending, with 'Fresh' having a negative influence, indicating another distinct customer segment. 
Understanding these segments can help us target our product offerings and promotions more effectively.

## Future Work

Need more time for the analysis as 1hr 40 mins is not enough for the whole project. 

- **More sophisticated clustering techniques**: While KMeans and hierarchical clustering provided interesting insights, more advanced clustering techniques like DBSCAN or Gaussian Mixture Models could be explored to see if they yield more distinct or interpretable clusters.

- **Incorporate additional data**: The current analysis is based solely on the Wholesale Data dataset. Incorporating additional data, such as customer demographics or regional information, could provide more context and lead to richer insights.

- **Time-series analysis**: If the data allows, a time-series analysis could be performed to understand how customer purchasing behavior changes over time.

- **Predictive modeling**: The unsupervised learning techniques used here could be complemented with supervised learning to predict certain outcomes based on the patterns identified. For example, a predictive model could be built to forecast future spending based on the identified clusters.

- **Feature engineering**: Additional feature engineering could be performed to create new variables that might better capture the underlying patterns in the data.

- **Hyperparameter tuning**: The parameters used in the clustering algorithms and PCA were chosen based on standard practices and some experimentation. A more systematic approach to hyperparameter tuning could potentially improve the results.


