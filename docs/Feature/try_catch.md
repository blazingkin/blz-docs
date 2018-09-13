Some operations in blz will create an error.

These can be recovered from using a try-catch block.

Example:
```
try
    print(1 / 0) # You can't divide by 0, this is an error
catch error
    print("Oops! An error occurred")
    print(error)
end
```

Or more realistically, perhaps you are parsing JSON

```
import JSON
try
    json = "[1, 2, 3" # Oops, no closing bracket. This JSON is invalid
    parsed = parse_json(json)
    do_something_with(parsed)
catch json_error
    print("Provided JSON was invalid!")
    do_something_with([])
end
```

Any kind of object can be thrown as an error, so make sure to check the documentation of the library used to see what kind of object you should handle.

To create an error, you can use the `throw` keyword.

For example

```
:divide(numerator, denominator)
    if denominator == 0
        throw "Denominator was 0" # Raise an exception
    end
    # If the denominator is not 0, then proceed with the division
    numerator / denominator
end
```