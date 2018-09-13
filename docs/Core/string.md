# Core String Functions
`blz-ospl\Packages\Core\StringUtil.blz`

These are some core string functions that are included in the Core package.

### Contains?
`contains?(substring)` - Checks if a string contains a substring

Example:
```
string = "hello"
print(string.contains?("he"))
print(string.contains?("hi"))
```

Output:
```
true
false
```

### Is Number?
`is_number?()` - Checks if a string is a number

Example:
```
print("123".is_number?())
print("123.123".is_number?())
print("hi!".is_number())
```

Output:
```
true
true
false
```

### Length
`length()` - Returns the length of a string

Example:
```
print("".length())
print("asdf".length())
print("four".length())
```

Output:
```
0
4
4
```

### Nil?
`nil?()` - Is this value nil (no it's not)

Example:
```
print("".nil?())
print("asdf".nil?())
```

Output:
```
false
false
```

### Slice
`slice(start, end)` - Slices a string between these indices

Example:
```
print("abc".slice(0,0))
print("abc".slice(0,1))
print("abc".slice(0,3))
```

Output:
```

a
abc
```

### Sort
`sort()` - Sorts a string based on unicode order

Example:
```
print("abc".sort())
print("cab".sort())
print("321abc".sort())
```

Output:
```
abc
abc
123abc
```

### To Array
`to_array()` - Converts a string to an array of singleton strings

Example:
```
print("".to_array())
print("abc".to_array())
```

Output:
```
[]
["a", "b", "c"]
```

### To Number
`to_number()` - Converts a string to a number (if it is one). Undefined for non-numbers

Example:
```
print("123".to_number())
print("008675309".to_number())
```

Output:
```
123
8675309
```

### To String
`to_string()` - Does nothing

Example:
```
print("This is useless".to_string())
```

Output:
```
This is useless
```

### Trim
`trim()` - Trims whitespace on the end of the string

Example:
```
print("    asdf".trim())
```

Output:
```
asdf
```