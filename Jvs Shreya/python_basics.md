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

* 

