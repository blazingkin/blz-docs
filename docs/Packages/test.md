This page is updated as of blz v2.6

The test package aims to help users write tests for their programs.

The entire package revolves around one method `expect`

## Expect
`expect(value, exit_on_failure=true)` - Declaration of a value to be tested

If exit_on_failure is true and an assertion fails, the program will exit with error code 1.

See below for examples

### Expect::is
`expect(value).is(other)` - Asserts that two values are equal

Example:
```
import Test
expect(2 + 2).is(4)
expect([1, 2, 3]).is([1, 2, 3])
expect("hi").is("bye") # Will fail and exit the program
```

### Expect::is_not
`expect(value).is_not(other)` - Asserts that two values are not equal

Example:
```
import Test
expect(2 + 2).is_not(5)
expect("one string").is_not("another")
```

### Expect::is_greater_than
`expect(value).is_greater_than(another)` - Asserts that a value is greater than or equal to another

Example:
```
import Test
expect(4).is_greater_than(3)
expect("b").is_greater_than("a")
expect(4).is_greater_than(4) 
expect(5).is_greater_than(6) # Will fail and exit the program
```

### Expect::is_less_than
`expect(value).is_less_than(another)` - Alias for `expect(another).is_greater_than(value)`

### Expect::to_be
`expect(value).to_be(another)` - Alias for Expect::is

### Expect::to_not_be
`expect(value).to_not_be(another)` - Alias for Expect::is_not

### Expect::is_not_nil
`expect(value).is_not_nil()` - Alias for `expect(value).is_not({blz.nil})`

### Expect::is_nil
`expect(value).is_nil()` - Alias for `expect(value).is({blz.nil})`

### Expect::is_true
`expect(value).is_true()` - Alias for `expect(value).is(true)`

### Expect::is_false
`expect(value).is_false()` - Alias for `expect(value).is(false)`