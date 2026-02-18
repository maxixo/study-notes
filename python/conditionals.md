. Understanding Booleans and Comparisons
In Python, the bool type has two possible values: True and False. Typically, these values result from comparison operators that answer yes/no questions:
Operation
Description
Operation
Description
a == b
a equal to b
a != b
a not equal to b
a < b
a less than b
a > b
a greater than b
a <= b
a less than or equal to b
a >= b
a greater than or equal to b
A common mistake is using a single equals sign (=) instead of double (==). Use == to ask about a value and = to change a value.
Example: A Presidential Eligibility Check
def can_run_for_president(age):
    """Can someone of the given age run for president in the US?"""
    # The US Constitution says you must be at least 35 years old
    return age >= 35

print("Can a 19-year-old run for president?", can_run_for_president(19)) # False [3]
2. Combining Logic with and, or, and not
You can combine boolean values to create complex logic.
• Precedence: and is evaluated before or.
• Best Practice: Use parentheses to ensure your logic is correct and readable.
Example: Complex Conditions
def can_run_for_president(age, is_natural_born_citizen):
    # Must be a natural born citizen AND at least 35 years old
    return is_natural_born_citizen and (age >= 35) [4]

# Improving readability with parentheses and multiple lines:
prepared_for_weather = (
    have_umbrella
    or ((rain_level < 5) and have_hood)
    or (not (rain_level > 0 and is_workday))
) [8]
3. Conditional Statements: if, elif, and else
Conditionals control which code blocks run based on a Boolean condition. Python uses colons (:) and whitespace (4 spaces) to define these blocks.
def inspect(x):
    if x == 0:
        print(x, "is zero")
    elif x > 0:
        print(x, "is positive")
    elif x < 0:
        print(x, "is negative")
    else:
        print(x, "is unlike anything I've ever seen...") [8, 9]
Note that elif (else if) and else blocks are optional.
4. "Truthy" and "Falsey" Values
Python can treat non-boolean objects as booleans. Generally, empty sequences (like "" or 0) are False, while everything else is True.
print(bool(1))     # True
print(bool(0))     # False
print(bool("asf")) # True
print(bool(""))    # False [10]

if "spam":
    print("spam") # This prints because "spam" is "truthy" [11]
