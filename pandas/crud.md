Pandas is the primary library for data analysis in Python
. To start using it, you first need to import it, typically using the alias pd
.
Creating Data from Scratch
There are two fundamental objects in pandas: the DataFrame and the Series
.
DataFrame: Think of this as a table or a spreadsheet. It consists of an array of individual entries where each value belongs to a specific row (record) and column
. You can create one using a dictionary where the keys are your column names and the values are lists of your data
. While pandas defaults to numeric row labels (0, 1, 2...), you can assign custom labels, known as an Index, using the index parameter
.
Series: This is a sequence of data values, similar to a list or a single column in a table
. While a Series has an overall name, it does not have individual column names like a DataFrame
. Interestingly, a DataFrame is essentially just a collection of Series "glued together"
.
Working with Existing Files
In real-world scenarios, you will usually load data from external files like CSVs (Comma-Separated Values), which are tables where data is separated by commas
.
Loading: Use pd.read_csv() to bring your file into a DataFrame
.
Inspecting: After loading, you can use .shape to see the dimensions (rows and columns) or .head() to view the first five rows of your data
.
Customising Imports: The read_csv function has over 30 parameters
. For example, if your file already contains an index, you can use index_col=0 to tell pandas to use that column instead of creating a new one
