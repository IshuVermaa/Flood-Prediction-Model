# Dataset for Kerela rainfall

A file named kerela.csv is attached to the repository which is the dataset used in this project. The fields of the dataset are Subdivision (string), Year(integer), Months(integer), Rainfall(integer), Floods(boolean)

# Setup Environmnt
Click on download zip, and after that unzip the folder. Right click on unzipped folder and select open in terminal. The type the command code . to open this in vscode. 

Create virtual environment: python -m venv myvenv
Activating virtual Environment: myvenv/Scripts/activate

pip install numpy
pip install pandas

In Flood_Prediction.ipynb file, in cell 4, edit this line os.chdir(r'C:/Users/DELL/Downloads/Flood-Prediction-Model-master/Flood-Prediction-Model'). Copy the path of this project folder in your system and paste it here in place of the current path.

After setting up, open Flood_Prediction.ipynb and click on Run All button on the top of the window.
It will run all the cells and will show the desired output. 

# Machine Learning Algorithms used

- This Model uses 5 Machine Learning Algorithms namely : 
- KNN Classification
- Logistic Regression
- Support Vector Machine
- Decision Tree
- Random Forest 

to get the best possible model to predict the floods using Kerela Rainfall Data.
<hr>
