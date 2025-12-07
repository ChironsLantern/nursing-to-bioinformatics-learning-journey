# Variables and Some Arithmetic
> 
> One of the most important features of any programming language is its ability to manipulate variables. A variable is just a name that refers to a value; you can think of a variable as a box that stores a piece of data.
> 
> In [Python](https://rosalind.info/glossary/python/), the basic data types are strings and numbers. There are two types of numbers: integers (both positive and negative) and floats (fractional numbers with a decimal point). You can assign numbers to variables very easily. Try running the following program:
> 
> a = 324
> b = 24
> c = a - b
> print 'a - b is', c
> **MY WORK**:  print("a - b is", c)
> *A little confused between this working, and when to concatenate string and integers* --
> 	When to Use Commas vs. Concatenation 

> [!NOTE]
> %% %% Python 3 has two main ways to print multiple items, and one is significantly easier because it handles the type conversions for you. 
> 
> Method 1: Using Commas (The easiest way, your correct solution) 
> 
> When you use a **comma** (`,`) inside the `print()` function in Python 3, you are passing multiple _arguments_ to the function. Python automatically adds a single space between each argument and handles the necessary conversion of integers (`c`) to a string format internally. 
> 
> - **Your Code (Correct):** `print("a - b is", c)`
> - **Output:** `a - b is 300` (assuming 
>     
>     ![](data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)
>     
>     a=324,b=24
>     
>     𝑎=324,𝑏=24
>     
>     ) 
> 
> This is the preferred method in Python 3 because it prevents type errors. 
> 
> Method 2: Using the `+` Operator (Manual Concatenation) 
> 
> The plus sign (`+`) operator performs **concatenation** (joining strings together). Python is a **strongly typed** language, meaning you cannot combine a string data type with an integer data type using the `+` operator directly. You must manually convert the integer to a string first using the `str()` function. 
> 
> - **Manual Concatenation (Correct):** `print("a - b is " + str(c))`
> - **Output:** `a - b is 300` 
> 
> If you try to use `+` without `str()`, you get a `TypeError`: 
> 
> - **Error Code:** `print("a - b is " + c)`
> - **Error Message:** `TypeError: can only concatenate str (not "int") to str` %% %%

> 
> In the above code, a, b, and c are all integers, and 'a - b is' is a string. The result of this program is to print:
> 
> a - b is 300
> 
> You can now use all common arithmetic operations involving numbers:
> 
> - Addition: `2 + 3 == 5`
> - Subtraction: `5 - 2 == 3`
> - Multiplication: `3 * 4 == 12`
> - Division: `15 / 3 == 5`
> - Division remainder: `18 % 5 == 3`
> - Exponentiation: `2 ** 3 == 8`
> 
> It is important to note that if you try to divide two integers, [Python](https://rosalind.info/glossary/python/) always rounds _down_ the result (so `18/5 == 3`).
> 
> To obtain a precise result for this division, you need to indicate floating point division; either of the following expressions results in a "float" data type: `18.0/5 == 3.6` or `float(18)/5 == 3.6`
> 
> In [Python](https://rosalind.info/glossary/python/), the single equals sign (`=`) means "assign a value to a variable". For example, `a = 3` assigns 3 to the integer a. In order to denote equality, [Python](https://rosalind.info/glossary/python/) uses the double equals sign (`==`).
> 
> In [Python](https://rosalind.info/glossary/python/), a string is an ordered sequence of letters, numbers and other characters. You can create string variables just like you did with :
> 
> a = "Hello"
> b = "World"
> 
> Notice that the string must be surrounded by " or ' (but not a mix of both). You can use quotes inside the string, as long as you use the opposite type of quotes to surround the string, e.g., `a = "Monty Python's Flying Circus"` or `b = 'Project "Rosalind"'`.
> 
> String operations differ slightly from operations on numbers:
> 
> a = 'Rosalind'
> b = 'Franklin'
> c = '!'
> print a + ' ' + b + c*3
> 
> Output:
> 
> Rosalind Franklin!!!

## Problem

Given: Two positive integers a and b, each less than 1000.

Return: The integer corresponding to the square of the hypotenuse of the right triangle whose legs have lengths a and b.

**Notes**:

1. The dataset changes every time you click "Download dataset".
2. We check only your final answer to the _downloaded_ dataset in the box below, not your code itself. If you would like to provide your code as well, you may use the upload tool. Please also note that the correct answer to this problem will not in general be 34; it is simply an example of what you should return in the specific case that the legs of the triangle have length 3 and 5.

## Sample Dataset

3 5
====
## Sample Output

34

> [!NOTE]
>  **My work:** 
> In Terminal
> need >>> not the string that ends with %, so
> typed in python3
> assigned the variables:
> a = 3
> b = 5
> attached Pythagorean Theorem to variable "square_of_hypotenuse"
> square_of_hypotenuse = (a ** 2) + (b ** 2) (ETA: In this Obsidian note, it deleted the asterisk x2 between a and 2, and b and 2) but they are there :) )
> print(square_of_hypotenuse)
> 
> Testing:
> I tried to put in new variables for a and b and then print again, but it gave me the same answer. (*Doesn't it modify the variables??*)
> 
> ==Per GoogleAI: **Python does not automatically recalculate a variable's value when its input variables change**; you must explicitly re-run the calculation line every time.==
> 
> ==In the interactive shell, each line of code runs sequentially and independently.== 