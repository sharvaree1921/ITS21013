> Date: 1/05/2021
## Numbers:
- All normal operators, parentheses (()) for grouping, % for remainder, ** for power.
- Division (/) always returns float value. To discard fractional part, use //. 
- Format for assigning/defining: `width = 20 `
- Complex number: **3+5j**
#### Variable _ :
- Last printed expression is assigned to it. (Read only variable)
- format: eg: ` 60 + _ `

## Strings:
- "text" or 'text', `print()` for output.

#### escaping single quote or double quote `\`
- For output, The string is enclosed in double quotes if the string contains a single quote and no double quotes, otherwise it is enclosed in single quotes.
```python
>>> 'doesn\'t'
"doesn't"
>>> '"Yes," they said.'
'"Yes," they said.'
>>> "\"Yes,\" they said."
'"Yes," they said.'
#using print statement
>>> print('"Isn\'t," they said.')
"Isn't," they said.
```
#### Newline:
```python
#eg1:
>>> s = "One\nTwo"
>>> print(s)
One
Two

#eg2:
>>> s = r'One\nTwo'     #Note the r before the string
>>> print(s)
One\nTwo
```
#### Using multiple lines in string:
- Use `'''...'''` or `"""..."""` 
- **Note: Here end of lines are automatically included.**
- **To prevent this, use `\` at the end of the line.**

#### OPERATIONS ON STRINGS
- Lenth of a string: `len()` eg: `len('var')` will give output 3.
- `+` and `*` 
```python
>>> 3 * 'a' + 'b'
'aaab' 
>>> print('Enter your name:')
x = input()           #Note this input func
print('Hello, ' + x)

>>> 'Py' 'thon'
'Python'        #**(note that this only works with literals and no expressions/variable)**
```
#### Index of a string
```python
>>> word = 'Python'
>>> word[0]  # character in position 0
'P'
>>> word[-1]  # last character
'n'
```
#### Slicing (To obtain substring) 
1. `word[0:2]` means 0(included) to 2(excluded)
2. `word[ :4]` means all characters upto 4(excluded)
3. `word[4: ]` means all characters from 4(included) till the end.

## Lists:
```python
>>> squares = [1,4,9,16]
>>> squares[0]
1
>>> len(squares)
4
>>> squares[2] = 8      #9 replaced by 8
>>> squares[0:2] = [3,4,5]
>>> squares.append(25)
>>> squares
[3,4,5,16,25]
```
- nesting
```python
>>> a = ['a', 'b', 'c']
>>> n = [1, 2, 3]
>>> x = [a, n]
>>> x
[['a', 'b', 'c'], [1, 2, 3]]
>>> x[0]
['a', 'b', 'c']
>>> x[0][1]
'b'
```
> Date: 2/05/2021
# Control Flow tools
#### if,elif,for,range:
```python
#format for if/elif
if/elif (condition):       #brackets not necessary
                (outcome)
#for iterates over items of any sequence
numbers = [1,2,3]
for n in numbers:
      (any operation)
```
- `range(10)` gives values from 0 to 9
- `range(4,7)` gives 4,5,6
- `range(n1,n2,d)` (n1,n2,d are integers) gives numbers starting from n1 upto n2(excluded) with common diff d.
- soem operations on range function:
```python
#Input
print(range(10))      #output: range(0,10)
sum(range(4))         #output: 6
list(range(4))        #output: [0,1,2,3]
```
#### break,continue,pass:
- break and continue same like C++ (`break` breaks out of the innermost enclosing `for` or `while` loop.
- `pass` does nothing!
      
## Function Definition
```python
#format:
def function_name(parameters):
    """documentation of the function"""   # optional, indented, if multi-line, leave one line blank between 2 lines.
    body of the function                  #indented
```
- To print the docstring, use the command `print(function_name.__doc__)`
- Default argument values : eg: `def ask_ok(prompt, retries=4, reminder='Please try again!')`
Here function can be called in 3 ways: 1 with only the compulsory argument ie `propmt`, 2nd with `prompt` and `retries(with value other than 4 as well)` and 3rd with all 3.
#### Systematic way to pass positional/keyword arguments in a function using `/` and `*`:
```python
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
# Passing arguments in the above function:
f(1,2,3 or kwd=3,kwd1=something,kwd2=something)
#keyword areguments can be passed in any order.
```
#### Variable number of arguments:
- `def f(*arg)` : Variable number of non-keyword arguments.
- `def f(**kwarg)` : Variable number of keyword arguments.
#### Function annotations:
- otpional data info of arguments and return values in user-defined fn.
- format: `def f(arg1: type, arg2: type = particular_value) -> type_of_return_value:`
-                             |
                        optional argument.

> Date: 4/05/2021
# Data Structures:































