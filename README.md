# Iris-Flower-Classification
# If the ipynb file is not opening or showing error on web try to download it and open it , it will work .
Iris Flowers Classification : Predict the different species of flowers on the length of there petals and sepals
This notebook trains a Random Forest classifier on the Iris dataset to predict the species of Iris flowers. The classifier achieves an accuracy of 97.33% on the test set.

To run the code in this notebook, simply click the "Run" button for each cell.

The predicted species is the species of Iris flower that the classifier predicts for the given data point. The feature importances plot shows which features are most important for the classifier's predictions.

Example Usage
To predict the species of a new Iris flower with sepal length 5.1 cm, sepal width 3.5 cm, petal length 1.4 cm, and petal width 0.2 cm, you can use the following code:

python
import pandas as pd
from sklearn.ensemble import RandomForestClassifier

Load the Iris dataset from a CSV file
iris_df = pd.read_csv("Iris.csv")

Separate features and target variable
X = iris_df.drop("species", axis=1)
y = iris_df["species"]

Train a Random Forest classifier
clf = RandomForestClassifier(n_estimators=100, random_state=42)
clf.fit(X, y)

Now you can make predictions for new data
new_data = pd.DataFrame({
  "sepal length (cm)": [5.1],
  "sepal width (cm)": [3.5],
  "petal length (cm)": [1.4],
  "petal width (cm)": [0.2]
})

predicted_species = clf.predict(new_data)
print(f"Predicted species: {predicted_species[0]}")


This code will predict that the species of the new Iris flower is **Setosa**.
You can save the README file by clicking the "File" menu and selecting "Save". The README file will be saved in the same directory as the notebook.

I hope this helps!
