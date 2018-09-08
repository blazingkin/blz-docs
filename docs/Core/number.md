# Core Numeric Functions
The blz core standard library comes with some built in methods that you can perform on numbers.
`blz-ospl\Packages\Core\NumberUtil.blz`

### Is nil?
`nil?()` - Returns if a number is nil (Always false)

Example:
```
is_nil = (3).nil?()
print(is_nil)
```

Output:
```
false
```

### To Double
`to_double()` - Coerces a number to be a double

Example:
```
print((3/2))
print((3/2).to_double())
```

Output:
```
3/2
1.5
```

### Floor
`floor()` - Performs the mathematical floor operation

Example:
```
print({pi}.floor())
print((5).floor())
```

Output:
```
3
5
```

### Ceil
`ceil()` - Performs the mathematical ceiling operation

Example:
```
print({pi}.ceil())
print((5).ceil())
```

Output:
```
4
5
```