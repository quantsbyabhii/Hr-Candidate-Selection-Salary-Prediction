# HR Candidate Selection & Salary Prediction System

A supervised machine learning project built in Python that automates two key HR recruitment decisions based on candidate evaluation metrics:
1. **Hiring Status Prediction:** Determines whether a candidate should be **Selected** or **Rejected**.
2. **Salary Estimation:** Predicts the **Offered Salary (in Lakhs)** for candidates who are selected.

---

## 📊 Dataset Overview

The models are trained on `hr_hiring_dataset.csv` (1,000 candidate records across 17 columns).

### Input Features (15)
* **Interview Rounds:** `Round_1_Score`, `Round_2_Score`, `Round_3_Score` (out of 100)
* **Assessments & Ratings:** `Technical_Skills_Score` (0–100), `Aptitude_Score` (0–100), `Communication_Rating` (1–5), `Interview_Feedback_Rating` (1–5)
* **Background & Qualifications:** `Degree` (`B.Sc`, `B.Tech`, `M.Tech`, `MBA`, `MCA`), `University_Tier` (`Tier 1`, `Tier 2`, `Tier 3`), `Certifications_Count` (0–5), `Experience_Years` (0–15)
* **Job & Compensation Details:** `Job_Position` (`Data Analyst`, `Data Scientist`, `DevOps Engineer`, `HR Specialist`, `Software Engineer`), `Previous_Salary_Lakhs`, `Expected_Salary_Lakhs`, `Notice_Period_Days` (0, 15, 30, 60, or 90)

### Target Variables (2)
* **`Status`:** Categorical (`Selected` / `Rejected`)
* **`Offered_Salary_Lakhs`:** Continuous numerical value

---

## 🧠 Machine Learning Approach

* **Data Preprocessing:** Categorical features (`Degree`, `Job_Position`, `University_Tier`, and `Status`) are converted into numerical format using `LabelEncoder`.
* **Classification Model (`DecisionTreeClassifier`):** Trained to classify candidates into `Selected` (`1`) or `Rejected` (`0`).
* **Regression Model (`DecisionTreeRegressor`):** Trained to predict the exact compensation package (`Offered_Salary_Lakhs`) when a candidate is selected.

---

## 🛠️ Tech Stack & Libraries

* **Python 3**
* **Pandas & NumPy** – Data manipulation and analysis
* **Scikit-Learn** – Label encoding and Decision Tree modeling
* **Jupyter Notebook** – Interactive development and CLI prediction

---

## 🚀 How to Run

1. **Clone or download** this repository and ensure `hr_hiring_dataset.csv` is in the same directory as the notebook.
2. **Install dependencies** (if not already installed):
   ```bash
   pip install pandas numpy scikit-learn jupyter
   ```
3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
4. Open the notebook (`Project Source Code (Python).ipynb`) and run all cells.
5. In the final cell, enter the candidate's scores and details when prompted to get an instant hiring decision and salary recommendation.


