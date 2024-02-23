# Breast Cancer Detection Project

This project aims to classify breast tumors as benign or malignant based on their features extracted from mammography images. The project uses Python and several libraries such as numpy, pandas, matplotlib, and sklearn.

Data

The data used for this project is the cancer.csv file, which contains 569 samples of breast tumors with 32 features each. The features include the mean, standard error, and worst values of 10 different measurements, such as radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, and fractal dimension. The target variable is the diagnosis, which is either M for malignant or B for benign.

The data is loaded and explored using pandas and matplotlib. Some columns, such as Unnamed: 32 and id, are dropped as they are not relevant for the analysis. The diagnosis column is encoded as 1 for M and 0 for B.

Preprocessing

The data is split into features (x) and target (y) variables. The features are normalized by subtracting the minimum value and dividing by the range of each column. This is done to scale the data and reduce the effect of outliers.

The data is then split into training and testing sets, with 85% of the data for training and 15% for testing. The random_state parameter is set to 42 to ensure reproducibility of the results.

Model

The model used for this project is a logistic regression, which is a simple and widely used classifier that predicts the probability of a binary outcome based on a linear combination of features. The model is imported from the sklearn.linear_model module and instantiated with the default parameters. The max_iter parameter is set to 1000000 to avoid convergence warnings.

The model is fitted on the training data and used to make predictions on the testing data. The accuracy of the model is evaluated by comparing the predicted labels with the true labels. The number of misclassified samples and the total number of samples are printed.

Results

The logistic regression model achieved an accuracy of 95.35% on the testing data, which means that it correctly classified 41 out of 43 samples. Only 2 samples were misclassified as benign when they were actually malignant. This is a good result, but it could be improved by using more complex models, such as neural networks or support vector machines, or by using more data or different features.
