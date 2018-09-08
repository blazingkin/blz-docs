This is current as of v2.6

import using `import CSV`

### parse_csv
`parse_csv(string)` - Parses a csv string into a 2 dimensional array

The outer array is of rows, the inner arrays are of columns

Example:
```
import CSV
print(parse_csv("a,b,c"))
print(parse_csv("1,2,3\n4,5,6"))
```

Output:
```
[[a, b, c]]
[[1, 2, 3], [4, 5, 6]]
```

Please note, this can throw an error if you pass a non-string.