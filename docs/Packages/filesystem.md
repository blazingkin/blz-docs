This page is updated as of blz v2.6

The FileSystem package allows for creation of resources.

Resources are currently either a file, or a network request.

**All operations to read from/write to resources are handled in the [Core/Resource](../../Core/resource) section**

### Open
`open(filepath, mode="r")` - Opens the file at filepath. Either an absolute path, or relative to the PWD of the program.

Mode - Modes can contain any of the following:
    * "r" - Read
    * "w" - Write
    * "c" - Create if it doesn't exist

Example:
```
import FileSystem
try
    file = open("testfile.dat", "cw")
    file.write("This is written to the file!\n")
    file.close()

    samefile = open("testfile.dat")
    contents = samefile.read_all()
    print(contents)
catch file_error
    print("Some file error occured! " + file_error)
end
```

### Open Http
`open_http(path, mode="r")` - Opens an http connection to the given path.

Currently only supports reading.

It is strongly recommended that you use open_https unless your endpoint does not support https

Example
```
import FileSystem
try
    response = open_http("google.com").read_all()
    print(response)
catch network_error
    print(network_error)
end
```

### Open Https
`open_https(path, mode="r")` - Opens an https connection to the given path.

Currently only supports reading.

Example
```
import FileSystem
try
    response = open_https("google.com").read_all()
    print(response)
catch network_error
    print(network_error)
end
```
