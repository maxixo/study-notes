Native Python Accessors
Pandas supports standard Python methods for accessing data, which makes it accessible for beginners
.
Attribute Access: You can access a column as a property of the object, such as reviews.country
.
Indexing Operator ([]): This dictionary-like method, reviews['country'], is more flexible because it can handle column names containing spaces or reserved characters
.
Advanced Accessors: iloc and loc
For more complex operations, pandas uses two primary indexing paradigms
. Both are row-first, column-second, which is the reverse of native Python
.
Index-based Selection (iloc): This method selects data based on its numerical position
. It follows the standard Python indexing scheme where the first element is included but the last is excluded (e.g., 0:10 selects entries 0–9)
.
Label-based Selection (loc): This selects data based on index labels rather than position
. Unlike iloc, it is inclusive of the end range (e.g., 0:10 selects 11 entries, including both 0 and 10)
. This is particularly useful when indexing non-numeric labels like strings
.
Filtering and Conditional Selection
You can select data by asking specific questions about its content
.
Logical Filters: Using a statement like reviews.country == 'Italy' generates a Series of booleans that can be passed into loc to filter the DataFrame
.
Combining Conditions: You can use the ampersand (&) for "and" logic and the pipe (|) for "or" logic to create complex filters
.
Built-in Selectors: isin() allows you to select values that appear in a specific list, while isnull() and notnull() are used to find or filter out missing (NaN) values
.
Index Manipulation and Data Assignment
set_index(): This method allows you to replace the default numeric index with a more meaningful column, such as a "title" field
.
Assignment: Adding data to a DataFrame is as simple as assigning a constant value or a list of values to a column name
