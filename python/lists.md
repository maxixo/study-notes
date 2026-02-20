. Lists: Ordered and Mutable Sequences
Lists are created using square brackets [] and can contain any mix of data types, including other lists.
• Indexing: Python uses zero-based indexing. list is the first element, and list[-1] is the last.
• Slicing: You can extract portions of a list using list[start:stop]. For example, planets[:3] retrieves the first three planets.
• Mutability: Unlike many other types, lists are "mutable," meaning you can change them "in place".
planets = ['Mercury', 'Venus', 'Earth', 'Mars']
planets[3] = 'Malacandra' # Changing an element [5]
planets.append('Jupiter')   # Adding to the end [6]
last_planet = planets.pop() # Removing the last element [7]
2. Useful List Functions and Methods
Python provides built-in functions like len(), sum(), and sorted() to work with lists. Additionally, lists have specific methods accessed via dot syntax:
• index(): Finds the index of a specific value.
• in operator: Checks if a value exists within the list.
• help(list): Displays all available methods, such as clear(), copy(), and sort().
3. Objects and Methods
In Python, "everything is an object". Objects carry:
• Attributes: Data associated with the object (e.g., x.imag).
• Methods: Functions attached to the object (e.g., bit_length()).
4. Tuples: The Immutable Alternative
Tuples are defined using parentheses () instead of square brackets. They function like lists but are immutable, meaning they cannot be changed once created.
• Common Use Case: Tuples are ideal for functions that return multiple values.
• Variable Swapping: You can use tuple-like syntax to swap variables: a, b = b, a.