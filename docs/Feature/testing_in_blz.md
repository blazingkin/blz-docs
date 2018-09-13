blz has builtin support for writing tests as of version 2.6. This comes in two different forms.

* The Test package
* The -test flag

## The Test package

This package can be imported by simply using
`import Test`

It uses a 'Domain Specific Testing Language' to make tests readable.

Currently, all assertions begin with the method `expect`.

For example, to assert that 2 + 2 is 4, you might use `expect(2 + 2).is(4)`

More complete documentation of this package will be available closer to the release of v2.6

## The -test flag

To run blz in 'test' mode, simply run using the `-t` or `-test` flag.

For example, if I want to test 2 files, Math.blz and Net.blz, I'd run `blz -t Math.blz Net.blz`

This will run every method in these files that starts with `test`.

For example, Math.blz might have a method such as the following
```
import Test
:test_two_plus_two()
    expect(2 + 2).to_be(4)
end
```

And running blz with the -t flag will run this method automatically because of the way it is named.