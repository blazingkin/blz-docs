This page is updated as of blz v2.7

The DataStructures package contains many commonly used data structures.

### Stack
`Stack()` - Creates a new stack

Example:
```
import DataStructures
s = Stack()
```


### Stack::push
`push(item)` - Pushes an item on to the stack

Example:
```
import DataStructures
s = Stack()
s.push("a")
s.push("b")
print(s)
s.push("c")
print(s)
```

Output:
```
[a, b]
[a, b, c]
```

### Stack::pop
`pop()` - Pops an item off of the stack

Example:
```
import DataStructures
s = Stack()
s.push("a")
s.push("b")
s.push("c")
print(s.pop())
print(s.pop())
```

Output:
```
c
b
```