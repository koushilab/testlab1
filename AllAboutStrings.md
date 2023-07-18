# Commonly Used String Operations 

`capitalize()`:
This method capitalizes the first character of a string while making all other characters lowercase.

Example:

```python
text = "hello world"
capitalized_text = text.capitalize()
print(capitalized_text)  # Output: "Hello world"
```

`upper()` and `lower()`:
`upper()` converts all characters of a string to uppercase, and `lower()` converts them to lowercase.

Example:

```python
text = "Hello, World"
upper_text = text.upper()
lower_text = text.lower()
print(upper_text)  # Output: "HELLO, WORLD"
print(lower_text)  # Output: "hello, world"
```

`title()`:
This method capitalizes the first letter of each word in a string.

Example:

```python
text = "hello, world"
title_text = text.title()
print(title_text)  # Output: "Hello, World"
```

`swapcase()`:
This method swaps the case of all characters in a string, converting uppercase to lowercase and vice versa.

Example:

```python
text = "Hello, World"
swapped_text = text.swapcase()
print(swapped_text)  # Output: "hELLO, wORLD"
```

`strip()`, `lstrip()`, and `rstrip()`:
These methods remove leading and trailing whitespace characters (spaces, tabs, newline) from a string. `strip()` removes both leading and trailing, `lstrip()` only removes leading, and `rstrip()` only removes trailing whitespace.

Example:

```python
text = "   Hello, World   "
stripped_text = text.strip()
left_stripped_text = text.lstrip()
right_stripped_text = text.rstrip()
print(stripped_text)         # Output: "Hello, World"
print(left_stripped_text)    # Output: "Hello, World   "
print(right_stripped_text)   # Output: "   Hello, World"
```

`find()` and `rfind()`:
`find()` returns the index of the first occurrence of a substring in a string, and `rfind()` returns the index of the last occurrence. If the substring is not found, both methods return -1.

Example:

```python
text = "Hello, World"
index1 = text.find("o")
index2 = text.rfind("o")
print(index1)  # Output: 4
print(index2)  # Output: 8
```

`replace()`:
This method replaces all occurrences of a substring with another substring in a string.

Example:

```python
text = "Hello, World"
new_text = text.replace("World", "Python")
print(new_text)  # Output: "Hello, Python"
```

`split()`:
This method splits a string into a list of substrings based on a delimiter. By default, the delimiter is whitespace.

Example:

```python
text = "apple,banana,orange"
fruits_list = text.split(",")
print(fruits_list)  # Output: ["apple", "banana", "orange"]
```

9. `join()`:
This method joins elements of a list into a single string using a specified separator.

Example:

```python
fruits_list = ["apple", "banana", "orange"]
fruits_text = ", ".join(fruits_list)
print(fruits_text)  # Output: "apple, banana, orange"
```

10. `startswith()` and `endswith()`:
`startswith()` checks if a string starts with a specified substring, and `endswith()` checks if it ends with a specified substring. Both methods return a boolean value.

Example:

```python
text = "Hello, World"
starts_with_hello = text.startswith("Hello")
ends_with_world = text.endswith("World")
print(starts_with_hello)  # Output: True
print(ends_with_world)    # Output: True
```

# String Concatenation and Formatting


String Concatenation:
You can concatenate (combine) two or more strings using the `+` operator.

Example:

```python
string1 = "Hello"
string2 = "World"
concatenated_string = string1 + ", " + string2
print(concatenated_string)  # Output: "Hello, World"
```

String Formatting (using f-strings):
f-strings (formatted string literals) allow you to embed expressions inside string literals, using curly braces `{}`. The expressions are evaluated and inserted into the string.

Example:

```python
name = "Alice"
age = 30
formatted_string = f"My name is {name} and I am {age} years old."
print(formatted_string)  # Output: "My name is Alice and I am 30 years old."
```

String Slicing:
Slicing allows you to extract a portion of a string based on its index. The syntax is `string[start:end]`, where `start` is the starting index, and `end` is the ending index (exclusive).

Example:

```python
text = "Hello, World"
substring1 = text[0:5]
substring2 = text[7:]
print(substring1)  # Output: "Hello"
print(substring2)  # Output: "World"
```

String Length (len()):
The `len()` function returns the length of a string, which is the number of characters in the string.

Example:

```python
text = "Hello, World"
length = len(text)
print(length)  # Output: 12
```

String Membership (in and not in):
You can check if a substring exists in a string using the `in` and `not in` keywords. These operations return a boolean value.

Example:

```python
text = "Hello, World"
contains_hello = "Hello" in text
contains_python = "Python" in text
print(contains_hello)  # Output: True
print(contains_python)  # Output: False
```

String Validation:
You can check if a string contains only specific types of characters using methods like `isalpha()`, `isdigit()`, `isalnum()`, etc.

Example:

```python
text1 = "Hello"
text2 = "123"
text3 = "Hello123"
print(text1.isalpha())  # Output: True (contains only alphabetic characters)
print(text2.isdigit())  # Output: True (contains only digits)
print(text3.isalnum())  # Output: True (contains both alphabetic characters and digits)
```

String Alignment (ljust(), rjust(), center()):
These methods allow you to align a string to the left, right, or center within a given width.

Example:

