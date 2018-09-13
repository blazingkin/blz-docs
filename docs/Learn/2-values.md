**Lesson 2: Values**

A core idea in programming languages is *values*. This is some kind of data that you want to store or manipulate.

blz has several kinds of built in values:

 * **Numbers** - integers, decimals, fractions (e.g. `1`, `2`, `1/2`, `3.141`)
 * **Strings** - a.k.a. text. Some characters wrapped around quotes (e.g. `"Hello World"`)
 * **Booleans** - The answer to a yes / no question. Either `true` or `false`
 * **Arrays** - An ordered list. Comma seperated and in square brackets. (e.g. `[1, 2, 3]`)
 * **Hash** - Stores a 'value' which is accessed with a 'key'
 * **Objects** - Used to give names to data
 * **Resources** - Used for reading / writing to a file or making network requests
 
In this section, we will just be learning about Numbers, Strings, and Booleans


### Numbers

There are 3 kinds of numbers:

 * Integers - a whole number; 1, 2, 20, -13, etc.
 * Doubles - a number with a decimal point; 1.2, -0.21, 3.141592, 1.414
 * Fractions - a number with an integer numerator and denominator; 1/2, -2/3, 5/6, etc.

In most cases, blz treats all numbers equally. Any exceptions should be pointed out explicitly.

There are several standard operations that you can do with numbers.

Open up the blz interactive mode by running `blz -i` to follow along. You can exit at any time by typing `exit`.

Numbers can be added (+) or subtracted (-)

```
> 2 + 2
4
> 2.2 + 3 + 4
9.2
> 1/2 + 1/3
5/6
> 5/2 - 1
3/2
> 2 - 5
-3
```

Numbers can be multiplied (\*) or divided (/)

```
> 2 * 4
8
> 0.1 * 10
1.0
> 1/10 * 10
1
> (1/10) / 10
1/100
```

*Note - You can use parenthesis () to group the order of expressions*

You can use exponentiation (\*\*) or logarithms (\_\_ *two underscores*)

```
> 2 ** 3
8
> 2 ** 0.5
1.414213562373133720883631
> 100 __ 10
2.000000000000039
> 50 __ {e}
3.9120230054281
```

*Note - {e} is a shortcut for the base of the natural logarithm. It is about 2.718*

You can compare numbers using less than (<), greater than (>), less than or equal (<=), greater than or equal (>=), or equals (==)

```
> 2 + 2 < 4
false
> 2 + 2 <= 4
true
> 2 * 4 > 3
true
> 2 * 4 >= 200
false
> 2 * 4 == 4 * 2
true
```

### Strings

Strings are a list of characters, one after another.

They are denoted by putting double quotes (`"`) around some text.

Use the interactive mode (`blz -i`) to follow along.

You can declare some strings

```
> "Hello!"
Hello!
> "Test 1, 2, 3"
Test 1, 2, 3
> "A new line can be added using \n See?"
A new line can be added using
 See?
```

*Note, the `\` character lets you put in special characters. `\n` is the most common*

Strings can be added

```
> "Strings " + "together"
Strings together
> "I " + "can " + "add "+ "multiple " + "strings!"
I can add multiple strings!
```

You can see what character is at a particular *index* of a string by using the array lookup (`[]`) operator

```
> "Test"[0]
T
> "Test"[1]
e
> "Test"[2]
s
> "Test"[3]
t
> "Test"[4]
Error occurred on line 1
Out Of Bounds! Tried to access index 4 of string Test
There was an issue running your last command
Type 'err' to see the error
```

Wow! A lot just happened. Let's try to break that down.

**Why did we start at 0?**

All index operations in blz (and most programming languages) count 0 as the first element

**What happened when we tried to access the 4th index (5th character)?**

By accessing the 4th index, we end up reading the 5th character (since 0 is an index). Well, the string "Test" only has 4 characters. So the 4th index is undefined.

An error happened! So blz tried to give a helpful error message to tell you what went wrong.

### Booleans

Booleans are simply the answer to a yes or no question.

That is, they are either `true`, or `false`

We can perform a [logical and](https://en.wikipedia.org/wiki/Logical_conjunction) (&&) or a [logical or](https://en.wikipedia.org/wiki/Logical_disjunction) (||)

```
> true && false
false
> true && true
true
> false || false
false
> true || false
true
```