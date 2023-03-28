# Soccer_2023_data_cleaning
Steps:
#1- import data 
#2- clean the data


What tools?
Numpy-lists and arrays and multidimentional arrays 
Pandas- data analysis, to check dataframe we can read a csv file in terms of rows and columns
using dataframes


## IMPORTING DATA 
import pandas as pd #to check dataframe we can read a csv file in terms of rows and columns
#using dataframes
df = pd.read_csv('FIFA23_official_data.csv')
df.shape #it is a property not a method, shows the overall data with index
to view datatypes of the 
df.describe()#gives mean,std,max min, all these datas - (method)
df.values #array values of all the data elements, array of diff players in it
## CLEANING DATA
to choose only certain columns
df.columns #headings of the columns
df1= pd.DataFrame(df,columns=['Name','Wage','Value']) #to view the values in respective columns
to convert 
pd.to_numeric(df1['Wage'].replace({'K': '*1e3', 'M': '*1e6'}, regex=True).map(pd.eval))

pd.to_numeric - to convert into int
map - can do operations mentioned in pd.eval with respect to the index 
can do the operations - pd.eval
### Visualizing
https://docs.bokeh.org/en/latest/docs/user_guide/tools.html#hovertool
df1=df1.sort_values(by=["Diff"],ascending=False) # descending with respect to the diff values 
Bokeh libraries- interactive data visualization cursors
Bokeh 
