## Python Basics
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
* Methods of lists:
     * 
