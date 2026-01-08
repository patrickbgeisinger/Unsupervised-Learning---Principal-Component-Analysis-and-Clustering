# Unsupervised-Learning---Principal-Component-Analysis-and-Clustering
This project performs an in-depth analysis of crime rates across the United States using unsupervised machine learning techniques.

## Project Overview
This project performs an in-depth analysis of crime rates across the United States using unsupervised machine learning techniques. Using the USArrests dataset from 1973, we apply Principal Component Analysis (PCA) for dimensionality reduction and multiple clustering techniques to identify patterns and relationships between different types of crime and urban density across the 50 US states.

## Features
- Comprehensive exploratory data analysis (EDA)
- Data preprocessing and normalization
- Correlation analysis of crime variables
- Principal Component Analysis (PCA)
- Biplot visualization of PC1 and PC2
- Multiple clustering techniques (K-Means, Hierarchical)
- Cluster interpretation and validation
- Statistical insights and reporting

## Technologies Used
- **Python 3.8+**
- **pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **scikit-learn** - PCA and clustering algorithms
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scipy** - Scientific computing and hierarchical clustering
- **Jupyter Notebook** - Interactive development

## Dataset Information

### USArrests Dataset
- **Source**: R datasets package
- **Year**: 1973
- **Observations**: 50 US states
- **Variables**:
  - **Murder**: Murder arrests per 100,000 residents
  - **Assault**: Assault arrests per 100,000 residents
  - **Rape**: Rape arrests per 100,000 residents
  - **UrbanPop**: Percentage of population living in urban areas
 

## Project Workflow

### 1. Data Exploration
- Load and inspect the USArrests dataset
- Check for missing values and data quality
- Generate descriptive statistics
- Visualize distributions of crime variables

### 2. Data Preprocessing
- Handle missing values (if any)
- Standardize/normalize features for PCA
- Justify preprocessing decisions based on data characteristics

### 3. Correlation Analysis
- Compute correlation matrix between variables
- Visualize correlations using heatmap
- Interpret relationships between crime types and urbanization
- Identify multicollinearity

### 4. Principal Component Analysis (PCA)
- Apply PCA to reduce dimensionality
- Analyze explained variance ratio
- Create scree plot to visualize variance explained
- Generate biplot of first two principal components
- Interpret PC loadings and their meaning

### 5. Component Selection
- Use elbow method or cumulative variance
- Justify number of components to retain
- Typically select components explaining 80-90% of variance

### 6. Clustering Analysis
- **K-Means Clustering**:
  - Determine optimal number of clusters (elbow method, silhouette score)
  - Apply K-Means algorithm
  - Visualize clusters in PCA space
  
- **Hierarchical Clustering**:
  - Generate dendrogram
  - Apply agglomerative clustering
  - Compare with K-Means results

### 7. Cluster Interpretation
- Analyze cluster characteristics
- Identify patterns within clusters
- Compare states within same cluster
- Draw insights about crime patterns and urban density

## Results

### Correlation Analysis Findings
[Add your findings after analysis]
- Strongest correlations: Murder and Assault - .80
- Urban density relationship: Urban population has weak positive correlation indicating poor prediction of crime rates
- Key observations: Based on the observations, violent crimes typically happen together. ('Assault' and 'Rape' (.66), 'Murder' and 'Rape' (.56))

### PCA Results
- **Total variance explained by PC1**: 62%
- **Total variance explained by PC2**: 25%
- **Cumulative variance (PC1 + PC2)**: 87%
- **Number of components selected**: 3 components
- **Justification**: Selected 3 componenents for PCA due to the third component bringing total explained variance to 96% resulting in reduced dimensionality with minimal loss in information.

### Biplot Insights

#### Primary Component 1 (horizontal axis)
- 'Murder', 'Assault' and 'Rape' all point strongly to the right
- States on the right have high crime rates while states on the left have low crime rates

#### Primary Component 2 (vertical axis)
- 'Urbanpop' points upward, while crim variables point slightly upward
- This captures the urban vs. rural dimension somewhat independently of crime

#### Arrow Length
- Longer arrows equal stronger contribution to the first two components
- 'Murder', 'Assault', and 'Rape' are the strongest contributors
- All crimes are pointing in similar directions confirming that the correlation is correct.
  
### Clustering Results

#### K-Means Clustering**:
- Optimal number of clusters: 3
- Silhouette score: 0.3889

#### Hierarchical Clustering**:
- Linkage method: [Ward/Complete/Average]
- Number of clusters: 3
- Comparison with K-Means: [Similarities/Differences]

## Visualizations

The project includes several key visualizations:

1. **Correlation Heatmap**: Shows relationships between all variables
2. **Scree Plot**: Displays variance explained by each principal component
3. **Biplot**: Visualizes states and variables in PC1-PC2 space
4. **Cluster Plots**: Shows clustering results in reduced dimensional space
5. **Dendrogram**: Hierarchical clustering tree structure

## Key Learnings
- PCA effectively reduces dimensionality while preserving variance
- Clustering reveals natural groupings in crime patterns
- Urban density has varying relationships with different crime types
- Standardization is crucial for PCA and distance-based algorithms
- Multiple clustering techniques provide validation and deeper insights

## Author
Patrick Geisinger

## License
This project is part of the Arizona State University bootcamp curriculum.

## Acknowledgments
- Arizona State University for the project guidelines
- R datasets package for the USArrests dataset
- scikit-learn contributors for excellent ML libraries
