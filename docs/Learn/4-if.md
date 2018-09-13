**Lesson 4: If**

### Code Blocks

Sometimes, we need to put several statements together in a *block*.

This seperates the code into an organized unit.

We often indent this block to make it easier to read.

It will look something like this

```
BLOCK HEADER
    BLOCK LINE 1
    BLOCK LINE 2
    BLOCK LINE 3
    ...
end
```

In blz, you always close blocks with the keyword `end`

### If

Sometimes you only want to execute code *if* some condition is true. That is, a boolean value is true.

Let's try it out. The `if` line is a block header, so we'll need an end

Here's a sample program

```
if 2 + 2 == 4
    print("2 + 2 = 4!")
end

if 2 + 2 == 5
    print("2 + 2 = 5?")
end

if true || false
    print("Either true or false was true!")
end
```

It's output
```
2 + 2 = 4
Either true or false was true!
```

As you can see, since 2 + 2 != 5, the second block was not executed.