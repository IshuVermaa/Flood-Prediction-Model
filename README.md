# Dataset for kerela rainfall

A file named kerela.csv is attached to the repository which is the dataset used in this project. The fields of the dataset are Subdivision (string), Year(integer), Months(integer), Rainfall(integer), Floods(boolean)

# Setup Environmnt

Create virtual environment: python -m venv myvenv
Activating virtual Environment: myvenv/Scripts/activate

pip install numpy
pip install pandas

After setting up, open Flood_Prediction.ipynb and click on Run All button on the top of the window.
It will run all the cells and will show the desired output. 

# Machine Learning Algorithms used

This Model uses 5 Machine Learning Algorithms namely : 
- KNN Classification
- Logistic Regression
- Support Vector Machine
- Decision Tree
- Random Forest 

to get the best possible model to predict the floods using Kerela Rainfall Data.
<hr>

# Explaining the details of the code

Here's a breakdown of what each section of the code does:

1. Importing modules and filtering warnings:

The code begins by importing the warnings module and using warnings.filterwarnings('ignore') to ignore all warnings.
It also imports the os module for operating system-dependent functionality.

2. Changing the current working directory:

The script uses os.chdir() to change the current working directory to the specified path. This is done to set the project folder where the flood prediction model files are located.
The path provided in the code is C:/Users/DELL/Downloads/Flood-Prediction-Model-master/Flood-Prediction-Model.

3. Importing necessary libraries:

The script imports the numpy library as np for numerical computations.
It imports the pandas library as pd for data processing and CSV file I/O.

4. Loading and analyzing the data:

The script uses pd.read_csv() to read the data from a CSV file named kerala.csv located in the project folder.
It then prints the loaded data using print(data).
Further data analysis is performed using methods like head(), tail(), isnull().sum(), shape, describe(), cov(), and corr().

5. Preprocessing the data:

The script replaces the values 'YES' and 'NO' in the 'FLOODS' column with 1 and 0, respectively, using data['FLOODS'].replace(['YES', 'NO'], [1, 0], inplace=True).
It separates the features (input data) and the flood labels (output data) into variables x and y, respectively.

6. Data visualization:

The script uses the matplotlib.pyplot library to create histograms and bar plots to visualize the data.

7. Scaling the data:

The script uses the preprocessing.MinMaxScaler from sklearn to scale the feature data between 0 and 1.

8. Splitting the dataset into training and test sets:

The script uses train_test_split from sklearn.model_selection to divide the data into training and test sets.

9. Training and evaluating the K-Nearest Neighbors (KNN) classifier:

The script creates a KNeighborsClassifier object, fits it to the training data using fit(), and predicts the flood values for the test data using predict().
It then evaluates the classifier's performance using accuracy, recall, ROC score, and confusion matrix.

10. Training and evaluating other classifiers:

Similar to the KNN classifier, the script trains and evaluates other classifiers such as Logistic Regression, Support Vector Machines (SVM), Decision Tree, and Random Forest.
Cross-validation and performance metrics such as accuracy, recall, ROC score, and confusion matrix are used.

11. Comparing the performance of different classifiers:

The script creates a list of classifier models and iterates over them to train and evaluate each one.
The accuracy scores of each classifier are stored in a pandas DataFrame and visualized using a bar plot.

12. Finding the maximum accuracy score:

The script determines the maximum accuracy score achieved among the different classifiers.


Overall, the code performs various steps involved in building a flood prediction model, including data loading, preprocessing, model training, evaluation, and comparison of different classifiers.
