# Advanced Data Mining for Data-Driven Insights and Predictive Modeling
## Deliverable 4: Final Insights, Recommendations, and Presentation

---

## Dataset Summary

This project uses the Titanic dataset, which contains passenger information such as age, gender, class, fare, family relationships, and survival status. The dataset is commonly used for classification problems because it contains both numeric and categorical features that influence survival outcomes.

Data preparation included handling missing values, removing duplicates, and dropping the Cabin column due to excessive missing entries. Categorical variables such as Sex and Embarked were converted into numeric form using one-hot encoding. Additional features were created, including FamilySize and IsAlone, to better capture passenger relationships and social structure on board.

---

## Project Steps
### 1. Data Preparation
- Loaded the Titanic dataset.
- Filled missing Age values with the median.
- Filled missing Embarked values with the mode.
- Dropped the Cabin column due to high missingness.
- Removed duplicate records.
- Applied one-hot encoding to categorical variables.
- Engineered new features: FamilySize and IsAlone.

### 2. Classification
Two classification models were used to predict passenger survival:
- Decision Tree
- k-Nearest Neighbors (KNN)

Steps included:
- Splitting the dataset into training and testing sets.
- Scaling features for distance-based models.
- Training both models and evaluating performance using accuracy and F1 score.
- Performing hyperparameter tuning on the Decision Tree using GridSearchCV.
- Evaluating models using confusion matrices and ROC curves.

### 3. Clustering
K-Means clustering was applied to identify natural passenger groups using:
- Age
- Fare
- FamilySize
- Passenger class (Pclass)

The elbow method was used to determine the optimal number of clusters, and PCA was applied to visualize the clusters in two dimensions.

### 4. Association Rule Mining
The Apriori algorithm was used to discover patterns between:
- Survival status
- Passenger class
- Gender
- Embarkation port

Frequent itemsets were generated, and association rules were extracted using confidence and lift metrics.

---

## Major Findings
### Classification Results
- The KNN model achieved the highest accuracy and F1 score among the tested models.
- Hyperparameter tuning significantly improved the Decision Tree’s performance.
- Feature importance analysis showed that gender, passenger class, and fare were the strongest predictors of survival.

### Clustering Insights
Three main passenger groups were identified:
- Lower-class passengers with lower fares and smaller families.
- Higher-class passengers with higher fares.
- Younger passengers with larger family groups.

Survival rates differed across clusters, confirming that the segmentation represented meaningful passenger profiles.

### Association Rule Insights
- Male passengers were strongly associated with lower survival outcomes.
- First-class and female passengers were more likely to survive.
- Certain embarkation ports were linked with specific passenger classes and survival trends.

---

## 📁 Repository Contents (for this deliverable)

- `MSCS_634_ProjectDeliverable_4.ipynb` – Complete implementation with code, comments, visualizations, and insights.
- `README.md` – Project summary, classification insights, clustering insights, real-world applications, and challenges and solutions.

---

## Conclusion

This project demonstrated how multiple data mining techniques can be used together to generate both predictive and descriptive insights. Classification models showed that KNN provided the best performance for predicting survival, while the tuned Decision Tree offered strong interpretability through feature importance analysis.

Clustering revealed natural groupings among passengers, highlighting how factors such as class, fare, and family size influenced survival outcomes. Association rule mining further exposed relationships between passenger characteristics and survival patterns.

Overall, the combined use of classification, clustering, and association rules provided a comprehensive understanding of the dataset and illustrated how different data mining techniques can complement each other in real-world predictive and exploratory analysis.

---