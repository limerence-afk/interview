In .NET, there are two categories of types, _reference types_ and _value types_.

Structs are _value types_ and classes are _reference types_.

The general difference is that a _reference type_ lives on the heap, and a _value type_ lives inline, that is, wherever it is your variable or field is defined.

A variable containing a _value type_ contains the entire _value type_ value. For a struct, that means that the variable contains the entire struct, with all its fields.

A variable containing a _reference type_ contains a pointer, or a _reference_ to somewhere else in memory where the actual value resides.

This has one benefit, to begin with:

-   _value types_ always contains a value
-   _reference types_ can contain a _null_-reference, meaning that they don't refer to anything at all at the moment

Internally, _reference type_s are implemented as pointers, and knowing that, and knowing how variable assignment works, there are other behavioral patterns:

-   copying the contents of a _value type_ variable into another variable, copies the entire contents into the new variable, making the two distinct. In other words, after the copy, changes to one won't affect the other
-   copying the contents of a _reference type_ variable into another variable, copies the reference, which means you now have two references to the same _somewhere else_ storage of the actual data. In other words, after the copy, changing the data in one reference will appear to affect the other as well, but only because you're really just looking at the same data both places

When you declare variables or fields, here's how the two types differ:

-   variable: _value type_ lives on the stack, _reference type_ lives on the stack as a pointer to somewhere in heap memory where the actual memory lives (though note [Eric Lipperts article series: The Stack Is An Implementation Detail](https://blogs.msdn.microsoft.com/ericlippert/2009/04/27/the-stack-is-an-implementation-detail-part-one/).)
-   class/struct-field: _value type_ lives completely inside the type, _reference type_ lives inside the type as a pointer to somewhere in heap memory where the actual memory lives.