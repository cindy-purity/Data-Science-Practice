# DataFrame-Series
selecting rows and columns using pandas
import pandas as pd

# Inspecting and reading data in csv file
df = pd.read_csv(r'C:\Users\Peter\Desktop\DataFrame\survey_results_public.csv')  # use r if error occurs
print(df.head(10))   # To view first 10 rows
print(df.tail(10))   # To view last 10 rows

schema_df = pd.read_csv(r'C:\Users\Peter\Desktop\survey_results_schema.csv')   # use r if error occurs
print(schema_df)

# Selecting Rows and Columns
print(df.columns)  # use .columns to see what columns are available
print(df['EdLevel'])  # To access the column EdLevel
print(df['EdLevel'].value_counts())  # Use .value_counts to count no of people for each education level
print(df['EdLevel'])
print(df.loc[0])  # To access the first the firs row
print(df.loc[0, 'EdLevel'])
print(df.loc[0:2,  'EdLevel':'LearnCodeCoursesCert'])   # To get the first three respones of column EdLevel to LarnCodeCoursesCert
