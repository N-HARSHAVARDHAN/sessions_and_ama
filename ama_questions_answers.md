# AMA SESSION QUESTIONS AND ANSWERS:

## Adhikya Edammala - Difference between `git add .` and `git add -A`?

- `git add .` → Adds new and modified files in current directory.
- `git add -A` → Adds all changes (new, modified, deleted) in entire repository.

---

## Allanki VV Manikanta Sai - What is an abstract class?

An abstract class is a class that cannot be instantiated and is used as a blueprint for other classes. It can contain abstract methods and concrete methods.

---

## Arpit Yadav - Do we need to implement all methods in child class for abstract class?

Yes. If all abstract methods are not implemented, the child class becomes abstract and cannot be instantiated.

---

## Boorle Sowmya Sri Lakshmi - What are generators in Python?

Generators are functions that return values one by one using `yield` instead of `return`. They are memory efficient.

---

## Injamuri Arun Kumar - What is the difference between `*args` and `**kwargs`?

- `*args` → Takes multiple positional arguments (tuple)
- `**kwargs` → Takes multiple keyword arguments or key value pairs  ( dictionary)

---

## Kamparapu Lakshman -  Can we declare concrete methods in abstract class?

Yes. Abstract classes can have both abstract methods and concrete (normal) methods.

---

## M Harivardhan Reddy - What is polymorphism?

Polymorphism means the same function or method behaves differently in different situations.

---

## Md Musharaf -  What is encapsulation?

Encapsulation is wrapping data and methods into a single unit (class) and restricting direct access to data.

---

## Naman Sharma -  What is abstraction?

Abstraction means hiding internal implementation details and showing only essential features.

---

## Parlapalli Sulochana - Can we create multiple objects of a class?

Yes. A single class can create multiple independent objects.

---

## Rongala Vasu - String methods in Python

- `upper()` → Converts all characters in a string to UPPERCASE
- `lower()` → Converts all characters in a string to lowercase
- `strip()` → Removes leading and trailing spaces
- `split()` → Splits a string into a list based on a separator
- `join()` → Joins elements of a list into a single string
- `find()` → Returns the index of the first occurrence of a substring (returns -1 if not found)
---

## Rovinpal Udupi - What is a module in Python?

A module is a `.py` file containing reusable functions, classes, and variables.

---

## Tumma Haritha - What is negative indexing in slicing?

Negative indexing starts from the end of a string or list:
- `-1` → last element
- `-2` → second last element

---

## Vikas Mehta - Difference between error and exception?

- Error → Serious issue (syntax/system), usually not handled
- Exception → Runtime issue that can be handled using try-except

---

## Yash Nitin Raut - Print even numbers from 0–10 without variable or modulo?

```python
print(*range(0, 11, 2))