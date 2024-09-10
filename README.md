# Decision-Trees
Understanding Decision Trees
# Decision Tree Classifier Implementation

## Project Overview

This project implements a **Decision Tree Classifier** from scratch using Python, applied to the Breast Cancer dataset from `sklearn.datasets`. A decision tree is a widely-used machine learning algorithm that partitions the data into subsets based on the feature values to predict an outcome. The classifier works by recursively splitting the dataset into subgroups to maximize information gain, which helps in making predictions for unseen data.

### Key Features

- **Custom Decision Tree Implementation**: The decision tree algorithm is implemented without using external libraries for machine learning. It includes methods for training (fitting) the model, predicting outcomes, and calculating entropy to evaluate the purity of the splits.
  
- **Breast Cancer Dataset**: The model is applied to the Breast Cancer dataset from `scikit-learn`, which consists of various features used to classify tumors as either malignant or benign.

- **Train-Test Split**: The data is split into training and testing sets to evaluate the performance of the model on unseen data.

### How It Works

1. **Entropy Calculation**: Entropy is a measure of disorder or impurity in a set of labels. The algorithm uses entropy to determine the best split for the data. By minimizing the entropy (or maximizing information gain), the decision tree can create more pure leaf nodes, which enhances the accuracy of predictions.

2. **Node Splitting**: The decision tree works by splitting the dataset into smaller subsets based on different features and their values. It greedily selects the feature and threshold that provide the best split (maximum information gain).

3. **Tree Growth**: The tree grows recursively, with each node being either a leaf node (representing a decision/prediction) or a decision node that leads to further splits. This process continues until certain conditions are met (such as reaching the maximum depth or a minimum number of samples per split).

4. **Making Predictions**: After training the model, predictions are made by traversing the tree from the root to the appropriate leaf node based on the input features. Each leaf node represents the most common label in that subset of the data.

5. **Accuracy**: A custom accuracy function is provided to measure the performance of the decision tree classifier by comparing predicted labels with the actual labels from the test set.

### Project Structure

- **Decision Tree Class**: This class contains the core functionality for fitting the decision tree to the training data, splitting nodes, and making predictions. It also handles calculating information gain using entropy.

- **Node Class**: Represents individual nodes in the decision tree, which can either be a decision node (splits further) or a leaf node (makes a prediction).

- **Accuracy Function**: A function to evaluate the accuracy of the model by comparing the predicted labels against the true labels.

### Results and Performance

The accuracy of the model is tested on the test set (20% of the original data) using the Breast Cancer dataset. The decision tree classifier demonstrates good predictive performance, showcasing the power of decision trees for binary classification tasks like this.

### Conclusion

This project provides an in-depth understanding of how decision trees work by implementing one from scratch. It covers important concepts such as entropy, information gain, and recursive splitting, giving hands-on experience in building a machine learning classifier without relying on high-level libraries like `scikit-learn` for the algorithm itself.
