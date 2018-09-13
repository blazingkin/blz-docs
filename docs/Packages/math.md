This page is updated as of blz v2.6

# Math Functions
`blz-ospl\Packages\Math`

### Absolute Value
`abs(x)` - Returns the absolute value of x.

Example:
```
print(abs(-1))
print(abs(1))
```
Output:
```
1
1
```

### Ceiling
`ceil(x)` - Returns the most negative value that is greater than or equal to the argument and is equal to a mathematical integer.

Example:
```
print(ceil(20.123))
print(ceil(20))
print(ceil(-4))
```
Output:
```
21.000
20
-4
```

### Sine
`sin(x, series_terms=10)` - Uses the taylor series to estimate the sine of x

`sine(x, series_terms=10)` - Alias for sin

REPL Example:
```
> sin({pi})
-5.2766142900984368597313941528129E-10
> sin({pi}/2)
0.99999999999999974410647080493330636301677176084
```

### Cosine
`cos(x, series_terms=10)` - Uses the taylor series to estimate the cosine of x

`cosine(x, series_terms=10)` - Alias for cos

REPL Example:
```
> cos({pi})
-1.00000257598757145040413463536951038353
> cos({pi}/2)
-5.2766142900984368597313941528129E-10
```

### Tangent
`tan(x, series_terms=10)` - Uses the taylor series to estimate the tangent of x

`tangent(x, series_terms=10)` - Alias for tan

### Cotangent
`cot(x, series_terms=10)` - Uses the taylor series to estimate the cotangent of x

`cotangent(x, series_terms=10)` - Alias for cot