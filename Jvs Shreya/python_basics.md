# Python Basics
Date: 30-04-2021, Time: 12:44

### 1.1 Numbers, Strings, Lists

* All the mathematical operations are same. For power use ** symbol. For remainder use %.
* There is no need to end a line explicitly. No need to specify data-type of variables as long as they are assigned some value.
* For strings, use '...' or "...". To print use `print()`. To include ' as part of string, use \ before it. For new line use `\n`. To include \n in string use `print(r'...\n...')`. 
* When a variable is assigned a string, it beacomes a 1D array. For length use `len(string_name)`. To split, use string_name[2:6] where 6 is excluded. Negative indices start from the last letter.
* Such a variable cannot be reassigned with a different character. Strings can be added and multiplied.
* Lists also are similar but lists can be reassigned and lists can have sublists (2D arrays). The `append()` can be used to add to the list.

```python
x = 5**2 + 3.5000
print(x)
print('"Hi! I\'m trying to learn python." she said. \n "Ok" I replied.')
print(r"Directory: Home\pyhton\new_file")

y = 'Taylor Swift'
z = y[7:] + 'ie :)'
print(y[0:3]*2 + ' is awesome!' + '\nI am a ' + z)
print(y[-3]+z[-1:100]) # Note that just z[100] will give an error but it can be used while splitting.

list = [2, 0, 2, 0, 'I', 'I', 'T']
print(list[4:])
list.append('B') 
list[3] = 1
list.append([1,2,3,4])
print(list[:4]+list[8])
```
Output:
```
28.5
"Hi! I'm trying to learn python." she said. 
 "Ok" I replied.
Directory: Home\pyhton\new file
TayTay is awesome!
I am a Swiftie :)
i)
['I', 'I', 'T']
[2, 0, 2, 1, 1, 2, 3, 4]
```
### 1.2 Control Flow Terms

* Same concept of loops like `while`, `for`, `if`, `elif` will apply. The `range()` lists all numbers between the given bracket. The `break` and `continue` statements can be used. `pass` statement is used to do nothing.
* Functions are defined with `def`. No need to mention data-types.
* Two kinds of arguments - keyword and positional arguments. Keyword arguments must always follow positional arguments. To separate them, use `/` (everything preceding this will be positional) and `*` (everything following this is keyword) . 
* Use `*name` to take in a 'tuple' i.e. multiple positional arguments. Use `**name` to take multiple keywords.
* `lambda` can be used to define small functions. Annotations are useful in documenting the program and keeping it organized.
```python
a,b = 0,1
while a < 100 :
  a,b = b,a+b
  print(a, end=' ')
  
for n in range(2, 9):
     for x in range(2, n):
            if n % x == 0:
                print(n, 'equals', x, '*', n//x)
                break
     else:
         # loop fell through without finding a factor
                print(n, 'is a prime number')
                
def cheeseshop(kind, *arguments, **keywords):
    print("-- Do you have any", kind, "?")
    print("-- I'm sorry, we're all out of", kind)
    for arg in arguments:
        print(arg)
    print(arg[2])
    print("-" * 40)
    for kw in keywords:
        print(kw, ":", keywords[kw])
cheeseshop("Limburger", "It's very runny, sir.", [1,2,3,4], shopkeeper="Michael Palin", client="John Cleese", sketch="Cheese Shop Sketch")

def make_incrementor(n):
     return lambda x: x + n
f = make_incrementor(10)
f(3)

def f(ham: str, eggs: str = 'eggs') -> str:
     print("Annotations:", f.__annotations__)
     print("Arguments:", ham, eggs)
     return ham + ' and ' + eggs
f('spam')
```
Output:
```
1 1 2 3 5 8 13 21 34 55 89 144 
2 is a prime number
3 is a prime number
4 equals 2 * 2
5 is a prime number
6 equals 2 * 3
7 is a prime number
8 equals 2 * 4
-- Do you have any Limburger ?
-- I'm sorry, we're all out of Limburger
It's very runny, sir.
[1, 2, 3, 4]
3
----------------------------------------
shopkeeper : Michael Palin
client : John Cleese
sketch : Cheese Shop Sketch
13
Annotations: {'ham': <class 'str'>, 'return': <class 'str'>, 'eggs': <class 'str'>}
Arguments: spam eggs
'spam and eggs'
```
### 1.3 Data Structures
* Methods of lists(Note:- [] means optional):
   * `append(x)` - adds at end, `extend(iterable)` - adds many at end, `insert(i, x)` - inserts in between, `remove(x)` - removes that value the first time it occurs, `pop([i])` - removes and returns value at that position, `clear()` - clears entire list, `index(x[, start[, end]])` - gives index of value x, `count(x)` - number of times x comes, `sort(\*, key=None, reverse=False)` - sorts list, `reverse()` - reverses list, `copy()` - same as a[:]
* Lists can also be interpreted as stacks(append, pop) or queues(append, popleft i.e. first entry leaves).
* Lists can be created in short forms()comprehensions using for and if. Ex:-  
  ``` python 
  [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
  ``` 
  is equivalent to
  ``` python
  combs = []
  for x in [1,2,3]:
      for y in [3,1,4]:
          if x != y:
              combs.append((x, y))
  combs
  ```
  Ex 2 :-
  ``` python
  matrix = [
     [1, 2, 3, 4],
     [5, 6, 7, 8],
     [9, 10, 11, 12],
  ]
  [[row[i] for row in matrix] for i in range(4)]
  ```
  Output:
  ```
  [[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
  ```
  (The `zip()` function does the above thing)
