# Traffic_accident_Severity_Classification_with_Pyspark

1. Create_undersampled_data
   - Data pre-processing
     - Handles null values (filling na, dropping rows and dropping columns)
     - Randomizes the dataset and splits by severity into 4 CSV files.
     - These are imported in Work_final_balanced with a 5000 limit, balancing the labels equally.
     - Randomizing before repartition is important for diversity in date, city, state, ... 
2. WorkFinal_balanced
   - Data pre-processing
     - Initiate Label Indexer and OneHotEncoder classes of pyspark.ml.feature library (transform categorical features into numerical representations) 
     - Initiate a Vector Assembler class of pyspark.ml.feature library (combining the columns into a single column)
     - Build a pipeline with Label Indexer, OneHotEncoder, and Vector Assembler.
     - Fit the data on the pipeline and transform the data. 
   - Machine Learning models
     - Train a logistic regression model, decision tree classifier, and random forest classifier
     - Perform Hyperparameter tunning for Logistic regression and Decision tree classifier
   - Evaluate the models
     - Evaluate the models using True positive rate per label, False Positive rate per label, and F Measure per label
     - Evaluate the model using F1 Score, True positive rate, False positive rate, Precision, Recall, and Hamming Loss 
3. Visualizations accidents 2016-2021
   - Tableau visualizations of the data 
      - Top 5 cities with most accidents 
      - Total number of accidents per Year, Month, and Weekday
      - Number of accidents per weather condition and temperature in Celsius 
      - Impact of road elements in the number of accidents 
      - Dynamic time series visualization of number of accidents per month in each state

Link to the original Dataset: [US Accidents (2016 - 2021)](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents).
![image](https://github.coventry.ac.uk/storage/user/2980/files/e59f907c-7450-44ce-b9a5-19a67aa2f608)
