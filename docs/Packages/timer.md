This page is current as of blz v2.6

The timer package aims to help with timing parts of program execution, particularily for performance testing purposes.

### Timer
`Timer()` - Creates a new timer

Example:
```
import Timer
timer = Timer()
```

### Timer::start
`start()` - (Re)starts the timer

A timer is already started when it is created, but if you want finer control on when it is started, use this method.

Example:
```
import Timer
timer = Timer()
# Do some stuff
timer.start()
```

### Timer::seconds_elapsed
`seconds_elapsed()` - Returns a number representing the number of seconds elapsed

Example:
```
import Timer
timer = Timer()
sleep(1000)
print(timer.seconds_elapsed())
```

Sample Output:
```
21/20
```

### Timer::milliseconds_elapsed
`milliseconds_elapsed()` - Returns an integer representing the number of milliseconds elapsed

Example:
```
import Timer
timer = Timer()
sleep(1000)
print(timer.millseconds_elapsed())
```

Sample Output:
```
1000
```