This page is current as of v2.6

`blz-ospl\Packages\Core\StandardIO.blz`


### Print

`print(x)` - Prints a string with a new line character following

Example:

```
print("Hello world")
print("This is from blz")
```

Output:

```
Hello world
This is from blz
```
### Print No Newline

`print_no_newline(x)` - Prints without appending a newline character

Example:
```
print_no_newline("Hello ")
print_no_newline("World")
```

Output:
```
Hello World
```

### Number Input
`number_input()` - returns an integer or decimal number input by the user

Example:
```
user_input = number_input()
# Execution stops until user inputs 5
print(user_input + 2)
```

Output:
```
7
```

### String Input
`string_input()` - returns a string input by the user

Example:
```
user_input = string_input()
# Execution stops until user inputs Hi there
print(user_input)
```

Output:
```
Hi there
```

### Exit
`exit(code)` - Exits execution of the program with the resulting code

Example:
```
exit(3)
print("test")
```

Output:
```
```

Program will exit with code 3

### Raw Print
`raw_print(int)` - Print the ascii representation of a character

Example:
```
raw_print(65) # Decimal 65 is ascii capital A
```

Output:
```
A
```

### Sleep
`sleep(milliseconds)` - Suspends execution for the given number of milliseconds

Example:
```
print(1)
sleep(1000) # Wait for a second
print(2)
```

Output
```
1
2
```

There will be a second pause between the 1 and the 2