The latest source focuses on **String Manipulation** and **Dictionaries**, two essential tools for handling data in Python.

### **1. String Manipulation**
Strings are sequences of characters defined by single (`'`) or double (`"`) quotes. 

*   **Handling Special Characters:** You can use the backslash (`\`) to "escape" characters like quotes or to create newlines (`\n`). Triple quotes (`"""`) allow for multi-line strings without explicit newline characters.
*   **Strings as Sequences:** Like lists, you can index, slice, and use `len()` on strings. However, strings are **immutable**, meaning you cannot change their characters in place. here 
*   **Key Methods:** 
    *   **Case & Search:** `.upper()`, `.lower()`, `.startswith()`, and `.endswith()`.
    *   **Split & Join:** `.split()` breaks a string into a list, while `.join()` sews a list of strings into one.
    *   **Formatting:** The `.format()` method is preferred over `+` concatenation because it automatically handles non-string types and allows for complex formatting (like setting decimal places or adding commas to large numbers).

```python
# String formatting example
"{} weighs about {:.2}kg".format("Pluto", 1.303 * 10**22)
# Output: "Pluto weighs about 1.3e+22kg"
```

### **2. Dictionary Essentials**
Dictionaries map **keys** to **values** using a `{key: value}` syntax.

*   **Access and Updates:** You access or modify values using square brackets `[]`.
*   **Dictionary Comprehensions:** Similar to lists, you can create dictionaries efficiently from iterables.
*   **Iteration:** You can loop over keys (default), `.values()`, or use `.items()` to iterate over both keys and values simultaneously.

```python
# Dictionary iteration
numbers = {'one': 1, 'two': 2}
for k, v in numbers.items():
    print("{} = {}".format(k, v))
```

