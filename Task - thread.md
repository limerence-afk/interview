## Differences Between Task And Thread

Here are some differences between a task and a thread.  

1.  The Thread class is used for creating and manipulating a [thread](http://msdn.microsoft.com/en-us/library/windows/desktop/ms684841%28v=vs.85%29.aspx) in Windows. A [Task](http://msdn.microsoft.com/en-us/library/vstudio/system.threading.tasks.task) represents some asynchronous operation and is part of the [Task Parallel Library](http://msdn.microsoft.com/en-us/library/dd460717%28v=vs.110%29.aspx), a set of APIs for running tasks asynchronously and in parallel.
2.  The task can return a result. There is no direct mechanism to return the result from a thread.
3.  Task supports cancellation through the use of cancellation tokens. But Thread doesn't.
4.  A task can have multiple processes happening at the same time. Threads can only have one task running at a time.
5.  We can easily implement Asynchronous using ’async’ and ‘await’ keywords.
6.  A new Thread()is not dealing with Thread pool thread, whereas Task does use thread pool thread.
7.  A Task is a higher level concept than Thread.