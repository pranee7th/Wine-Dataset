The wine dataset is the result of a chemical analysis of wines grown in the same region in Italy but derived from three different cultivars.
( only 2 classes, 0 and 1, will be included for the classification task.) The analysis determined the quantities of 13 constituents found in each of the three types of wines.

The objective is to classify the wines into class 0 or 1 using the 13 given attributes and a decision tree classifier.

Steps Invovled: 

Data Preparation:

The project starts by loading a wine dataset (wine) and creating a pandas DataFrame (X) containing the features and a target variable (y).
The dataset is then subset to include only instances where the target variable is 0 or 1, indicating a binary classification task.

Data Splitting:
The data is split into a training set (70%) and a validation set (30%). This is a common practice in machine learning to train the model on one 
subset and evaluate its performance on another to assess generalization.

Decision Tree Classifier:
A decision tree classifier is fitted to the training set without any pruning. This initial step helps to understand the structure of the tree and its performance on the training data.
Pruning with Cost Complexity:
The decision tree is then pruned using cost complexity. This technique involves adjusting the complexity parameter (alpha) to find the right balance between tree complexity and accuracy.

Alpha Selection:
The code analyzes different alpha values and observes that a high alpha results in more nodes, which may not necessarily improve accuracy.
The best alpha is chosen based on accuracy, and in this case, it's not the alpha with the highest accuracy, as a value of 0 is problematic. Another alpha value (0.02) is chosen, which provides a good trade-off between accuracy and tree complexity.
Graphical Analysis:
Subplots are used to visualize the accuracy of different alpha values graphically. This step helps in making an informed decision about the right alpha value.

Conclusion:
The project concludes by selecting an alpha value (0.02) that offers high accuracy while maintaining a reasonable level of tree complexity.
This alpha value is used for final model training and evaluation.
In summary, the project involves preprocessing a wine dataset, splitting it into training and validation sets, building an initial decision tree, pruning it using cost complexity, and visually analyzing the impact of different alpha values to select the optimal one for achieving a balance between accuracy and simplicity.

Note: This project was part of my Data Mining Course at Northeastern
