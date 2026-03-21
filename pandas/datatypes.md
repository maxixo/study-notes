 "Data Types and Handling Missing Values," explains how pandas categorises information and provides tools for cleaning incomplete datasets.
Understanding Data Types (Dtypes)
The "dtype" represents how pandas stores data internally
.
Common Types: You will frequently see float64 (64-bit floating point numbers) and int64 (integers)
.
The Object Type: A unique quirk of pandas is that columns consisting entirely of strings are given the object type rather than a specific "string" type
.
Inspecting and Converting: You can use the .dtype property for a single column or .dtypes to see the types for an entire DataFrame
. If you need to change a column's type—for example, converting integers to decimals—you can use the astype() function
.
Managing Missing Data
In pandas, missing values are labeled as NaN ("Not a Number")
.
Technical Note: For technical reasons, NaN values are always stored as the float64 dtype
.
Detection: To find these missing entries, you use pd.isnull() (or its counterpart pd.notnull())
. This is often used to filter a DataFrame to see only the rows with missing information
.
Replacing and Filling Values
There are two primary methods for dealing with missing or incorrect data:
fillna(): This is used to replace NaN values. You can fill them with a specific placeholder, such as "Unknown," or use a strategy like "backfill," which fills the gap with the first non-null value that appears after the missing record
.
replace(): This is a versatile tool for swapping out specific values. It is often used to update data (like a user's changed social media handle) or to replace "sentinel" values—placeholders like "Invalid" or "Undisclosed"—that aren't technically NaN but still represent missing data
.