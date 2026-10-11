# Netflix Movies and TV Shows Clustering

## Project Overview

This project explores the Netflix Movies and TV Shows dataset using Python and unsupervised machine learning. The goal is to analyze Netflix content, identify patterns in its characteristics, and group similar titles using the K-Means clustering algorithm.

The project includes exploratory data analysis, data cleaning, feature engineering, preprocessing, clustering, model evaluation, visualization, and cluster interpretation.

## Objectives

- Analyze the distribution of Netflix movies and TV shows.
- Explore ratings, genres, release years, countries, and directors.
- Identify missing values, inconsistent data, and potential outliers.
- Prepare categorical and numerical features for machine learning.
- Apply K-Means clustering to group Netflix titles.
- Evaluate clustering performance and interpret the resulting groups.
- Suggest potential strategies for organizing and exploring content.

## Dataset

The dataset contains **7,787 records and 12 columns**.

Key columns include:

- `show_id`
- `type`
- `title`
- `director`
- `cast`
- `country`
- `date_added`
- `release_year`
- `rating`
- `duration`
- `listed_in`
- `description`

The dataset covers Netflix movies and TV shows, including information about their genres, ratings, release years, and other content characteristics.

> Note: Dataset availability and redistribution depend on the original source's terms. Refer to the original dataset source before redistributing the CSV.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

- Inspected the dataset structure and data types.
- Analyzed movie and TV show distributions.
- Explored ratings, genres, release years, countries, and directors.
- Created visualizations to identify patterns in Netflix content.

### 2. Data Cleaning

- Checked missing values and duplicate records.
- Examined inconsistent or unknown categorical values.
- Investigated potential outliers using the Interquartile Range (IQR) method.

### 3. Feature Engineering and Preprocessing

- Selected relevant features for clustering.
- Prepared categorical features using encoding techniques.
- Scaled numerical features.
- Created a numerical feature matrix for machine learning.

### 4. K-Means Clustering

Applied the K-Means algorithm to group Netflix titles into three clusters using the prepared feature matrix.

### 5. Model Evaluation

Used the following techniques to examine the clustering results:

- **Elbow Method:** Examined inertia across different values of K.
- **Silhouette Score:** Evaluated how well the resulting clusters were separated.
- **Hierarchical Clustering:** Used a dendrogram to explore hierarchical relationships in a sample of the data.

### 6. Cluster Interpretation

Analyzed cluster sizes and characteristics to understand how the titles were grouped. The results showed that the selected features separated movies and TV shows into distinct groups, with additional differences between TV show clusters.

### 7. Stakeholder Recommendations

Based on the exploratory cluster profiles, the project suggests potential approaches for organizing content categories and improving content discovery. These are exploratory recommendations, not verified business outcomes.

## Results

The final K-Means model used three clusters.

| Metric | Result |
|---|---:|
| Dataset records | 7,787 |
| Number of clusters | 3 |
| Cluster 0 | 5,377 titles |
| Cluster 1 | 1,573 titles |
| Cluster 2 | 837 titles |
| Silhouette Score | 0.1717 |
| Inertia | 420,512.07 |

### Cluster Observations

- **Cluster 0:** Primarily movies.
- **Cluster 1:** Primarily TV shows.
- **Cluster 2:** Primarily TV shows with a different feature profile from Cluster 1.

The Silhouette Score of approximately 0.1717 indicates limited separation between clusters. The results should therefore be interpreted as exploratory groupings rather than definitive categories of Netflix content.

## Limitations

- The clustering results depend on the selected features and preprocessing methods.
- The relatively low Silhouette Score indicates that cluster separation could be improved.
- The dataset does not include viewer engagement, watch time, revenue, or recommendation performance.
- The stakeholder recommendations have not been validated using business outcome data.
- Additional feature engineering and alternative clustering algorithms could improve the analysis.

## Future Improvements

- Experiment with alternative clustering algorithms such as DBSCAN and agglomerative clustering.
- Improve feature selection and representation.
- Compare clustering performance across different feature combinations.
- Explore text-based features from content descriptions.
- Validate recommendations using viewer engagement or business data, if available.

## How to Run the Project

1. Clone or download this repository.
2. Install Python and Jupyter Notebook.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

4. Place the dataset in the location expected by the notebook.
5. Open `Netflix Movies.ipynb` in Jupyter Notebook.
6. Run the notebook cells from top to bottom.
