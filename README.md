# OKCupid: Date-A-Scientist

🔬 Project Overview: Date-A-Scientist
Goal: Can we predict if an OKCupid user works in a STEM field based solely on their lifestyle markers (Age, Diet, Religion, and Education)?

🚀 Key Findings
The Model: After testing K-NN, Naive Bayes, and Lasso Regression, an Optimized SVM (RBF Kernel) emerged as the winner.

The Metric: Achieved an F1-Score of 0.4371 and a robust ROC-AUC, proving that lifestyle "clusters" are significant predictors of career paths in the SF Bay Area.

The Insight: STEM professionals exhibit non-linear behavioral patterns—meaning their identity isn't just about one trait (like education), but a complex "vibe" of combined lifestyle choices.

🛠️ Tech Stack
Python | Pandas | Scikit-Learn | Matplotlib | Seaborn

Advanced Techniques: GridSearchCV Hyperparameter Tuning, Multi-task Lasso Feature Selection, and SMOTE-style Class Balancing.

## 🏗️ Project Scope
### 1. Project Goals
* **Primary Objective:** To develop a machine learning model that can accurately classify whether an OKCupid user works in a STEM (Science, Technology, Engineering, Math) field based on their profile data.
* **Secondary Objective:** To identify the key "lifestyle markers" (religion, diet, drinking habits, etc.) that are most strongly correlated with individuals in scientific professions.

### 2. Data
* **Source:** The `profiles.csv` dataset, which contains ~60,000 anonymized entries from OKCupid.
* **Key Features:** age, status, sex, orientation, diet, drinks, drugs, education, job, and religion.
* **Preprocessing:** Handle missing values (NaNs), convert categorical text into numerical data (One-Hot Encoding), and normalize continuous variables like age.

### 3. Analysis
* **Exploratory Data Analysis (EDA):** Use Matplotlib and Seaborn to visualize the distribution of scientists across age groups and education levels.
* **Feature Engineering:** Create a label column where 1 represents a "Scientist" (science/tech/eng) and 0 represents all other professions.
* **Model Selection:** Compare the performance of three algorithms:
    * K-Nearest Neighbors (K-NN)
    * Multinomial Naive Bayes
    * Support Vector Machines (SVM)

### 4. Evaluation
* **Metrics:** We will use a Confusion Matrix, Accuracy, Precision, and Recall to determine how well the model identifies scientists without misclassifying others.
* **Validation:** Split the data into 80% Training and 20% Testing sets.

### 5. Output
* A predictive model capable of taking a new "blind" profile and guessing the user's career path.
* Visual insights (graphs) showing the "Average Scientist Profile" vs. the "General User Profile."

---

## 🧠 Scoping Philosophy & Methodology
Following the **Data Science for Social Good (DSSG)** framework, this project is designed to be **Problem-Centric**, not just Data-Centric.

### The Core Philosophy
* **Data-Centric approach:** "I have 60,000 OKCupid profiles, let's make some random charts."
* **Problem-Centric approach:** "I want to see if STEM professionals have distinct lifestyle patterns so we can predict career paths from social data."

### Screening Criteria
* **Impactful:** It explores social behavior and professional identity in the digital dating age.
* **Solvable:** We have access to the `profiles.csv` dataset with ~60,000 entries.
* **Actionable:** A dating app could use these insights to improve "career compatibility" matching algorithms.

### Analysis Types & Trade-offs
This project utilizes **Prediction** (Using Classifiers to predict `job`) and **Description** (Identifying the percentage of users in engineering fields).

**The "Trade-off" Conversation:** * **False Positive:** Predicting someone is a scientist when they are an artist. (Low cost).
* **False Negative:** Missing a real scientist and labeling them "other." (Higher cost for niche matching).
* **Equity Note:** We aim to balance errors across demographic groups (gender, race, age) to ensure the model isn't biased.

🏁 Conclusion: The "Date-A-Scientist" Outcome
1. What was the Problem?
The goal was to determine if an individual’s professional identity (STEM vs. Non-STEM) is reflected in their lifestyle choices on a dating platform. Can we accurately "map" a scientist based only on their age, diet, religion, and education?

2. What Action did we take?
We implemented a multi-stage Machine Learning pipeline:

Exploratory Data Analysis: Visualized the distributions of age and lifestyle markers across 60,000 profiles.

Feature Engineering: Cleaned and encoded categorical data to handle "noisy" social inputs.

Model Selection: Compared K-Nearest Neighbors, Multinomial Naive Bayes, and Lasso Regression.

Optimization: Finalized the project with a Support Vector Machine (SVM), using GridSearchCV to find the optimal non-linear boundary (RBF Kernel, C=0.1).

3. What are the Results?
The optimized SVM achieved an F1-Score of 0.4371.

The Insight: The RBF kernel's success confirms that "Scientists" exist in complex socio-demographic clusters rather than following simple, linear trends.

The Reality: While the model is significantly better than random guessing, the 0.43 score highlights that career labels do not strictly define personal lifestyle. In the San Francisco dating scene, individuality often outweighs professional categorization.

4. Final "Social Good" Action
This model serves as a reminder that while data can find patterns in how we live, it cannot fully predict the complexity of a human being. We recommend using these insights for suggestive matchmaking (helping like-minded people find each other) rather than deterministic labeling (stereotyping users based on their data). 






