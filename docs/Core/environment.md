## Introduction

blz-ospl has many environment variables they can be useful to learn things about the current state of the machine. The environment variables also contain several useful constants to save you some time when making your program.

## How to use

To access an environment variable, simply put the name of the variable inside curly braces.

For example, to get the current time you might do the following:

`time = {system.time.currenttimemillis}`

## List of environment variables

### Program Arguments

`arguments` - Arguments passed to the blz program (Array of strings)

### Time

`system.time.currenttimemillis` - The number of milliseconds since the Unix epoch (Integer)

### Operating System

`system.os.name` - The name of the operating system (String)

`system.os.version` - The version of the operating system (String)

### Process File Location

`file.path` - The full path to the currently running file (String)

`file.name` - Returns the name of the currently running file (String)

`file.location` - Returns the path of the parent directory of the currently running file (String)

### Math Constants

`pi` - The mathematical constant 𝜋 (3.1415....) (Number)

`e` - The mathematical constant e (2.718....) (Number)

### blz-ospl Runtime Information

`blz.version` - Returns the version of blz-ospl that is running (String)

`blz.runtime.stack` - Returns the current runtime stack (String)

`blz.method.stack` - Returns the current method stack (String)

`blz.context.id` - Returns the current context id (Integer)

### Text Constants

`text.newline` - The newline character (i.e. '\n', or ASCII 0xA) (String)

`text.space` - The space character ' ' (String)

`text.tab` - The tab character (i.e. '\t') (String)

`text.shift` - The shift character (String)

`text.backspace` - The backspace character (i.e. '\b') (String) 

### Nil

`blz.nil` - The "nil" constant (Nil)

### Running Process Data

`process.current.uuid` - Get the universally unique id of the currently running process (String)

`process.all` - Get the count of running processes (Integer)