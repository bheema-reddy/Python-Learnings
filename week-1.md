Here are various patterns you can use to build logic in pattern matching, which will also help in understanding loops—a crucial part of learning Data Structures and Algorithms (DSA).

### 1. **Right-Angled Triangle with Numbers**

#### **Code:**
```python
n = 5
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print(j, end="")
    print()
```

#### **Output:**
```
1
12
123
1234
12345
```

### 2. **Sequenced Number Triangle**

#### **Code:**
```python
n = 5
count = 1
for i in range(1, n + 1):
    for j in range(i):
        print(count, end="")
        count += 1
    print()
```

#### **Output:**
```
1
23
456
78910
1112131415
```

### 3. **Alphabet Triangle**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i + 1):
        print(chr(65 + j), end="")
    print()
```

#### **Output:**
```
A
AB
ABC
ABCD
ABCDE
```

### 4. **Right-Angled Triangle with Stars**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i + 1):
        print("*", end="")
    print()
```

#### **Output:**
```
*
**
***
****
*****
```

### 5. **Inverted Right-Angled Triangle with Stars**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i, n):
        print("*", end="")
    print()
```

#### **Output:**
```
*****
****
***
**
*
```

### 6. **Pyramid Pattern with Stars**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i, n):
        print(" ", end="")
    for k in range(i + 1):
        print("*", end="")
    for l in range(i):
        print("*", end="")
    print()
```

#### **Output:**
```
    *
   ***
  *****
 *******
*********
```

### 7. **Diamond Pattern with Stars**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i, n):
        print(" ", end="")
    for k in range(i + 1):
        print("*", end="")
    for l in range(i):
        print("*", end="")
    print()

for i in range(n):
    for j in range(i + 1):
        print(" ", end="")
    for k in range(i, n - 1):
        print("*", end="")
    for l in range(i, n - 1):
        print("*", end="")
    print()
```

#### **Output:**
```
    *
   ***
  *****
 *******
*********
*********
 *******
  *****
   ***
    *
```

### 8. **Zigzag Number Pattern**

#### **Code:**
```python
n = 5
for i in range(n):
    if i % 2 == 0:
        for j in range(i + 1):
            if j % 2 == 0:
                print("1", end = "")
            else:
                print("0", end = "")
    else:
        for j in range(i + 1):
            if j % 2 == 0:
                print("0", end = "")
            else:
                print("1", end = "")
    print()
```

#### **Output:**
```
1
01
101
0101
10101
```

### 9. **Palindromic Number Triangle**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i):
        print(j + 1, end="")
    for k in range(i, n - 1):
        print(" ", end="")
    for l in range(i, n - 1):
        print(" ", end="")
    for m in range(i):
        print(i - m, end="")
    print()
```

#### **Output:**
```
        
1      1
12    21
123  321
12344321
```

### 10. **Sequential Alphabet Triangle**

#### **Code:**
```python
n = 5
for i in range(n):
    for j in range(i + 1):
        if j == 0:
            print("A", end="")
        elif j == 1:
            print("B", end="")
        elif j == 2:
            print("C", end="")
        elif j == 3:
            print("D", end="")
        else:
            print("E", end="")
    print()
```

#### **Output:**
```
A
AB
ABC
ABCD
ABCDE
```

---

