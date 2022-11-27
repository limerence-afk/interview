
Both the `ref` and `in` require the parameter to have been initialized before being passed to a method. The `out` modifier does not require this and is typically not initialized prior to being used in a method.
By default, a reference type passed into a method will have any changes made to its values reflected outside the method as well. If you assign the reference type to a new reference type inside the method, those changes will only be local to the method.
Using the `ref` modifier, you have the option to assign a new reference type and have it reflected outside the method.
Using the `ref` modifier, you can also change value types outside the method as well.

Using the `out` modifier, we initialize a variable inside the method. Like `ref`, anything that happens in the method alters the variable outside the method. With `ref`, you have the choice to _not_ make changes to the parameter. When using `out`, you must initialize the parameter you pass inside the method. The parameter being passed in often is null.
The `out` modifier works with value types as well. A useful example is using the `out` modifier to change a string to an int.
The `in` modifier is most often used for performance reasons and was introduced in C# 7.2. The [motivation](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-7.2/readonly-ref#motivation) of `in` is to be used with a struct to improve performance by declaring that the value will not be modified. When using with reference types, it only prevents you from assigning a new reference.
	
### Modifiers Are Not Allowed on All Methods
It's important to note that `in`, `out`, and `ref` cannot be used in methods with the `async` modifier. You can use them in synchronous methods that return a task, though.

You cannot use them in iterator methods that have a `yield return` or `yield break` either.
	 