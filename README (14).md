Student Performance Analysis
Project Overview
This project analyzes students' academic performance in Mathematics,
Reading, and Writing using Python and data analysis libraries. It
explores score statistics, calculates total and average scores, derives
percentages, classifies students as Pass or Fail, identifies possible
Mathematics score outliers, and visualizes score distributions.
Objectives
- Understand the structure and summary statistics of the dataset.
- Check for missing values.
- Calculate mean, median, mode, standard deviation, and the first
  quartile for subject scores.
- Calculate each student's total score, percentage, and average score.
- Classify students as Pass or Fail using a minimum score of 40 in
  every subject.
- Identify potential Mathematics score outliers using the IQR method.
- Visualize Mathematics score distribution and compare subject scores.
Dataset
The notebook loads a CSV file named StudentsPerformance.csv.

The code expects these columns: - math score - reading score -
writing score

The dataset should also contain any other student-related columns
included in the original CSV. The notebook does not define the dataset's
source or provide a complete data dictionary.
Technologies Used
- Python
- Pandas --- data loading, cleaning checks, calculations, and
  analysis
- NumPy --- numerical computing
- Matplotlib --- plotting
- Seaborn --- imported for visualization (not used in the shown
  notebook cells)
- Jupyter Notebook / Google Colab --- notebook environment
Workflow
1. Import the required libraries.
2. Load StudentsPerformance.csv into a Pandas DataFrame.
3. Inspect the dataset with describe(), info(), head(), and
   tail().
4. Check missing values using isnull().sum().
5. Explore descriptive statistics for Mathematics, Reading, and Writing
   scores.
6. Create the following derived columns:
   - Total Score: sum of the three subject scores.
   - Percentage: total score divided by 300, multiplied by 100.
   - Average Score: mean of the three subject scores for each
     student.
   - Pass/Fail: Pass if all three subject scores are at least
     40; otherwise Fail.
7. Use the interquartile range (IQR) method to identify possible
   outliers in Mathematics scores.
8. Plot a histogram of Mathematics scores and box plots comparing the
   three subjects.
How to Run
1. Download or place StudentsPerformance.csv in your notebook
   environment.
2. Open Untitled12.ipynb in Jupyter Notebook or Google Colab.
3. Update the CSV file path if necessary. The current notebook uses:
   df = pd.read_csv("/content/StudentsPerformance.csv")
4. Run the notebook cells from top to bottom.
Pass/Fail Rule
A student is classified as Pass only when all three scores are 40 or
above: - Mathematics score >= 40 - Reading score >= 40 - Writing score
>= 40

If any one of these scores is below 40, the student is classified as
Fail. This is the rule implemented in the notebook and may differ
from an institution's official grading policy.
Outlier Detection
The notebook calculates the first quartile (Q1), third quartile (Q3),
and interquartile range (IQR) for Mathematics scores. It flags scores
below Q1 - 1.5 × IQR or above Q3 + 1.5 × IQR as potential outliers.
Visualizations
- Histogram of Mathematics scores.
- Box plots for Mathematics, Reading, and Writing scores.
Notes and Limitations
- The CSV file is required to run the notebook; it was not included
  with the uploaded notebook.
- The notebook checks for missing values but does not show a
  missing-value treatment step.
- The notebook identifies potential outliers but does not remove them.
- The notebook calculates statistics and creates plots; it does not
  train a machine-learning model or make predictions.
Conclusion
This project provides a basic exploratory analysis of student scores. It
summarizes performance across three subjects, derives useful academic
measures, applies a simple pass/fail rule, checks for potential
Mathematics outliers, and visualizes score patterns.
