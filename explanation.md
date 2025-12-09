🟦 1. pandas (pd)
✔ Purpose:

Working with datasets in table form.

Load CSV files (like the Titanic dataset).

Clean, filter, and preprocess data.

✔ Why we use it:

The Titanic dataset is a table with rows = passengers, columns = features.
Pandas lets us explore and manipulate it easily.

🟧 2. numpy (np)
✔ Purpose:

Mathematical operations

Handling arrays

Numerical calculations

✔ Why we use it:

Machine learning often involves:

Converting data to numeric forms

Handling missing values

Working with arrays/matrices

🟩 3. matplotlib.pyplot (plt)
✔ Purpose:

Basic plotting and visualization

✔ Why we use it:

To visualize:

Age distributions

Survival rates

Correlation heatmaps

Understanding data visually is a key ML step.

🟪 4. seaborn (sns)
✔ Purpose:

Advanced, prettier visualizations built on matplotlib

Statistical plots

✔ Why we use it:

Great for:

Count plots

Box plots

Heatmaps

Pair plots

You will likely use it to explore which features influence survival.

🟫 5. sklearn.model_selection.train_test_split
✔ Purpose:

Splits data into training and test sets.

✔ Why we use it:

We train the model on one portion of the data and test its performance on unseen data to evaluate accuracy properly.

🟩 6. sklearn.ensemble.RandomForestClassifier
✔ Purpose:

A machine learning model consisting of many decision trees.

Works well even with messy data.

✔ Why we use it:

The Random Forest classifier:

Handles missing values moderately well

Avoids overfitting better than a single decision tree

Works great for Kaggle Titanic competitions

🟧 7. sklearn.metrics

Includes:

✔ accuracy_score

Measures how many predictions were correct.

✔ classification_report

Gives:

precision

recall

F1 score
for each class (survived vs not survived)

✔ confusion_matrix + ConfusionMatrixDisplay

Helps visualize:

true positives

true negatives

false positives

false negatives

A must for classification tasks.

⚠️ 8. warnings.filterwarnings('ignore')

This simply hides warning messages so the notebook looks cleaner.