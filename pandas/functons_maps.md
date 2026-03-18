Summary Functions
Pandas offers several "summary functions" to quickly grasp the characteristics of a dataset:
describe(): This is a type-aware method that provides a high-level overview
. For numerical data, it shows statistics like mean and quartiles, while for string data, it displays unique values and the most frequent entry
.
Statistical Helpers: Functions like mean() calculate averages, while unique() provides a list of all distinct values in a column
.
value_counts(): This method is used to see a list of unique values alongside their frequency in the dataset
.
Mapping and Transformation
Maps are used to transform data from its current format into a new representation
.
map(): This method is used on a Series. It takes a function (often a lambda) that processes a single value and returns a transformed version, resulting in a new Series
.
apply(): This is the equivalent for a DataFrame. It can transform the data by calling a custom function on each row (using axis='columns') or each column (using axis='index')
.
Immutability: A key detail is that map() and apply() do not modify the original data; they return entirely new objects
.
Built-in Operators
For simpler transformations, pandas supports standard Python operators (like +, -, or ==), which are often preferable to maps:
Speed: These operators are faster because they use internal pandas optimisations
.
Vectorization: You can perform operations between a whole Series and a single value (e.g., subtracting a mean from every row) or between two Series of equal length
.
Flexibility: While operators are faster, map() and apply() remain necessary for advanced tasks involving complex conditional logic
