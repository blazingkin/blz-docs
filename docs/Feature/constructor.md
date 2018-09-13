Constructors are part of the blz language as of version 2.5. They are used to initialize objects within the language.

We will introduce several different parts of a constructor, one at a time.

Properties
=====

A constructor can specify properties of the resulting object

For example, we can specify a `Cup` that has a few properties

```
constructor Cup
    color = "red"
    contents = "coffee"
end
```

To make a new cup and print it's color, we might do the following.

```
coffee_mug = Cup()
print(coffee_mug.color)
```


*Note* - Once an object has been created, new properties can be added outside of the constructor

For instance, we can add a weight property to our cup after it has been created.

```
coffee_mug = Cup()
coffee_mug.weight = 2
print(coffee_mug.weight)
```


Methods
=====

Just like properties, a constructor can specify methods that belong to an object.

For example, we can add a `drink` method to our `Cup` constructor.

```
constructor Cup
    color = "red"
    contents = "coffee"

    :drink
        contents = "nothing"
    end
end
```

Then, we can use this method to modify our object.

```
coffee_mug = Cup()
print("We start with " + coffee_mug.contents)
coffee_mug.drink()
print("And after drinking, we have " + coffee_mug.contents)
```

*Note* - Sometimes, variable naming can make references ambiguous, for this reason each object contains the field `this` which is a reference to itself.

This can be seen in practice here.

```
constructor Cup
    color = "red"
    contents = "coffee"

    :drink
        contents = "nothing"
    end

    :fill(contents)
        this.contents = contents
    end
end
```

Constructor Parameters
=====

To allow constructors to be dynamic in behavior, parameters may be passed. These parameters will automatically become properties of the object.

For instance, our first `Cup` constructor could be made in the following way.

```
constructor Cup(color, contents)
end
```

Now, when we create a new Cup, we can easily set the color and contents.

```
coffee_mug = Cup("red", "coffee")
tea_cup = Cup("blue", "tea")
print("The mug is filled with " + coffee_mug.contents)
print("The cup is filled with " + tea_cup.contents)
```