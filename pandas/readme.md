# What Is Pandas In Python?

Pandas is an open source Python package that is most widely used for data science/data analysis and machine learning tasks. It is built on top of another package named Numpy, which provides support for multi-dimensional arrays. As one of the most popular data wrangling packages, Pandas works well with many other data science modules inside the Python ecosystem, and is typically included in every Python distribution, from those that come with your operating system to commercial vendor distributions like ActiveState’s ActivePython

# What Can You Do With DataFrames Using Pandas?
Pandas makes it simple to do many of the time consuming, repetitive tasks associated with working with data, including:

Data cleansing
Data fill
Data normalization
Merges and joins
Data visualization
Statistical analysis
Data inspection
Loading and saving data

Object creation

Creating a Series by passing a list of values, letting pandas create a default integer index:

# DataFrame.to_numpy() 
gives a NumPy representation of the underlying data. Note that this can be an expensive operation when your DataFrame has columns with different data types, which comes down to a fundamental difference between pandas and NumPy: NumPy arrays have one dtype for the entire array, while pandas DataFrames have one dtype per column. When you call DataFrame.to_numpy(), pandas will find the NumPy dtype that can hold all of the dtypes in the DataFrame. This may end up being object, which requires casting every value to a Python object.



# How do I select specific columns from a DataFrame?

DataFrame.shape is an attribute : (do not use parentheses for attributes,) of a pandas Series and DataFrame containing the number of rows and columns: (nrows, ncolumns). A pandas Series is 1-dimensional and only the number of rows is returned.

# To select multiple columns, use a list of column names within the selection brackets [].

The loc/iloc operators are required in front of the selection brackets []. When using loc/iloc, the part before the comma is the rows you want, and the part after the comma is the columns you want to select.

# Getting data in/out¶
CSV

Writing to a csv file:

HDF5¶

Reading and writing to HDFStores.

Excel

Reading and writing to MS Excel.
