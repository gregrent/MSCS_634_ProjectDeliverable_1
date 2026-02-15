# Advanced Data Mining for Data-Driven Insights and Predictive Modeling
## Deliverable 3: Classification, Clustering, and Pattern Discovery

---

## Dataset Overview

The Titanic dataset was used to perform classification, clustering, and association rule mining. The dataset contains demographic and travel-related information about passengers, such as age, sex, ticket class, fare, and family size. The main predictive task was to determine passenger survival.

---

## Classification Insights

Two classification models were developed: Decision Tree and k-Nearest Neighbors (KNN). Hyperparameter tuning was applied to the Decision Tree model using grid search, which improved its performance.

Key observations:

- The tuned Decision Tree achieved better F1 score and overall accuracy compared to the baseline models.

- Passenger sex, class, and fare were among the most influential features in predicting survival.

- The confusion matrix and ROC curve showed that the model could reasonably distinguish between survivors and non-survivors.

These results demonstrate that relatively simple classification models can effectively capture important survival patterns in the dataset.

---

## Clustering Insights

K-Means clustering was applied using numerical features such as age, fare, passenger class, and family size.

The clustering results revealed distinct passenger groups:

- A cluster representing higher-fare, first-class passengers.

- A cluster consisting of lower-fare, third-class passengers with larger families.

- A middle group with moderate fares and smaller family sizes.

These clusters reflect socioeconomic differences among passengers and help explain variations in survival outcomes.

---

## Association Rule Mining Insights

Association rule mining using the Apriori algorithm identified meaningful relationships among passenger attributes.

Notable patterns included:

- Female passengers were strongly associated with survival.

- First-class passengers had a higher likelihood of survival.

- Male passengers in lower classes were more likely to be associated with non-survival.

These rules reinforce known survival patterns and provide interpretable relationships between passenger characteristics and outcomes.

---

## Practical Relevance and Real-World Applications

The techniques used in this deliverable have broad real-world applications:

- **Classification models** can be used in fraud detection, medical diagnosis, customer churn prediction, and credit risk assessment.

- **Clustering** is useful for customer segmentation, targeted marketing, and anomaly detection.

- **Association rule mining** is commonly applied in market basket analysis, recommendation systems, and behavior pattern discovery.

Together, these methods help organizations make data-driven decisions and uncover hidden patterns in large datasets.

---

## Challenges and Solutions

**1. Handling Categorical Data**
- Many features were categorical (e.g., sex, embarked port).
- **Solution:** One-hot encoding was used to convert categorical variables into numerical form.

**2. Model Performance and Overfitting**
- Initial Decision Tree models risked overfitting.
- **Solution:** Hyperparameter tuning with GridSearchCV was applied to find optimal depth and split parameters.

**3. Association Rule Warnings**
- The Apriori and association rule steps produced runtime warnings due to division-by-zero issues in certain metrics.
- **Solution:** Warnings were safely suppressed since they originated from internal calculations and did not affect the required metrics (support, confidence, lift).

---

## 📁 Repository Contents (for this deliverable)

- `MSCS_634_ProjectDeliverable_3.ipynb` – Complete implementation with code, comments, and visualizations.
- `README.md` – Project summary, classification insights, clustering insights, real-world applications, and challenges and solutions.

---

## Conclusion

This deliverable demonstrated how classification, clustering, and association rule mining can be used together to generate both predictive and descriptive insights. The models confirmed that factors such as passenger class, fare, and sex played major roles in survival, while clustering and association rules revealed meaningful passenger segments and behavioral patterns. These techniques illustrate the power of data mining methods in solving real-world analytical problems.

---