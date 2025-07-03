# Wholesale-Customers-Decision-Tree-Classifier
## Objective 
The goal of this project is to classify wholesale customers into two categories — HORECA (Hotel/Restaurant/Cafe) and Retail — based on their annual spending across six product categories. This classification was achieved using a Decision Tree Classifier.

## Dataset used
-	<a href="https://github.com/SelvaTharsan/Wholesale-Customers-Decision-Tree-Classifier/blob/main/Wholesale%20customers%20data.csv"> Dataset </a>
- Dataset: Wholesale Customers Data
- Source: UCI Machine Learning Repository
- Features:
       - Fresh, Milk, Grocery, Frozen, Detergents_Paper, Delicassen
	     - Channel (1 = HORECA, 2 = Retail)
	     - Region (1 = Lisbon, 2 = Oporto, 3 = Other Region)

## Questions (KPIs)
-	Which product spending categories are the most important for identifying customer channels?
-	Are Retail customers more likely to spend heavily on certain categories (e.g., Grocery or Detergents_Paper)?
-	Can we visualize patterns that clearly differentiate HORECA and Retail customers?
-	What is the accuracy of the Decision Tree model?



##  Exploratory Data Analysis (EDA)
-	Scatter Plot: Retail customers showed higher spending on Grocery and Detergents_Paper.
-	Histograms: Spending distributions are highly skewed.
-	Correlation Heatmaps: Strong correlation observed between Grocery and Detergents_Paper.
-	Bar Charts: Total and average spending by Channel helps highlight product preferences.

## Feature Selection
- Dropped Channel (target) and Region (less relevant).
-	Focused on:
      - Fresh, Milk, Grocery, Frozen, Detergents_Paper, Delicassen
-	Visual analysis supported the choice of features that strongly correlated with Channel (e.g., Grocery, Detergents_Paper, Milk).

## Model Building & Training
-	Used DecisionTreeClassifier from sklearn.
-	Split dataset into 80% training and 20% testing.
-	Achieved accuracy of ~84%.
-	Model trained on the selected features and target Channel (HORECA vs. Retail).

## Model Evaluation
- Classification Report:
         - High precision and recall, especially for HORECA (Channel 1).
- Confusion Matrix:
         - Minimal misclassification between the two customer types.
- Decision Tree Visualization:
         - Key splits were made based on Grocery, Milk, and Detergents_Paper.



##  Conclusion
-	The Decision Tree successfully identified critical spending patterns that distinguish HORECA and Retail customers.
-	Visuals (heatmaps, bar charts, 3D plots) helped inform feature selection.
-	The model is interpretable, making it valuable for non-technical business stakeholders to understand customer behavior.