```python
text = "Hello"
left_aligned = text.ljust(10)
right_aligned = text.rjust(10)
centered = text.center(10)
print(left_aligned)   # Output: "Hello     "
print(right_aligned)  # Output: "     Hello"
print(centered)       # Output: "  Hello   "
```


# String Partitions

String Count:
The `count()` method counts the occurrences of a substring within a string.

Example:

```python
text = "apple, banana, orange, apple"
count_apple = text.count("apple")
print(count_apple)  # Output: 2
```

String Partition and rpartition:
The `partition()` method splits a string into three parts based on the first occurrence of a separator. If the separator is not found, it returns the original string and two empty strings. `rpartition()` works similarly but starts searching from the right.

Example:

```python
text = "apple, banana, orange"
part1, separator, part2 = text.partition(", ")
print(part1)       # Output: "apple"
print(separator)   # Output: ", "
print(part2)       # Output: "banana, orange"
```

String isX methods:
Python provides several `isX` methods to check the characteristics of a string. For example: `isalnum()`, `isalpha()`, `isdigit()`, `islower()`, `isupper()`, `isspace()`, etc.

Example:

```python
text1 = "Hello123"
text2 = "abc"
text3 = "123"
print(text1.isalnum())  # Output: True (contains only alphanumeric characters)
print(text2.isalpha())  # Output: True (contains only alphabetic characters)
print(text3.isdigit())  # Output: True (contains only digits)
```

String Splitlines:
The `splitlines()` method splits a string at line breaks and returns a list of lines.

Example:

```python
multiline_text = "Line 1\nLine 2\nLine 3"
lines_list = multiline_text.splitlines()
print(lines_list)  # Output: ["Line 1", "Line 2", "Line 3"]
```

String Encoding and Decoding:
Python allows you to encode a string into bytes and decode bytes back into a string using different character encodings like UTF-8, ASCII, etc.

Example:

```python
text = "Hello, World!"
encoded_bytes = text.encode("utf-8")
decoded_string = encoded_bytes.decode("utf-8")
print(encoded_bytes)   # Output: b'Hello, World!'
print(decoded_string)  # Output: "Hello, World!"
```

String Replace with Limit:
The `replace()` method also allows specifying a limit for the number of occurrences to replace.

Example:

```python
text = "apple, banana, orange, apple, cherry, apple"
replaced_text = text.replace("apple", "pear", 2)
print(replaced_text)  # Output: "pear, banana, orange, pear, cherry, apple"
```

String Justification with Fill Character:
You can specify a fill character for the `ljust()`, `rjust()`, and `center()` methods.

Example:

```python
text = "Hello"
left_aligned = text.ljust(10, "-")
right_aligned = text.rjust(10, "*")
centered = text.center(10, "+")
print(left_aligned)   # Output: "Hello-----"
print(right_aligned)  # Output: "*****Hello"
print(centered)       # Output: "+++Hello++"
```

String Formatting with `%`:
Old-style string formatting using `%` is also possible, although f-strings (formatted string literals) are generally preferred.

Example:

```python
name = "Alice"
age = 30
formatted_string = "My name is %s and I am %d years old." % (name, age)
print(formatted_string)  # Output: "My name is Alice and I am 30 years old."
```


# Less Used String Operations 

String Zfill:
The `zfill()` method pads a numeric string with zeros to a specified width.

Example:

```python
number = "42"
padded_number = number.zfill(6)
print(padded_number)  # Output: "000042"
```

String Case Swapping:
You can swap the case of characters in a string using the `casefold()` method.

Example:

```python
text = "Hello, World"
swapped_case = text.swapcase()
print(swapped_case)  # Output: "hELLO, wORLD"
```

String Justification with Centering:
The `center()` method can take an additional fill character to center the text.

Example:

```python
text = "Hello"
centered = text.center(10, "-")
print(centered)  # Output: "--Hello---"
```

String Title Case:
The `title()` method capitalizes the first character of each word, similar to the `title()` function explained earlier.

Example:

```python
text = "hello, world"
title_case = text.title()
print(title_case)  # Output: "Hello, World"
```

String Checking (isX methods):
You can check for specific conditions with `isnumeric()`, `isdecimal()`, `isprintable()`, etc.

Example:

```python
num_str = "123"
print(num_str.isnumeric())    # Output: True (contains only numeric characters)
print(num_str.isdecimal())    # Output: True (contains only decimal characters)
print(num_str.isprintable())  # Output: True (all characters are printable)
```

String Translation (str.maketrans and translate):
You can use `str.maketrans()` to create a translation table for characters and then use `translate()` to apply the translation.

Example:

```python
text = "Hello, World"
translation_table = str.maketrans("eo", "34")
translated_text = text.translate(translation_table)
print(translated_text)  # Output: "H4ll4, W4rld"
```

String Centering with String Formatting:
You can use string formatting to center text using the format specification.

Example:

```python
text = "Hello"
centered = "{:^10}".format(text)
print(centered)  # Output: "  Hello   "
```

String Alignment with String Formatting:
String formatting allows for alignment using `<`, `>`, or `^` along with width specification.

Example:

```python
text = "Hello"
left_aligned = "{:<10}".format(text)
right_aligned = "{:>10}".format(text)
print(left_aligned)   # Output: "Hello     "
print(right_aligned)  # Output: "     Hello"
```

These are some more useful string operations in Python that can help you work with strings effectively. Python's rich string manipulation capabilities make it easy to handle various text processing tasks.