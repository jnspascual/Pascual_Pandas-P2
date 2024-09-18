**##ECE 2112: ADVANCED COMPUTER PROGRAMMING AND ALGORITHMS**

**EXPERIMENT 3**

**PYTHON DATA ANALYSIS (PANDAS)**

Pascual, Jasmine Nicole S.

2ECE-B

September 17, 2024

**I. Intended Learning Outcomes:**

1. To identify the codes and functions incorporated in the Pandas library
2. To be able to apply and use the different codes and functions in creating a Python program using a Pandas library

**II. Instructions:**

Write a Python script/code in the Jupyter Notebook to do the given problems. 
You may submit your Jupyter notebook in the dedicated submission bin.

For this programming assignment. download the following file and save to your default user folder:
http://bit.ly/Cars_file
##
**PROBLEM 2**
Save your file as Surname_Pandas-P2.py

Using the dataframe cars in problem 1, extract the following information using subsetting, slicing and indexing operations.

a. Display the first five rows with odd-numbered columns (columns 1, 3, 5, 7 ...) of cars.

b. Display the row that contains the 'Model' of 'Mazda RX4'.

c. How many cylinders ('cyl') does that car model 'Camaro Z28' have?

d. Determine how many cylinders ('cyl') and what gear type ('gear') do the models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have.

**Python code:**

      import pandas as pd _#Access the Pandas library_ 
      
      cars = pd.read_csv('cars.csv') _#Load the .csv file into a DataFrame called 'cars'_
      
      cars _#Display the DataFrame 'cars'_
      
      odd_columns = cars.iloc[:, ::2]  _#Check all the rows in the DataFrame and select columns which are odd numbered, and assign it to odd_columns_
      
      print("Here are the first five rows with odd-numbered columns:") _#Present a statement introducing the first 5 rows with odd-numbered columns of the DataFrame_
      
      print(odd_columns.head()) _#Display the first 5 rows of the DataFrame 'cars'_
      
      mazdarx4_row = cars[cars['Model'] == 'Mazda RX4'] _#Check for the Model of the Mazda RX4 and assign it to a mazdarx4_row_ 
      
      print("Row containing the Model of Mazda RX4:") _#Present a statement introducing the Model of Mazda RX4_
      
      print(mazdarx4_row) _#Display the row containing the Model of Mazda RX4_
      
      camaroz28_cylinders = cars[cars['Model'] == 'Camaro Z28']['cyl'].iloc[0] _#Starting at 0 index, check for the Model of Camaro Z28, then its cylinder, and assign it to camaroz28_cylinders_
      
      print(f"Number of cylinders in Camaro Z28: {camaroz28_cylinders} cylinders") _#Display the number of cylinders of the Camaro Z28_
      
      target_models = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic'] _#Generate a DataFrame containing the selected cars, and assigning it to target_models_
      
      info = cars[cars['Model'].isin(target_models)][['Model', 'cyl', 'gear']] _#Check for the details of these cars, selecting specific information, and assigning it to info_
      
      print("Cylinders and gear type for the selected models:") _#Present a statement introducing the cylinders and gear type for the selected models_
      
      print(info) _#Display the DataFrame_

##

**Progress Tracker:**

September 17, 2024: Created the repository, created the Python code for Problem 2, and submitted in Canvas
September 18, 2024: Edited the code
