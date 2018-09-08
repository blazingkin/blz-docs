This page is updated as of blz v2.6

The JSON package allows for parsing JSON strings into blz objects.




### Parse JSON
`parse_json(string)` - parses string into a blz object, or throws JSONError

Example
```
json_string = "\"im a string!\""
print(parse_json(json_string))
```

Output
```
im a string!
```

Example 2:
```
json_string = "[1, 2, 3]"
print(parse_json(json_string))
```

Output 2:
```
[1, 2, 3]
```

Example 3:
```
json_string = "{\"key\": [1,2,3]}"
print(parse_json(json_string))
```

Output 3:
```
{key=[1, 2, 3]}
```

Example 4:
```
parse_json("Invalid JSON!!!")
```

Output 4:
```
JSON Error: Expected some JSON token, but reached end of string instead
```


### Constructor JSONError

Has fields
    - `message` - with the error message
    - `type` - "JSON" string literal