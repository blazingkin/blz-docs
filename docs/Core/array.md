Updated as of blz v2.6

`blz-ospl\Packages\Core\ArrayUtil.blz`

### Concatenate
`concatenate(arr)` - Returns the resulting concatenation of two arrays.

Example:
```
my_arr_A = [0, 1, 2]
my_arr_B = [3, 4, 5]
my_arr_AB = my_arr_A.concatenate(my_arr_B)
print("my_arr_AB: " + my_arr_AB)
```
Output:
```
my_arr_AB: [0, 1, 2, 3, 4, 5]
```

### Contains
`contains?(element)` - Returns true if the element is contained in the array and false otherwise.

Example:
```
my_arr = [1, 2]
print(arr.contains?(1))
```
Output:
```
true
```

### Copy Array Contents
`copy()` - Returns a copy of the array.

Example:
```
my_arr = [0, 1, 2]
my_arr_copy = my_arr.copy()
print(my_arr_copy)
```
Output:
```
[0, 1, 2]
```

### Each
`each(method)` - Takes a method and performs it on each element in the array.

Example:
```
my_arr = ["apple", "peach", "cherry"]
my_arr.each(print)
```
Output:
```
apple
peach
cherry
```

### Empty
`empty?()` - Returns true if the array is empty.

Example:
```
my_arr = []
print(my_arr.empty?())

my_arr2 = [1]
print(my_arr2.empty?())
```
Output:
```
true
false
```

### Filter
`filter(method)` - Selects the elements of the array that produce `true` when passed to the method

Example:
```
:is_even?(number)
    return number % 2 == 0
end

:main
   arr = [1,2,3,4,5,6,7]
   print(arr.filter(is_even?))
end
```

Output:
```
[2, 4, 6]
```

### Fold Left
`fold_left(accumulator, method)` - Collapses the array using the method with the accumulator and elements as parameters, from left to right.

Example:
```
:add(a, b)   #method returns the sum of a and b
    return a + b
end

my_arr = [1, 2, 3, 4, 5]
print(arr.fold_left(0, add))

print(arr.fold_left(5, add))
```
Output:
```
15
20
```

### Fold Right
`fold_right(accumulator, method)` - Collapses the array using the method with the accumulator and elements as parameters, from right to left.

Example:
```
:add(a, b)     #method returns the sum of a and b
    return a + b
end

arr = [1, 2, 3, 4, 5]
print(arr.fold_right(0, add))

print(arr.fold_right(5, add))
```
Output:
```
15
20
```

### Length 
`length()` - Returns the length of the array.

Example:
```
my_arr = [0, 1, 2, 3]
len = my_arr.length()
print("my_arr length: " + len)
```
Output:
```
my_arr length: 4
```

### Map
`map(method)` - Calls method on each element in the array.

Example:
```
my_arr = ["apple", "peach", "cherry"]
my_arr.map(print)

my_arr.map!(sort)
print(my_arr)
```
Output:
```
apple
peach
cherry
[aelpp, acehp, cehrry]
```

### Nil?
`nil?()` - Is this array nil? (spoilers no)

Example:
```
print([1].nil?())
```

Output:
```
false
```

### Remove
`remove(index)` - Removes the element at the index from the array.

Example:
```
my_arr = [0, 1, 2, 3, 4, 5, 6]
print("before remove: " + arr)
my_arr.remove!(3)
print("after removing index 3: " + my_arr)
my_arr.remove!(5)
print("after removing index 5: " + my_arr)
my_arr.remove!(0)
print("after removing index 0: " + my_arr)
arr2 = my_arr.remove(1)
print("arr2 makes a copy of my_arr and removes index 1: " + arr2)
```
Output:
```
before remove: [0, 1, 2, 3, 4, 5, 6]
after removing index 3: [0, 1, 2, 4, 5, 6]
after removing index 5: [0, 1, 2, 4, 5]
after removing index 0: [1, 2, 4, 5]
arr2 makes a copy of my_arr and removes index 1: [1, 4, 5]
```

### Reverse Array Order
`reverse()` - Reverses the order of elements in the array.

Example:
```
my_arr = [0, 1, 2, 3]
my_arr = my_arr.reverse()
print(my_arr)
```
Output:
```
[3, 2, 1, 0]
```

### Sample From Array
`sample()` - Returns a random entry in the array

Example:
```
arr = [1, 2, 3, "a", "b", "c"]
print(arr.sample())
print(arr.sample())
```

Sample Output:
```
a
2
```

### Show
`show()` - Returns a string representation of the string

Example:
```
arr = [1, 2, "a", "b"]
print(arr.show())
```

Output:
```
[1, 2, a, b]
```

### Shuffle Array Contents
`shuffle()` - Shuffles the contents of the array.

Example:
```
my_arr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
my_arr = my_arr.shuffle()
new_arr = my_arr.shuffle()         # will be my_arr shuffled again.
print("my_arr: " + my_arr)
print("new_arr: " + new_arr)
```
Output:
```
my_arr: [9, 3, 2, 1, 0, 6, 5, 7, 4, 8]
new_arr: [1, 2, 9, 6, 8, 3, 7, 4, 0, 5]
```

### Size
`size()` - Returns the size of the array.

Example:
```
my_arr = [0, 1, 2, 3]
len = my_arr.size()
print("my_arr length: " + len)
```
Output:
```
my_arr length: 4
```


### Slice
`slice(start, end)` - Returns a slice of the array indexed from `start` to, but not including, `end`.

Example:
```
my_arr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
new_arr_1 = my_arr.slice(4, 8)                     # a sub-array
new_arr_2 = my_arr.slice(0, array_length(my_arr))  # the entire array
new_arr_3 = my_arr.slice(0, 0)                     # none of the array
print("new_arr_1: " + new_arr_1)
print("new_arr_2: " + new_arr_2)
print("new_arr_3: " + new_arr_3)
```
Output:
```
new_arr_1: [4, 5, 6, 7]
new_arr_2: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
new_arr_3: []
```

### Sort by Ascending Order
`sort()` - Sorts the array in ascending order.

Example:
```
my_arr = [9, 3, 2, 1, 0, 6, 5, 7, 4, 8]
my_arr = my_arr.sort()
print(my_arr)
```
Output:
```
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

### To String
`to_string()` - Return the array as a string.

Example:
```
my_arr = [1, 2, 3, 4]
print(my_arr.to_string())
```
Output:
```
[1, 2, 3, 4]    # this is equivalent to the string "[1, 2, 3, 4]"
```

### To JSON
`to_json()` - Returns a string that is a JSON representation of the array

Example:
```
arr = [1, 2, "a", "b"]
print(arr.to_json())
```

Output:
```
[1, 2, "a", "b"]
```

### Unique
`unique()` - Returns a copy of the array with duplicate elements removed.

Example:
```
my_arr = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
my_arr = my_arr.unique()
print(my_arr)

my_arr = [2, 9, 2, 9, 9, 6, 4, 5, 9, 4, 3, 4, 6, 1, 5, 3, 4, 7, 5, 7, 8, 3]
my_arr = my_arr.unique()
print(my_arr)
```
Output:
```
[1, 2, 3, 4]
[2, 9, 6, 4, 5, 3, 1, 7, 8]
```
