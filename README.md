# FlightPatternsAnalysis
This project explores the application of pattern mining algorithms—specifically Apriori and FP-Growth—to identify frequent flight patterns in airline data. These patterns are used to enhance the interpretability and predictive performance of a Random Forest model, with a focus on airline type classification.

Project Overview
Goal: Discover frequent flight patterns and use them to improve the prediction of airline types.

Techniques Used: Pattern mining (Apriori, FP-Growth), Feature Engineering, Random Forest Classifier.

Dataset: Real-world flight data sourced from Kaggle with features like airline, flight code, departure/arrival times, class, duration, stops, and ticket price.

Key Steps
1. Data Preprocessing
One-hot encoding for categorical variables.

Binning and encoding continuous variables (Duration, Price, Days Left).

Transformation of the dataset into binary format for compatibility with pattern mining algorithms.

2. Pattern Mining
Algorithms: Apriori and FP-Growth.

Patterns were discovered using varying minimum support thresholds.

High-confidence and statistically significant patterns were extracted, especially for the dominant airline "Vistara".

3. Feature Engineering
Discovered frequent itemsets and rules were integrated into the dataset as new features.

These pattern-based features aimed to enrich the dataset and provide model explainability.

4. Predictive Modeling
Random Forest Classifier used to predict the airline type.

Model trained on various feature combinations (categorical, continuous, Apriori-derived).

Evaluation metrics: Accuracy, Precision, Recall, F1-score.

Results
Feature Set	Accuracy
Apriori Features Only	0.2700
Categorical Features Only	0.5840
Continuous Features Only	0.7500
Categorical + Continuous	0.9620
Continuous + Apriori Features	0.8300
Categorical + Apriori Features	0.5840
Categorical + Continuous + Apriori	0.9627

The highest accuracy was obtained using the full feature set.

Apriori-derived features improved model explainability, revealing associations like:

Business class + 1 stop → Vistara

Evening arrival + 1 stop → Vistara

Medium price + short duration + 1 stop → Vistara

Conclusion
While the Apriori-derived features had limited impact on raw predictive performance, they significantly contributed to the interpretability of the model. This highlights the value of combining traditional machine learning with pattern mining for real-world airline data analytics.

Requirements
Python 3.8+

pandas, numpy, mlxtend, scikit-learn, matplotlib, seaborn

Developers
Sena Ezgi Anadollu

About the Project
This project was developed as part of a Data Mining course. The development was completed in August 2024.
