blz has an operator called the _!_ or _bang!_ operator.

This operator allows you to choose between passing by value (default) or passing by reference (by using a `!`).

You can use the _bang!_ operator by adding an `!` to the name of a function.
e.g
* sort => sort!
* reverse => reverse!
* map => map!

Let's look at an example to see what this means.

```
array = [3, 1, 2]

# Because this call to sort doesn't use a !, the array is copied and then passed to sort
sorted = array.sort()
print("No Bang")
print("Sorted: " + sorted)
print("Original " + array)
print("")

# The bang! operator passes a reference to our array
bang_sorted = array.sort!()
print("With Bang")
print("Sorted: " + bang_sorted)
print("Original: " + array)
```

The output looks like this
```
No Bang
Sorted: [1, 2, 3]
Original: [3, 1, 2]

With Bang
Sorted: [1, 2, 3]
Original: [1, 2, 3]
```

As you can see, using the _bang!_ operator lets the sort function modify our original array.