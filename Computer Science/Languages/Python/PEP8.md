```toc
```
## Code Lay-out
### Indentation

**Use 4 spaces per indentation level**

```python
# Add 4 spaces (an extra level of indentation) to distinguish arguments from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)

# Wrong:

# Arguments on first line forbidden when not using vertical alignment.
foo = long_function_name(var_one, var_two,
    var_three, var_four)

# Further indentation required as indentation is not distinguishable.
def long_function_name(
    var_one, var_two, var_three,
    var_four):
    print(var_one)
```

### Maximum Line Length

**Limit all lines to a maximum of 79 characters**

Limiting the required editor window width makes it possible to have several files open side by side

### Should a Line Break Before or After a Binary Operator

```python
# Wrong:
# operators sit far away from their operands
income = (gross_wages +
          taxable_interest +
          (dividends - qualified_dividends) -
          ira_deduction -
          student_loan_interest)
# Correct:
# easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
```

### Blank Lines

* Surround top-level functions and class definitions with **two blank lines**.
* Method definitions inside a class are surrounded by a single blank line
* Extra blank lines may be used (sparingly) to separate groups of related functions.
* Use blank lines in functions, sparingly, to indicate logical section

### Imports 

Imports should usually be on separate lines:
```python
# Correct:
import os
import sys

# Wrong:
import sys, os

# Correct:
from subprocess import Popen, PIPE
```

Imports should be grouped in the following order:

1. Standard library imports
2. Related third party imports
3. Local application/library specific imports

You should put a blank line between each group of imports

## Whitespace in Expressions and Statements

Avoid extraneous whitespace in the following situations:

* Immediately inside parentheses, brackets or braces:
  ```python
  # Correct:
  spam(ham[1], {eggs: 2})

  # Wrong:
  spam( ham[ 1 ], { eggs: 2 } )
  ```
* Between a trailing comma and a following close parenthesis:
```python
# Correct:
foo = (0,)

# Wrong:
bar = (0, )
```
* Immediately before a comma, semicolon, or colon:
```python
# Correct:
if x == 4: print(x, y); x, y = y, x

# Wrong:
if x == 4 : print(x , y) ; x , y = y , x
```
* Immediately before the open parenthesis that starts the argument list of a function call:
```python
# Correct:
spam(1)

# Wrong:
spam (1)
```
* Immediately before the open parenthesis that starts an indexing or slicing:
```python
# Correct:
dct['key'] = lst[index]

# Wrong:
dct ['key'] = lst [index]
```
* More than one space around an assignment (or other) operator to align it with another:
```python
# Correct:
x = 1
y = 2
long_variable = 3

# Wrong:
x             = 1
y             = 2
long_variable = 3
```

## Comments
