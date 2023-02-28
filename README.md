# Traffic_accident_Severity_Classification_with_Pyspark

Create_undersampled_data: 
  -Data preprocessing
   -Handles null values (filling na, dropping rows and dropping columns)
   -Randomizes the dataset and splits by severity into 4 CSV files.
   -These are imported in Work_final_balanced with a 5000 limit, balancing the labels equaly. 
   -Randomizing before repartition is important for diversity in date, city, state,... 


Link to the original [Dataset](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents).

