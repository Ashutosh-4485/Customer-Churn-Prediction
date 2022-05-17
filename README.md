**About Dataset**

The dataset is Telco Customer Churn dataset from kaggle

"Predict behavior to retain customers. You can analyze all relevant customer data and develop focused customer retention programs." [IBM Sample Data Sets]

Each row represents a customer, each column contains customer’s attributes described on the column Metadata.

The data set includes information about:

1. Customers who left within the last month – the column is called Churn
2. Services that each customer has signed up for – phone, multiple lines, internet, online security, online backup, device protection, tech support, and streaming TV and movies
3. Customer account information – how long they’ve been a customer, contract, payment method, paperless billing, monthly charges, and total charges
4. Demographic info about customers – gender, age range, and if they have partners and dependents

**Libraries**
1. Pandas
2. Numpy
3. Matplotlib
4. sklearn
5. seaborn
6. tensorflow

**Data Preprocessing **
1. Dropped unwanted columns
2. Converted all data types to int or float.
3. Dropped Null rows.
4. Used One Hot Encoding
5. Trained the Model 

After training the model, the values for precision, recall and f1-score was not satisfying enough.
The dataset was quite unbalanced.


**What is imbalanced data?**

Imbalanced data refers to those types of datasets where the target class has an uneven distribution of observations, i.e one class label has a very high number of observations and the other has a very low number of observations.

**Approach to deal with the imbalanced dataset problem**

1. Choose Proper Evaluation Metric
2. Resampling (Oversampling and Undersampling)
3. SMOTE
4. BalancedBaggingClassifier
5. Threshold moving

I have used SMOTE technique

**3. SMOTE**
 
Synthetic Minority Oversampling Technique or SMOTE is another technique to oversample the minority class. Simply adding duplicate records of minority class often don’t add any new information to the model. In SMOTE new instances are synthesized from the existing data. If we explain it in simple words, SMOTE looks into minority class instances and use k nearest neighbor to select a random nearest neighbor, and a synthetic instance is created randomly in feature space.

**Conclusion **

After applying SMOTE, I trained the model on 
XGBoostClassifier, ANN (with 3 hidden layers over 100 epochs) and SGDClassifier, XGBoost has given the best accuracy of 82%.

