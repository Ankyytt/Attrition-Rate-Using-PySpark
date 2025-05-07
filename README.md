# 🚀 Employee Attrition Analysis using PySpark

This project demonstrates how to apply scalable machine learning techniques using Apache Spark to analyze an employee dataset. It includes feature engineering, dimensionality reduction, clustering, and classification tasks, all powered by PySpark in a Google Colab environment.

---

## 📁 Dataset

The dataset used is `employees.csv`, which includes the following features:

- `Emp_Name`: Employee name
- `Age`: Employee age
- `Salary`: Monthly salary
- `Department`: Department of the employee

We also generate a synthetic **Attrition** label to simulate employee turnover for classification.

---

## 🧰 Technologies Used

- Python 3.x
- Apache Spark 3.4.1
- PySpark (Spark MLlib)
- Google Colab
- Pandas, Matplotlib (for minor tasks)

---

## 🔍 Project Workflow

1. **Environment Setup**
   - Installed Spark and Java in Colab
   - Configured SparkSession

2. **Data Preprocessing**
   - Loaded CSV into Spark DataFrame
   - Indexed categorical variables (`Department`)
   - Assembled numerical and categorical features into vectors

3. **Dimensionality Reduction**
   - Applied PCA (Principal Component Analysis) to reduce features to 2D

4. **Clustering**
   - Used KMeans to group employees into 3 clusters based on PCA features

5. **Feature Engineering**
   - Created a new `Attrition` column based on salary threshold

6. **Classification**
   - Applied and evaluated:
     - Naive Bayes
     - Gradient Boosted Trees
   - Split data into training and testing sets
   - Used AUC (Area Under Curve) for model evaluation

---

## 📈 Results

| Model             | Metric Used | AUC Score     |
|------------------|-------------|---------------|
| Naive Bayes      | ROC AUC     | 1.0 |
| GBT Classifier   | ROC AUC     | 0.9533 |

- Clustering helped visualize natural employee groupings
- GBT outperformed Naive Bayes in predictive performance

---

## 💡 Key Takeaways

- Spark MLlib provides a powerful pipeline structure for large-scale ML.
- Dimensionality reduction using PCA aids in understanding high-dimensional data.
- The project shows how scalable ML workflows can be executed in environments like Colab using PySpark.

---

## 📎 How to Run

1. Open the `AttritionRate..ipynb` notebook in Google Colab.
2. Upload the `employees.csv` file.
3. Run all cells step-by-step (first-time Spark setup may take a few minutes).
4. Modify or expand the notebook as needed.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 🤝 Acknowledgments

- Apache Spark Documentation
- Google Colab
- PySpark MLlib Guide
