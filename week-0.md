These notes will help you create a comprehensive understanding of basic programming concepts required before proceeding DSA using Python.

### **This Notes is made for people who want to learn DSA from A to Z for free in a well-organized and structured manner.**

---
## Step 1 : Learn the basics


## **Table of Contents**

1. [User Input/Output](#user-inputoutput)
2. [Data Types](#data-types)
3. [Operations on Data Types](#operations-on-data-types)
4. [Dictionary and Set](#dictionary-and-set)
5. [Mutable vs Immutable](#mutable-vs-immutable)
6. [Conversion Between Data Types](#conversion-between-data-types)
7. [Slicing in Python](#slicing-in-python)
8. [Conditional Statements (If-Else)](#conditional-statements-if-else)
9. [Loops (For and While)](#loops-for-and-while)
10. [Functions (Pass by Reference and Value)](#functions-pass-by-reference-and-value)
11. [Arrays and Strings](#arrays-and-strings)
12. [Time Complexity](#time-complexity)

---

## **1. User Input/Output**

### **User Input**
- **Taking Input from the User**:
  - In Python, user input is taken using the `input()` function.
  - The `input()` function always returns the input as a string. Therefore, conversion might be necessary.
  
  ```python
  name = input("Enter your name: ")
  age = int(input("Enter your age: "))  # Converting input to an integer
  ```
  
- **Example**:
  ```python
  name = input("What is your name? ")
  print(f"Nice to meet you, {name}!")
  ```

### **User Output**
- **Displaying Output to the User**:
  - The `print()` function is used to display output.
  - It can take multiple arguments and concatenate them with a space by default.
  
  ```python
  print("Hello", name, "!")
  print("You are", age, "years old.")
  ```

- **Formatted Strings**:
  - Python provides formatted string literals (f-strings) for easier and more readable output.
  
  ```python
  print(f"Hello, {name}! You are {age} years old.")
  ```

---

## **2. Data Types**

### **Primitive Data Types**
- **Integers (`int`)**:
  - Whole numbers, positive or negative, without a decimal point.
  - Example: `5`, `-10`, `0`
  
- **Floating-Point Numbers (`float`)**:
  - Numbers with a decimal point.
  - Example: `3.14`, `-2.0`, `0.5`
  
- **Strings (`str`)**:
  - Sequence of characters enclosed in quotes (single, double, or triple).
  - Example: `"Hello"`, `'Python'`, `"""This is a multiline string."""`
  
- **Boolean (`bool`)**:
  - Represents one of two values: `True` or `False`.
  - Often used in conditional statements.
  
  ```python
  is_adult = age >= 18
  ```

### **Composite Data Types**
- **Lists**:
  - Ordered, mutable collection of items.
  - Example: `[1, 2, 3, 4, 5]`
  
- **Tuples**:
  - Ordered, immutable collection of items.
  - Example: `(1, 2, 3, 4, 5)`
  
- **Sets**:
  - Unordered collection of unique items.
  - Example: `{1, 2, 3, 4, 5}`
  
- **Dictionaries**:
  - Unordered collection of key-value pairs.
  - Example: `{"name": "Alice", "age": 25}`

### **Type Conversion**
- **Implicit Type Conversion**:
  - Python automatically converts one data type to another when necessary.
  - Example: Adding an integer and a float results in a float.
  
  ```python
  result = 5 + 2.0  # result is 7.0 (float)
  ```

- **Explicit Type Conversion**:
  - Manually converting data types using functions like `int()`, `float()`, `str()`, etc.
  
  ```python
  number = int("10")
  pi = str(3.14)
  ```

---

## **3. Operations on Data Types**

### **Arithmetic Operations**
- **Addition (`+`)**:
  - Adds two numbers.
  - Example: `5 + 3 = 8`
  
- **Subtraction (`-`)**:
  - Subtracts the second number from the first.
  - Example: `5 - 3 = 2`
  
- **Multiplication (`*`)**:
  - Multiplies two numbers.
  - Example: `5 * 3 = 15`
  
- **Division (`/`)**:
  - Divides the first number by the second (result is always a float).
  - Example: `5 / 2 = 2.5`
  
- **Floor Division (`//`)**:
  - Divides and returns the largest integer less than or equal to the result.
  - Example: `5 // 2 = 2`
  
- **Modulus (`%`)**:
  - Returns the remainder of the division.
  - Example: `5 % 2 = 1`
  
- **Exponentiation (`**`)**:
  - Raises the first number to the power of the second.
  - Example: `5 ** 2 = 25`

### **Comparison Operations**
- **Equal to (`==`)**:
  - Checks if two values are equal.
  - Example: `5 == 5  # True`
  
- **Not equal to (`!=`)**:
  - Checks if two values are not equal.
  - Example: `5 != 3  # True`
  
- **Greater than (`>`)**:
  - Checks if the first value is greater than the second.
  - Example: `5 > 3  # True`
  
- **Less than (`<`)**:
  - Checks if the first value is less than the second.
  - Example: `3 < 5  # True`
  
- **Greater than or equal to (`>=`)**:
  - Checks if the first value is greater than or equal to the second.
  - Example: `5 >= 5  # True`
  
- **Less than or equal to (`<=`)**:
  - Checks if the first value is less than or equal to the second.
  - Example: `3 <= 5  # True`

### **Logical Operations**
- **AND (`and`)**:
  - Returns `True` if both conditions are `True`.
  - Example: `(5 > 3) and (5 < 10)  # True`
  
- **OR (`or`)**:
  - Returns `True` if at least one condition is `True`.
  - Example: `(5 > 3) or (5 > 10)  # True`
  
- **NOT (`not`)**:
  - Inverts the Boolean value.
  - Example: `not(5 > 3)  # False`

---

## **4. Dictionary and Set**

### **Dictionary**
- **Definition**:
  - A dictionary is an unordered, changeable, and indexed collection.
  - It consists of key-value pairs, where each key is unique.
  
- **Creating a Dictionary**:
  ```python
  person = {"name": "Alice", "age": 25, "city": "New York"}
  ```

- **Accessing Values**:
  - Access the value associated with a key using square brackets.
  
  ```python
  print(person["name"])  # Output: Alice
  ```

- **Modifying Values**:
  - Modify the value associated with a key by assigning a new value.
  
  ```python
  person["age"] = 26
  ```

- **Adding Items**:
  - Add a new key-value pair by assigning a value to a new key.
  
  ```python
  person["email"] = "alice@example.com"
  ```

- **Removing Items**:
  - Remove a key-value pair using the `del` statement or the `pop()` method.
  
  ```python
  del person["age"]
  email = person.pop("email")
  ```

### **Set**
- **Definition**:
  - A set is an unordered collection of unique items.
  
- **Creating a Set**:
  ```python
  fruits = {"apple", "banana", "cherry"}
  ```

- **Adding Items**:
  - Add an item to a set using the `add()` method.
  
  ```python
  fruits.add("orange")
  ```

- **Removing Items**:
  - Remove an item using the `remove()` or `discard()` method.
  
  ```python
  fruits.remove("banana")
  ```

- **Set Operations**:
  - **Union (`|`)**: Combines two sets, returning all unique items.
  - **Intersection (`&`)**: Returns common items between two sets.
  - **Difference (`-`)**: Returns items that are in the first set but not in the second.
  - **Symmetric Difference (`^`)**: Returns items that are in either set but not in both

.
  
  ```python
  set1 = {1, 2, 3}
  set2 = {3, 4, 5}
  union_set = set1 | set2  # {1, 2, 3, 4, 5}
  intersection_set = set1 & set2  # {3}
  difference_set = set1 - set2  # {1, 2}
  sym_diff_set = set1 ^ set2  # {1, 2, 4, 5}
  ```

---

## **5. Mutable vs Immutable**

### **Mutable Objects**
- **Definition**:
  - Objects that can be modified after creation.
  
- **Examples**:
  - Lists, dictionaries, and sets are mutable.
  
- **Example**:
  ```python
  my_list = [1, 2, 3]
  my_list[0] = 10  # Now my_list is [10, 2, 3]
  ```

### **Immutable Objects**
- **Definition**:
  - Objects that cannot be modified after creation.
  
- **Examples**:
  - Strings, tuples, and integers are immutable.
  
- **Example**:
  ```python
  my_tuple = (1, 2, 3)
  # my_tuple[0] = 10  # This will raise an error
  
  my_string = "Hello"
  # my_string[0] = "h"  # This will raise an error
  ```

---

## **6. Conversion Between Data Types**

### **Implicit Type Conversion**
- **Automatic Conversion**:
  - Python automatically converts one data type to another when needed.
  
- **Example**:
  ```python
  x = 5
  y = 2.5
  result = x + y  # result is 7.5 (float)
  ```

### **Explicit Type Conversion**
- **Manual Conversion**:
  - Convert data types manually using functions like `int()`, `float()`, `str()`, etc.
  
- **Examples**:
  ```python
  num_str = "10"
  num_int = int(num_str)  # Converts string to integer
  
  pi = 3.14
  pi_str = str(pi)  # Converts float to string
  ```

---

## **7. Slicing in Python**

### **What is Slicing?**
- **Definition**:
  - Slicing allows you to extract a portion of a sequence (like a list, tuple, or string) by specifying a start, stop, and step.
  
- **Syntax**:
  ```python
  sequence[start:stop:step]
  ```

- **Explanation**:
  - **Start**: The index where the slice starts (inclusive).
  - **Stop**: The index where the slice ends (exclusive).
  - **Step**: The number of steps to skip between elements (optional).
  
- **Examples**:
  ```python
  text = "Hello, World!"
  
  # Extract 'Hello'
  print(text[0:5])  # Output: Hello
  
  # Extract 'World' using negative indices
  print(text[-6:-1])  # Output: World
  
  # Extract every second character
  print(text[::2])  # Output: Hlo ol!
  
  # Reverse the string
  print(text[::-1])  # Output: !dlroW ,olleH
  ```

---

## **8. Conditional Statements (If-Else)**

### **If-Else Statements**
- **Definition**:
  - Conditional statements allow you to execute a block of code based on a condition.
  
- **Syntax**:
  ```python
  if condition:
      # code to execute if condition is true
  elif another_condition:
      # code to execute if another_condition is true
  else:
      # code to execute if no conditions are true
  ```

- **Example**:
  ```python
  age = int(input("Enter your age: "))
  
  if age >= 18:
      print("You are an adult.")
  elif age >= 13:
      print("You are a teenager.")
  else:
      print("You are a child.")
  ```

- **Nested If Statements**:
  - You can nest if statements to check multiple conditions.
  
  ```python
  num = int(input("Enter a number: "))
  
  if num > 0:
      if num % 2 == 0:
          print("Positive even number")
      else:
          print("Positive odd number")
  else:
      print("Negative number or zero")
  ```

---

## **9. Loops (For and While)**

### **For Loop**
- **Definition**:
  - The `for` loop is used to iterate over a sequence (like a list, tuple, dictionary, set, or string).
  
- **Syntax**:
  ```python
  for item in sequence:
      # code to execute for each item
  ```

- **Example**:
  ```python
  fruits = ["apple", "banana", "cherry"]
  
  for fruit in fruits:
      print(fruit)
  ```

- **Looping with `range()`**:
  - The `range()` function generates a sequence of numbers.
  
  ```python
  for i in range(5):
      print(i)  # Output: 0, 1, 2, 3, 4
  ```

### **While Loop**
- **Definition**:
  - The `while` loop repeats a block of code as long as a condition is true.
  
- **Syntax**:
  ```python
  while condition:
      # code to execute as long as condition is true
  ```

- **Example**:
  ```python
  i = 0
  while i < 5:
      print(i)
      i += 1  # Output: 0, 1, 2, 3, 4
  ```

- **Infinite Loop**:
  - A loop that never ends (usually because the condition never becomes false).
  
  ```python
  while True:
      print("This loop will run forever!")
  ```

- **Breaking out of a Loop**:
  - Use the `break` statement to exit a loop prematurely.
  
  ```python
  i = 0
  while i < 10:
      if i == 5:
          break
      print(i)
      i += 1  # Output: 0, 1, 2, 3, 4
  ```

- **Skipping an Iteration**:
  - Use the `continue` statement to skip the rest of the loop for the current iteration.
  
  ```python
  for i in range(5):
      if i == 3:
          continue
      print(i)  # Output: 0, 1, 2, 4
  ```

---

## **10. Functions (Pass by Reference and Value)**

### **Functions**
- **Definition**:
  - A function is a block of code that performs a specific task and can be reused.
  
- **Syntax**:
  ```python
  def function_name(parameters):
      # code to execute
      return value  # optional
  ```

- **Example**:
  ```python
  def greet(name):
      return f"Hello, {name}!"
  
  message = greet("Alice")
  print(message)  # Output: Hello, Alice!
  ```

### **Pass by Value vs Pass by Reference**
- **Pass by Value**:
  - When an immutable object (e.g., integers, strings) is passed to a function, a copy is made, and the original object is not modified.
  
  ```python
  def modify_value(x):
      x = 10
  
  num = 5
  modify_value(num)
  print(num)  # Output: 5
  ```

- **Pass by Reference**:
  - When a mutable object (e.g., lists, dictionaries) is passed to a function, the original object can be modified.
  
  ```python
  def modify_list(lst):
      lst[0] = 10
  
  numbers = [1, 2, 3]
  modify_list(numbers)
  print(numbers)  # Output: [10, 2, 3]
  ```

### **Default Parameters**
- **Definition**:
  - Functions can have default parameter values that are used if no argument is provided.
  
- **Example**:
  ```python
  def greet(name="Guest"):
      return f"Hello, {name}!"
  
  print(greet())  # Output: Hello, Guest!
  print(greet("Alice"))  # Output: Hello, Alice!
  ```

### **Keyword Arguments**
- **Definition**:
  - Functions can accept arguments using their parameter names (keywords).
  
- **Example**:
  ```python
  def describe_pet(animal_type, pet_name):
      print(f"I have a {animal_type} named {pet_name}.")
  
  describe_pet(animal_type="dog", pet_name="Rex")
  ```

### **Arbitrary Arguments**
- **Definition**:
  - Functions can accept an arbitrary number of arguments using `*args` for positional arguments and `**kwargs` for keyword arguments.
  
- **Example**:
  ```python
  def print_numbers(*args):
      for number in args:
          print(number)
  
  print_numbers(1, 2, 3, 4, 5)
  ```

---

## **11. Arrays and Strings**

### **Arrays**
- **Definition**:
  - In Python,

 lists can be used as arrays to store multiple items in a single variable.
  
- **Operations on Arrays**:
  - **Accessing Elements**: Use indexing to access elements.
  - **Modifying Elements**: Assign a new value to an index.
  - **Appending Elements**: Use the `append()` method to add elements.
  
  ```python
  numbers = [1, 2, 3]
  print(numbers[0])  # Output: 1
  
  numbers[1] = 10
  print(numbers)  # Output: [1, 10, 3]
  
  numbers.append(4)
  print(numbers)  # Output: [1, 10, 3, 4]
  ```

### **Strings**
- **String Operations**:
  - **Concatenation**: Use the `+` operator to concatenate strings.
  - **Repetition**: Use the `*` operator to repeat a string.
  - **Indexing**: Access individual characters using indices.
  
  ```python
  text = "Hello"
  
  # Concatenation
  text = text + " World"
  print(text)  # Output: Hello World
  
  # Repetition
  print(text * 3)  # Output: Hello WorldHello WorldHello World
  
  # Indexing
  print(text[0])  # Output: H
  print(text[-1])  # Output: d
  ```

- **String Methods**:
  - **Uppercase**: `upper()` converts the string to uppercase.
  - **Lowercase**: `lower()` converts the string to lowercase.
  - **Split**: `split()` splits the string into a list of substrings.
  - **Join**: `join()` joins elements of a list into a string.
  
  ```python
  text = "Hello, World!"
  
  print(text.upper())  # Output: HELLO, WORLD!
  print(text.lower())  # Output: hello, world!
  
  words = text.split()
  print(words)  # Output: ['Hello,', 'World!']
  
  new_text = "-".join(words)
  print(new_text)  # Output: Hello,-World!
  ```

---

## **12. Time Complexity**

### **What is Time Complexity?**
- **Definition**:
  - Time complexity is a way to represent the amount of time an algorithm takes to complete as a function of the size of its input.
  
### **Big-O Notation**
- **Definition**:
  - Big-O notation is used to classify algorithms based on their time complexity.
  
- **Common Time Complexities**:
  - **O(1)**: Constant time (e.g., accessing an element in an array).
  - **O(log n)**: Logarithmic time (e.g., binary search).
  - **O(n)**: Linear time (e.g., traversing a list).
  - **O(n log n)**: Log-linear time (e.g., merge sort).
  - **O(n^2)**: Quadratic time (e.g., bubble sort).
  - **O(2^n)**: Exponential time (e.g., recursive algorithms like Fibonacci).
  - **O(n!)**: Factorial time (e.g., permutations).
  
### **Example of Time Complexity Analysis**
- **Linear Search**:
  - Time Complexity: O(n)
  
  ```python
  def linear_search(arr, target):
      for i in range(len(arr)):
          if arr[i] == target:
              return i
      return -1
  ```
  
- **Binary Search**:
  - Time Complexity: O(log n)
  
  ```python
  def binary_search(arr, target):
      left, right = 0, len(arr) - 1
      while left <= right:
          mid = (left + right) // 2
          if arr[mid] == target:
              return mid
          elif arr[mid] < target:
              left = mid + 1
          else:
              right = mid - 1
      return -1
  ```

---


Feel free to clone this repository and practice the concepts by writing your own code and testing different scenarios!
