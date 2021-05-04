##### Strings:
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
