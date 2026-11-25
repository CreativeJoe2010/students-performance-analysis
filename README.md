# Students Performance: Data Analysis and Machine Learning

An end-to-end beginner data science project exploring student exam performance through data cleaning, exploratory data analysis, visualisation, and introductory machine-learning models.

## Project overview

The notebook investigates:
1. Relationships between maths, reading and writing scores.
2. Differences in average scores by test-preparation status.
3. The distribution of students across the project's grade bands and pass/fail categories.
4. Differences in performance across parental education levels.
5. Differences in performance by gender and subject.
6. Differences in performance across race/ethnicity groups.

It also compares Decision Tree, Random Forest and XGBoost models for:
- **Regression:** predicting students' average scores, evaluated with mean absolute error (MAE).
- **Classification:** predicting the project-defined pass/fail result, evaluated with balanced accuracy.

## Repository structure

```text
students-performance/
├── students_performance.ipynb
├── data/
│   └── students_performance.csv
├── outputs/
│   └── students_performance_cleaned.csv
├── requirements.txt
└── .gitignore
```

The notebook also checks for `students_performance.csv` in the repository root if it is not found in `data/`.

## Getting started

1. Clone or download this repository.
2. Place the source CSV file at `data/students_performance.csv` (or beside the notebook).
3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Launch Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `students_performance.ipynb` and run the cells from top to bottom.

The cleaned dataset is saved automatically to the `outputs/` folder.

## Dataset

The notebook expects a CSV file named `students_performance.csv` with the columns used in the notebook, including `gender`, `race/ethnicity`, `parental level of education`, `lunch`, `test preparation course`, and the three subject score columns.

The file which I downloaded from Kaggle was made by Aman Chauhan and can also be downloaded from this link [Students Performance Dataset](https://www.kaggle.com/datasets/whenamancodes/students-performance-in-exams)

## Notes and limitations

- The grade boundaries and pass mark are defined in the notebook for this analysis; they should not be assumed to represent an official grading system.
- The analysis describes associations and does not establish causation.
- The classification target (`result`) is derived from `average_score`. The score-derived columns are excluded from the model inputs, so the classification experiment uses the remaining categorical information to predict that score-based category.
- The post-tuning cross-validation scores are exploratory: because hyperparameter tuning has already used the training data, they are not a fully independent estimate of generalisation performance.

## Tools used

Python, Jupyter Notebook, pandas, NumPy, Matplotlib, Seaborn, scikit-learn and XGBoost.

## My Own Rating of the Project:
7.5/10
Still have a lot to learn apparently