* `del` deletes stuff without returning.
* Tuples can contain multiple values of any data-type. For empty tuple - `()`, for singleton end with comma. Values of a defined tuple cannot be changed. They can be unpacked like this:- ` x, y, z = t` where t can be `[23,4,'hi']`.
* Sets are unordered collection made by `{1,2,3}` or `set(1,2,3)`.  For empty set - `set()`. If a,b are sets,
   * **a - b** - in a but not b, **a | b** - union, **a & b** - intersection, **a ^ b** - a or b but not both.
* Dictionaries are a set of *(immutable) keys : value* pairs. `list(d)` give list of all keys. `dict()` constructor creates dictionary from a comprehension. 
* `.items()` is used to get both the pairs in loops. `'reversed()'` and `sorted()` can be used for sequences in loops. Sequences can be compared in lexicographic order.
* A boolean expression is evaluated from lest to right and is terminated when the result is determined. When a variable is assigned a boolean expression, it returns the last evaluated value. 
 ```python
 questions = ['name', 'favorite color']
 answers = ['lancelot', 'blue']
 for q, a in zip(questions, answers):
     print('What is your {0}?  It is {1}.'.format(q, a))
 ```
 Output:
 ```
 What is your name?  It is lancelot.
 What is your favorite color?  It is blue.
 ```
 ### 1.4 Modules
 * These are like header files in cpp. Use `import` to call them. To get specific functions from module, use `from` mod `import` func. To import all funcs, use `*`. To change the name, use `as`.
 * To run a module as a *script* use the following code:  
    ```python
    if __name__ == "__main__":
    import sys
    mod(int(sys.argv[1]))
    ```
 * When we import a module, python first searches the directory, _path_ variable, and then installation-dependent default. After initialization, Python programs can modify sys.path by putting the directory name at the start of the address.
 *  Python caches the compiled version of each module in the  __ pycache __ directory under the name module.version.pyc, where the version gives the Python version used.
 *  Python has some default modules and libraries like `sys`. The `dir()` function lists all names(except built-in functions) defined in that module. For built-in, use `import builtins` and then `dir(builtins)`.
 *  Packages structure the modules. These are done in a dotted format. Ex:-  
    ```python
    ITSP/
         __init__.py
         python/
                __init__.py
                basics.py
                libs.py
                ...
         ml/
            __init__.py
            images.py
    ```
    And to access libs, use `import ITSP.python.libs`. Again, `from` ... `import` can be used.
 *  When * is used while importing a package, it will import all the sub-modules only if `__all__` is defined in `__init__.py`and it contains all the sub-modules. Else, it will import only till the package level.  

    >__Note:- Using * to import all is *not* recommended.__
 *   When a module is already imported from a package, but you want another module from same package, you can just use dots. `from . import func2`.
> 09-05-2021, 00:21 AM

### 1.5 Input and Output
* To print values of variables, enclose them in {...} and put`f` or `F` before the start of the string. Another way:  
   ```python
   x,y,z='hello',5,'yay'
   '{:8}. I got {:-7}. {:15}!'.format(x,y,z)
   ```
   Output:
   ```
   'hello   . I got       5. yay            !'
   ```
* The `str()` function simply prints the string form of the variable. The `repr()` functon includes backslashes and single quotes as part of text. Placeholders like `$x` can also be used.
* Number after `:` tells min width of string. To convert, use - `!a` for ascii(), `!r` for repr(), `!s` for str(). Ex:  
  ```python
  table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
  for name, phone in table.items():
      print(f'{name:10} ==> {phone:10d}')
  print('Jack: {0[Jack]:d}; Sjoerd: {0[Sjoerd]:d}; Dcab: {0[Dcab]:d}'.format(table)) 
  #The [] gives access to key. Same output obtained when {Jack:d} and .format(**table) is used.
      
  print('The story of {1}, {0}, and {other}.'.format('Bill', 'Manfred', other='Georg')) 
  
  import math
  print('The value of pi is approximately %5.3f.' % math.pi) #Here, 5 is width of string, 3 is precision. % replaces with value specified.
  ```
  Output:
  ```
  Sjoerd     ==>       4127
  Jack       ==>       4098
  Dcab       ==>       7678
  Jack: 4098; Sjoerd: 4127; Dcab: 7678
  The story of Manfred, Bill, and Georg.
  The value of pi is approximately 3.142.
  ```
* `str.rjust(5)` right justifies with 5 places to the left. Similarly, `str.ljust()`, `str.center()`. `str.zfill(6)` makes sure there at least 6 chars in number by adding preceding zeroes.
* To open a file, use `open('filename','r')`. Here the second char says what to do with file-  
   * `r` - read(default), `w` - write(from scratch), `a` - append, `r+` - read and write
* IMPORTANT: Normally files are read in txt form. But any file which contains other than text, use `'b'` to read it in binary format.
* Use `with` keyword to always close a file. Or use file.close() at end. But always close a file!
* `f.read()` reads entire file. `f.readline()` - each line. `list(f)` and `f.readlines()` reads all. `f.write('bla\n')` returns number of bytes entered. `f.tell()` gives currnet (bytes)position. `f.seek(offset, whence)` changes current position to offset + starting point which is start if whence is 0, current if 1 and end if 2.  
  seek doesn't work well with text only files.
* 
