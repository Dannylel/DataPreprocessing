# DataPreprocessing

# The Information :
takes a data frame as an argument and performs an exploratory data analysis. It replaces any missing values with NaN, calculates the percentage of null values and duplicated rows, and determines whether each column is numerical or categorical. It returns a pandas data frame with columns indicating the name of each feature, unique values, number of unique values, data type, number of nulls, and percentage of nulls. Additionally, it prints out the number and percentage of nulls, the number and percentage of duplicated rows, and the numerical and categorical columns with their respective types.

# The ImputeNulls :
takes a data frame and optional dictionaries col_method, col_value, and type_method as arguments. It imputes the missing values in the data frame using the given method for each specified column. If no method is specified for a column, it will use a default method based on the data type of the column. 

# The Outliers :
takes a data frame and optional arguments display, drop, drop_order, columns_to_display, and columns_to_drop. It identifies any potential outliers in the numerical columns of the data frame using a boxplot and histogram. If display is set to True, it displays the boxplot and histogram for each numerical column, either all columns or specified columns using columns_to_display. If drop is set to True, it removes any rows that contain an outlier in at least one of the numerical columns. The drop_order argument specifies the order of the process of removing outliers, either (1) removing rows that contain an outlier in any numerical column first or (2) removing outliers in each numerical column separately first. It returns a new data frame with or without the rows containing outliers, depending on the value of the drop argument. If columns_to_drop is specified, it will only remove outliers in the specified columns.

# Encode Categorical :
This is a method that encodes categorical variables in a pandas dataframe using either one-hot encoding or label encoding. The method takes in several parameters:
df: the pandas dataframe to encode
col_method: a dictionary where the keys are the column names and the values are either "label" or "one_hot", indicating the encoding method to use for each column. If a column is not specified in this dictionary, it will not be encoded.
one_hot: a boolean indicating whether to use one-hot encoding for all categorical columns
labeling: a boolean indicating whether to use label encoding for all categorical columns
default: a boolean indicating whether to use default encoding, which is one-hot encoding for columns with fewer than 20 unique values and label encoding for columns with more than 20 unique values.

# Model :
takes in a DataFrame df, a machine learning model, a target_name, the type of problem (classification or regression), and optional parameters such as test_size and random_state.
The function first splits the data into training and testing sets using train_test_split() from sklearn
Finally, the function prints classification_report and returns the trained model.
