
# Python String Operations & Methods

## What is a String?

A **string** in Python is an immutable sequence of characters.

A string is used to store text data.

```python
name = "Harsha"
```

Examples of strings:

* Names
* Sentences
* Passwords
* Email addresses
* Messages

---

## Important Properties of Strings

* Ordered
* Immutable
* Indexed
* Iterable

---

## What does immutable mean?

It means once a string is created, it cannot be changed.

 Wrong:

```python
name = "Python"
name[0] = "J"
```

This gives error.

 Correct:

```python
name = "Jython"
```

---

# 1. Creating Strings

## Using Double Quotes

```python
name = "Python"
```

---

## Using Single Quotes

```python
name = 'Python'
```

---

## Using Triple Quotes

Used for multi-line strings.

```python
text = """Hello
Welcome to Python"""
```

---

# 2. String Indexing

Strings use **zero-based indexing**

```python
word = "Python"
```

| Character | Index |
| --------- | ----- |
| P         | 0     |
| y         | 1     |
| t         | 2     |
| h         | 3     |
| o         | 4     |
| n         | 5     |

---

## Access Character

```python
word[0]
```

Output:

```python
'P'
```

---

## Negative Indexing

Access from end.

```python
word[-1]
```

Output:

```python
'n'
```

---

# 3. String Slicing

Used to extract part of a string.

Syntax:

```python
string[start:end]
```

---

## Example

```python
word = "Python"

word[0:3]
```

Output:

```python
'Pyt'
```

---

## From Beginning

```python
word[:4]
```

Output:

```python
'Pyth'
```

---

## Till End

```python
word[2:]
```

Output:

```python
'thon'
```

---

## Reverse String

```python
word[::-1]
```

Output:

```python
'nohtyP'
```

---

# 4. String Concatenation

Joining strings using `+`

```python
first = "Hello"
second = "World"

first + " " + second
```

Output:

```python
'Hello World'
```

---

# 5. String Repetition

Using `*`

```python
"Hi" * 3
```

Output:

```python
'HiHiHi'
```

---

# 6. String Length

Using `len()`

```python
len("Python")
```

Output:

```python
6
```

---

# 7. Checking Characters

## `in`

```python
"P" in "Python"
```

Output:

```python
True
```

---

## `not in`

```python
"x" not in "Python"
```

Output:

```python
True
```

---

# 8. Important String Methods

| Method         | Description            |
| -------------- | ---------------------- |
| `upper()`      | Converts to uppercase  |
| `lower()`      | Converts to lowercase  |
| `capitalize()` | First letter uppercase |
| `title()`      | Capitalize each word   |
| `strip()`      | Removes spaces         |
| `replace()`    | Replace text           |
| `split()`      | Convert string to list |
| `join()`       | Join list into string  |
| `find()`       | Finds position         |
| `count()`      | Counts occurrences     |
| `startswith()` | Checks beginning       |
| `endswith()`   | Checks ending          |

---

# 9. `upper()`

Converts all letters to uppercase.

```python
text = "python"

text.upper()
```

Output:

```python
'PYTHON'
```

---

# 10. `lower()`

Converts to lowercase.

```python
"PYTHON".lower()
```

Output:

```python
'python'
```

---

# 11. `capitalize()`

Makes first letter uppercase.

```python
"python".capitalize()
```

Output:

```python
'Python'
```

---

# 12. `title()`

Capitalizes each word.

```python
"hello world".title()
```

Output:

```python
'Hello World'
```

---

# 13. `strip()`

Removes spaces from both sides.

```python
"  hello  ".strip()
```

Output:

```python
'hello'
```

---

## `lstrip()`

Removes left spaces

```python
" hello".lstrip()
```

---

## `rstrip()`

Removes right spaces

```python
"hello ".rstrip()
```

---

# 14. `replace()`

Replaces text.

```python
text = "I like Java"

text.replace("Java", "Python")
```

Output:

```python
'I like Python'
```

---

# 15. `split()`

Converts string into list.

```python
text = "apple,banana,mango"

text.split(",")
```

Output:

```python
['apple', 'banana', 'mango']
```

---

# 16. `join()`

Joins list into string.

```python
words = ["Python", "is", "easy"]

" ".join(words)
```

Output:

```python
'Python is easy'
```

---

# 17. `find()`

Returns first occurrence index.

```python
"Python".find("t")
```

Output:

```python
2
```

If not found:

```python
-1
```

---

# 18. `index()`

Similar to `find()`

Difference:

* `find()` returns -1
* `index()` gives error

```python
"Python".index("t")
```

---

# 19. `count()`

Counts occurrences.

```python
"banana".count("a")
```

Output:

```python
3
```

---

# 20. `startswith()`

Checks if string starts with value.

```python
"Python".startswith("Py")
```

Output:

```python
True
```

---

# 21. `endswith()`

Checks ending.

```python
"Python".endswith("on")
```

Output:

```python
True
```

---

# 22. String Formatting

## f-string (Best way)

```python
name = "Harsha"
age = 21

f"My name is {name} and I am {age}"
```

Output:

```python
'My name is Harsha and I am 21'
```

---

## `format()`

```python
"My name is {}".format("Harsha")
```

---

# 23. Escape Characters

| Escape Character | Meaning      |
| ---------------- | ------------ |
| `\n`             | New line     |
| `\t`             | Tab          |
| `\"`             | Double quote |
| `\\`             | Backslash    |

---

## Example

```python
print("Hello\nWorld")
```

Output:

```python
Hello
World
```

---

# 24. String Checking Methods

## `isalpha()`

Checks only letters

```python
"Python".isalpha()
```

---

## `isdigit()`

Checks only digits

```python
"123".isdigit()
```

---

## `isalnum()`

Checks letters + numbers

```python
"abc123".isalnum()
```

---

## `isspace()`

Checks only spaces

```python
"   ".isspace()
```

---

# 25. Iterating Through Strings

```python
word = "Python"

for char in word:
    print(char)
```

---

# 26. Comparing Strings

```python
"abc" == "abc"
```

Output:

```python
True
```

---

```python
"abc" > "abb"
```

Comparison is alphabetical.

---

# 27. Common String Operations

## Reverse String

```python
text[::-1]
```

---

## Count Words

```python
len(text.split())
```

---

## Remove Spaces

```python
text.replace(" ", "")
```

---


# 28. Common Mistakes

## Trying to Modify String


```python
name[0] = "H"
```

---

## Forgetting Reassignment

wrong way:
```python
text.upper()
```

correct way:
```python
text = text.upper()
```

---

