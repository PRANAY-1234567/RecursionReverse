📘 Reverse String Using Recursion (Python)

📌 Overview

This Python program reverses a given string using a recursive approach.

Recursion is a technique where a function calls itself to solve smaller instances of the same problem until it reaches a stopping condition (base case).

⚙️ Source Code
def reverse_string(s):
    if len(s) == 0:
        return s
    else:
        return reverse_string(s[1:]) + s[0]

print(reverse_string("hello"))
🧠 How It Works
1️⃣ Function Definition
def reverse_string(s):

Defines a function that takes a string s as input.

2️⃣ Base Case
if len(s) == 0:
    return s

Stops recursion when the string becomes empty.

Prevents infinite recursive calls.

3️⃣ Recursive Case
return reverse_string(s[1:]) + s[0]

s[1:] → Removes the first character of the string.

s[0] → First character of the string.

The function keeps calling itself with a smaller substring.

Characters are added back in reverse order.

🔄 Execution Example

For:

reverse_string("hello")

The recursive breakdown looks like:

reverse_string("hello")
= reverse_string("ello") + "h"
= reverse_string("llo") + "e" + "h"
= reverse_string("lo") + "l" + "e" + "h"
= reverse_string("o") + "l" + "l" + "e" + "h"
= reverse_string("") + "o" + "l" + "l" + "e" + "h"
= "" + "o" + "l" + "l" + "e" + "h"

Final Output:

olleh
▶️ Output
olleh
🔑 Key Concepts Demonstrated

Recursive function design

Base case and recursive case

String slicing (s[1:])

Understanding function call stack behavior

⏱️ Time & Space Complexity

Time Complexity: O(n²)
(Due to string slicing in each recursive call)

Space Complexity: O(n)
(Recursive call stack depth)

🚀 Alternative (Pythonic) Approach

Using slicing (non-recursive):

def reverse_string(s):
    return s[::-1]

This method is more efficient and recommended for practical use.

📚 Learning Outcomes
After reviewing this project, you should understand:

How recursion works with strings

Importance of base conditions

How smaller subproblems combine into a final solution

Performance considerations of recursive solutions

<img width="826" height="631" alt="image" src="https://github.com/user-attachments/assets/d1604f68-8a8c-474b-bda7-296bd9915341" />

