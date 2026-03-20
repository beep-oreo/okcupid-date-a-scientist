# OKCupid: Date-A-Scientist

## 1. Scoping Philosophy
Following the **Data Science for Social Good (DSSG)** framework, this project is designed to be **Problem-Centric**, not just Data-Centric.

* **Data-Centric approach (Avoid):** "I have 60,000 OKCupid profiles, let's make some random charts."
* **Problem-Centric approach (This Project):** "I want to see if STEM professionals have distinct lifestyle patterns so we can predict career paths from social data."

### Screening Criteria
* **Impactful:** It explores social behavior and professional identity in the digital dating age.
* **Solvable:** We have access to the `profiles.csv` dataset with ~60,000 entries.
* **Actionable:** A dating app could use these insights to improve "career compatibility" matching algorithms.

## 2. The 5-Step Iterative Process
| Step | Meaning | OKCupid Application |
| :--- | :--- | :--- |
| **0. Problem** | Context & Gaps | Who are these users? Why do we care about their jobs? |
| **1. Goals** | Measurable outcomes | Increase the Accuracy of predicting a "Scientist" label. |
| **2. Actions** | What do we do? | Flag profiles as "Likely STEM" for recommendation engines. |
| **3. Data** | Internal/External | Use `profiles.csv` and internal profile attributes. |
| **4. Analysis** | Type of Math | **Prediction:** Using Classifiers (SVM/KNN) to predict `job`. |

## 3. Analysis Types
This project utilizes three specific types of analysis:
* **Description:** Identifying the percentage of users in engineering vs. other fields using `.value_counts()`.
* **Detection:** Identifying potential anomalies or "outlier" profiles in the dataset.
* **Prediction:** Using religion, diet, and habits to predict if a person is a scientist.

## 4. The "Trade-off" Conversation
We must decide which errors are more acceptable in our model:
* **False Positive:** Predicting someone is a scientist when they are an artist. (Low cost, might indicate shared hobbies).
* **False Negative:** Missing a real scientist and labeling them "other." (Higher cost if the goal is specialized matching).

> **Equity Note:** We aim to balance these errors across demographic groups (gender, race, age) to ensure the model isn't biased (e.g., ensuring high accuracy for all genders, not just one).

## 5. Evaluation & Output
* **Metrics:** Accuracy, Precision, Recall, and Confusion Matrix.
* **Validation:** 80/20 Train-Test split.
* **Deliverable:** A predictive classifier and a statistical profile of the "Average Scientist."
