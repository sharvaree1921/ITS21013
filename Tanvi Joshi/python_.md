### Strings:
- strings can be enclosed in single quotes ` '...' ` or double quotes ` "..." `
- `\` is used to escape double quotes
- The string is enclosed in double quotes if the string contains a single quote and no double quotes, otherwise it is enclosed in single quotes.
- \n produces a new line
- `print('text')` prints `text`; omits the enclosing quotes; prints escaped and special characters; if `\` is not to be interpreted as a special character(to be printed just as it it), use raw strings by adding `r` before the first quote 
- eg: `>>> print('C:\some\name')  # here \n means newline!`
- `C:\some`
- `ame`
- `>>> print(r'C:\some\name')  # note the r before the quote`
- `C:\some\name`
- strings spanning lines: using triple quotes `""" text """` or `'''text'''`, end of lines are automatically included in the string, but it’s possible to prevent this by adding a `\` at the end of the line
- Strings can be concatenated (glued together) with the `+` operator, and repeated with `*`; consecutive string literals automatically concatenated; to concatenate variables or a variable and a literal use `+` only (no automatic)
- strings can be indexed(index less than length of string), 1st char has index 0 ( if `word='Python'`, `word[0]` gives `'P'`), negative indices mean counting from right
- slicing: get substrings, ( `word[0:2]` gives `'Py'` (characters 0(included) to 2(excluded)), `word[2:5]` gives `'tho'` (characters 2(included) to 5(excluded)) ); default: omitted 1st index means 0, omitted 2nd index means uptil and including end of string (`word[-2:]` gives `on`, -2 is 2nd last and NOT 3rd last)
- out of range slice indexes are handled in slicing, strings cannot be changed (immutable), assigning to an indexed position in the string gives error
- `len(string_name)` returns length of string

[Functions](https://docs.python.org/3/library/stdtypes.html#string-methods "functions on strings")
##### lists:
- they are mutable(elements can be changed), unlike strings
- elements can be added to end of list using `list_name.append(element)1
- The keyword argument end can be used to avoid the newline after the output
- You can also add new items at the end of the list, by using the append()
##### loops
- `if/elif`
- `range(0, 10, 3)` numbers from 0 to less than 10, incremented by 3; if instead of ,3 nothing is mentioned it means 1
- gives `0, 3, 6, 9`
- `print(range(10))`
- gives `range(0, 10)`
- `sum(range(4))` gives `6`
- `print(range(10))` gives `range(0,10)`
- `sum(range(4))` gives `6`
- `list(range(4))` gives the complete as a list `[0,1,2,3]`
- `break` causes loop to end abruptly, `continue` brings back to starting of loop, `pass` does nothing
##### functions:
- defined by: `def function_name(parameters):`
-             `body`(must be indented, 1st line may be a docstring)
- functions with no return statement return `None` (can be visible using print)
- cannot put non-keyword argument(positional) after a keyword argument in the function parameters when calling the function 
- Example: `def parrot(voltage, state='a stiff', action='voom', type='Norwegian Blue'):`
- `print("-- This parrot wouldn't", action, end=' ')`
- `print("if you put", voltage, "volts through it.")`
- `print("-- Lovely plumage, the", type)`
- `print("-- It's", state, "!")`
- `parrot(voltage=5.0, 'dead')` this call to the function is wrong
- `*arguments` mean a set of strings as parameter, `**keywords` mean a set of variables which have been assigned a string each(printing the variable prints variable name, `keyword[variablename]` prints string assigned to variable
- `def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):`
- `    -----------    ----------     ----------`
- `      |             |                  |`
- `      |        Positional or keyword   |`
- `      |                                - Keyword only`
- `       -- Positional only` 
- `lambda` keyword creates small anonymous function
### Data Structures
- `list.append(x)` adds x(element) to the end of list, `list,extend(list2)` add all elements from list2 to the end of list, `list.insert(i,x)` insert x at ith index, `list.remove(x)` remove 1st time x appears, `list.pop([i])` remove item at ith position and return it, `list.pop()` removes and returns last element, `list.clear()` remove all items from list, `list.index(x[, start[, end]])` return index of 1st x (start and end can limit the search to a subsequence of the list), `list.count(x)` times x appears, `list.sort(*, key=None, reverse=False)` sort items in place, `list.reverse()` reverse elements, `list.copy()` return copy of list.
- `zip(*)` function
- `del list[i]` deletes ith element from list, returns nothing, `del list[i:j]` deletes ith,..(j-1)th elements
- 
