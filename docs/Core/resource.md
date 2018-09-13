Updated as of v2.6

These are methods that you can perform on already open resources. This could be an open file, an open tcp connection, etc.

`blz-ospl\Packages\Core\ResourceUtil.blz`

### Close
`close()` - Closes a resource

Example:
```
import FileSystem
file = open("/", "r")
file.close()
```

### Has Next
`has_next?()` - Checks if the resource has anything more to read

Example:
```
import FileSystem
file = open("/", "r")
print(file.has_next?())
file.read_all()
print(file.has_next?())
```

Output:
```
true
false
```

### Next
`next()` - Reads the next unit from a resource (usually a byte)

Example:
```
import FileSystem
file = open("/", "r")
print(file.next())
```

Output:
```
b
```

### Read All
`read_all()` - Reads all the contents of a resource and returns it

Example:
```
import FileSystem
file = open("/lorem_ipsum", "r")
print(file.read_all())
```

Output:
```
Neque porro quisquam est qui dolorem
ipsum quia dolor sit amet, consectetur,
adipisci velit
```

### Read Lines
`read_lines()` - Reads all contents of a resource and converts to an array where each entry is a line in the resource

Example:
```
import FileSystem
file = open("/lorem_ipsum", "r")
print(file.read_lines())
```

Output:
```
["Neque porro quisquam est qui dolorem", "ipsum quia dolor sit amet, consectetur,", "adipisci velit"]
```

### Write
`write(message)` - Writes contents to a resource

Example:
```
import FileSystem
file = open("/tmp/file", "cw")
file.write("this is only a test\n")
file.close()
```