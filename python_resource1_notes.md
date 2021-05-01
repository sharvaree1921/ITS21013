## Comments:
Start with #

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

#### escaping single quote or double quote
- The character `\` is used to escape quotes.
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
>>> prefix = 'Py'
>>> prefix + 'thon'
'Python'
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




















