# Reverse a String Using Recursion in Python

## 📌 Project Overview

This project demonstrates how to reverse a string in Python using **recursion**.

Recursion is a programming technique in which a function calls itself to solve a problem by breaking it down into smaller subproblems. The process continues until a specified **base condition** is reached.

This project focuses on understanding recursive function calls, base cases, string slicing, and the function call stack.

## 🎯 Objectives

* Understand the concept of recursion in Python.
* Implement a recursive function to reverse a string.
* Understand the importance of base and recursive cases.
* Explore Python string slicing.
* Analyze the time and space complexity of recursive solutions.

## ⚙️ Technologies Used

* **Programming Language:** Python
* **Concepts:** Recursion, Functions, String Slicing

## 💻 Source Code

```python
def reverse_string(s):
    # Base Case
    if len(s) == 0:
        return s

    # Recursive Case
    return reverse_string(s[1:]) + s[0]


# Function Call
result = reverse_string("hello")
print(result)
```

## ▶️ Output

```text
olleh
```

## 🧠 How It Works

The program uses two important components:

### 1. Function Definition

```python
def reverse_string(s):
```

Defines a recursive function that accepts a string as an argument.

### 2. Base Case

```python
if len(s) == 0:
    return s
```

* Checks whether the string is empty.
* Stops further recursive function calls.
* Prevents infinite recursion.

### 3. Recursive Case

```python
return reverse_string(s[1:]) + s[0]
```

* `s[1:]` removes the first character from the string.
* `s[0]` retrieves the first character.
* The function calls itself with the remaining substring.
* Characters are added back as the recursive calls return.

## 🔄 Execution Flow

Consider the input:

```python
reverse_string("hello")
```

The recursive execution takes place as follows:

```text
reverse_string("hello")
    reverse_string("ello") + "h"
        reverse_string("llo") + "e"
            reverse_string("lo") + "l"
                reverse_string("o") + "l"
                    reverse_string("") + "o"
```

When the empty string is reached, the base case returns an empty string.

The recursive calls then return in reverse order:

```text
"" + "o" + "l" + "l" + "e" + "h"
```

**Final Result:**

```text
olleh
```

## ⏱️ Time and Space Complexity

| Complexity       | Analysis |
| ---------------- | -------- |
| Time Complexity  | O(n²)    |
| Space Complexity | O(n)     |

**Time Complexity – O(n²):**

Each recursive call creates a new substring using string slicing. Since slicing takes time proportional to the substring length, the total time complexity is O(n²).

**Space Complexity – O(n):**

The recursive function creates approximately n function calls before reaching the base case.

## 🚀 Alternative Approach

Python also provides a simple string slicing technique to reverse a string without recursion.

```python
def reverse_string(s):
    return s[::-1]


print(reverse_string("hello"))
```

**Output:**

```text
olleh
```

The slicing expression `[::-1]` reverses the string by traversing it in the opposite direction.

## 📚 Key Learning Outcomes

By completing this program, you will understand:

* How recursion works in Python.
* How to implement base and recursive cases.
* How string slicing works.
* How recursive calls are stored in the call stack.
* How to analyze the time and space complexity of recursive algorithms.
* The difference between recursive and built-in string reversal approaches.

## 👨‍💻 Author

**Pranay Jadhao**

* GitHub: [PRANAY-1234567](https://github.com/PRANAY-1234567)
* LinkedIn: [Pranay Jadhao](https://linkedin.com/in/pranayjadhao)

---

⭐ If you find this project helpful, consider giving the repository a star!

<img width="826" height="631" alt="image" src="https://github.com/user-attachments/assets/d1604f68-8a8c-474b-bda7-296bd9915341" />

