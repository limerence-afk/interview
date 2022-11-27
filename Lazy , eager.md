
**Eager Loading:** Eager Loading helps you to load all your needed entities at once. i.e. related objects (child objects) are loaded automatically with its parent object.

**When to use:**

1.  Use Eager Loading when the relations are not too much. Thus, Eager Loading is a good practice to reduce further queries on the Server.
2.  Use Eager Loading when you are sure that you will be using related entities with the main entity everywhere.

**Lazy Loading:** In case of lazy loading, related objects (child objects) are not loaded automatically with its parent object until they are requested. By default LINQ supports lazy loading.

**When to use:**

1.  Use Lazy Loading when you are using one-to-many collections.
2.  Use Lazy Loading when you are sure that you are not using related entities instantly.

> NOTE: Entity Framework supports three ways to load related data - eager loading, lazy loading and explicit loading.



In practice, they mean essentially the same thing. However, it's preferable to use the term _deferred_.

-   **Lazy** means _"don't do the work until you absolutely have to."_
    
-   **Deferred** means _"don't compute the result until the caller actually uses it."_
    

In practice, when the caller decides to use the result of an evaluation (i.e. start iterating through an `IEnumerable<T>`), that is precisely the point at which the "work" needs to be done (such as issuing a query to the database).

The term **deferred** is more specific/descriptive as to what's actually going on. When I say that I am _lazy_, it means that I _avoid doing unnecessary work_; it's ambiguous as to what that _really_ implies. However, when I say that execution/evaluation is _deferred_, it essentially means that I am not giving you the real result at all, but rather a _ticket you can use to claim the result_. I _defer_ actually going out and _getting_ that result until you _claim_ it.

Please use the term _deferred_ when discussing the subject as it pertains to C#. _Lazy_ is a vaguer version.

