This page is updated as of blz v2.6

The Lists package aims to contain standard List data structures.

## Range
`range(end)` - Returns an array containing all integers `[0, end)`

`range(start, end)` - Returns an array containing all integers `[start, end)`

Example:
```
import Lists
print(range(2))
print(range(2, 5))
```

Output:
```
[0, 1]
[2, 3, 4]
```

## Iterator
`Iterator(array)` - Creates an iterator over an array

### Iterator::has_next?
`has_next?()` - Returns a boolean if the iterator has a next element

Example:
```
import Lists
it1 = Iterator([])
it2 = Iterator([1])
print(it1.has_next?())
print(it2.has_next?())
```

Output:
```
false
true
```

### Iterator::next
`next()` - Returns the next element

Example:
```
import Lists
it = Iterator([1, 2, 3])
print(it.next())
print(it.next())
print(it.next())
```

Output:
```
1
2
3
```

### Iterator::remaining
`remaining()` - Returns the remaining part of the list

Example:
```
import Lists
it = Iterator([1, 2, 3])
print(it.remaining())
it.next()
print(it.remaining())
it.next()
print(it.remaining())
it.next()
print(it.remaining())
```

Output:
```
[1, 2, 3]
[2, 3]
[3]
[]
```

## LinkedList
`LinkedList(value)` - Creates a LinkedList with 1 element (value)

You can access the first elements value using `list.value` and the tail of the list using `list.next`

### LinkedList::add
`add(value)` - Adds the value to the end of the linked list

Note this is an `O(n)` operation

Example:
```
import Lists
list = LinkedList(1)
print(list)
list.add(2)
print(list)
```

Output:
```
1
1, 2
```

### LinkedList::add_at_beginning
`add_at_beginning(value)` - Adds the value to the beginning of a linked list

Note this is an `O(1)` operation

**NOTE: This operation does not mutate, you must use reassignmnet**

Example:
```
import Lists
list = LinkedList(1)
print(list)
list = list.add_at_beginning(0) # Must use reassignment
print(list)
```

Output:
```
1
0, 1
```

### LinkedList::length
`length()` - Returns the length of the linked list

Note this is an `O(n)` operation

Example:
```
import Lists
list = LinkedList(1)
print(list.length())
list.add(2)
print(list.length())
```

Output:
```
1
2
```