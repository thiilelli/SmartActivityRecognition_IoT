# SmartActivityRecognition_IoT

#Code Description

This code, inspired by the research conducted by G. Singla, D. Cook, and M. Schmitter-Edgecombe in their paper titled "Recognizing independent and joint activities among multiple residents in smart environments" (Ambient Intelligence and Humanized Computing Journal, 2009), performs various data preprocessing and modeling tasks on a dataset in a smart environment.

This project was carried out as part of an IoT module project.

#Dependencies

The code imports necessary libraries such as pandas, numpy, os, matplotlib.pyplot, torch, and sklearn to handle data manipulation, visualization, and machine learning tasks.

#Data Processing

The code begins by defining the folder path where the dataset is located.
It reads multiple CSV files from the specified path and concatenates them into a single DataFrame called combined_df.
Rows with values in the 'ResidentID3' and 'TaskID3' columns, which are not needed, are removed.
Data cleaning and formatting operations are performed on the 'Date' and 'Time' columns of the DataFrame.
The DataFrame is further filtered based on valid 'SensorID' values.
Time features are encoded cyclically to capture their cyclical nature.
The 'SensorID', 'ResidentID', 'TaskID', and 'Value' columns are encoded using one-hot encoding.
Unnecessary columns and rows are dropped from the DataFrame.
Model Training and Evaluation
The data is split into training and testing sets for model evaluation, with a set random seed for reproducibility.
A list of model configurations is defined to be used for training.
Neural network models with different hidden layer configurations are trained and evaluated using the defined configurations.
