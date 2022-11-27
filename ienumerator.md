```csharp
public void M()
{
	List<int> list = new List<int>();
	List<int>.Enumerator enumerator = list.GetEnumerator();
	try
	{
		while (enumerator.MoveNext())
		{
			int current = enumerator.Current;
		}
	}
	finally
	{
		((IDisposable)enumerator).Dispose();
	}
}
```
  