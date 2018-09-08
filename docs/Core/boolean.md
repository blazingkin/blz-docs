# Core Boolean Functions
Boolean helper functions included in the core library.
`blz-ospl\Packages\Core\BooleanUtil.blz`

### Is nil?
`nil?()` - Checks if the value is nil (always false)

Example:
```
print(false.nil?())
```

Output:
```
false
```

### Negate
`negate()` - Negates a boolean value

Example:
```
print(false.negate())
print(true.negate())
```

Output:
```
true
false
```

### Is true?
`true?()` - Checks if the value is true

Example:
```
print(false.true?())
print(true.true?())
```

Output:
```
false
true
```

### Is false?
`false?()` - Checks if the value is false

Example:
```
print(false.false?())
print(true.false?())
```

Output:
```
true
false
```