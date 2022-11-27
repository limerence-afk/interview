The main difference between IEnumerable and IQueryable in C# is that IQueryable queries out-of-memory data stores, while IEnumerable queries in-memory data. Moreover, IQueryable is part of .NET's System.LINQ namespace, while IEnumerable is in System.Collections namespace.

IQueryable contains methods for constructing expression trees. IQueryable inherits IEnumerable, so IQueryable does everything that IEnumerable does. IQueryable extends the IEnumerable with logic for querying data.

- *The main disadvantage of casting IQueryable to IEnumerable is slower performance. Since IEnumerable works on local objects, we first need to load all the objects to memory. IQueryable is better in that sense because we can pick just what we need. 

- *Interpreted queries in C# are operations that translate expression trees at runtime. For example, EntityFramework translates IQueryable expression trees to SQL queries.

- *The benefit of using interpreted queries is that we can write the same code, but have different translations. For example, we can write the same C# code for the SQL server and for the PostgreSQL. We use the IQueryable interface, but interpreter figures out the underlying queries.

`IQueryable<T>` is a C# interface that lets you query different data sources. The type `T` specifies the type of the data source that you're querying. Under the hood, [IQueryable](https://docs.microsoft.com/en-us/dotnet/api/system.linq.iqueryable-1) uses expression trees that translate LINQ queries into the query language for the data provided.

Since `IQueryable<T>` extends the `IEnumerable<T>` interface, we can enumerate the result.

