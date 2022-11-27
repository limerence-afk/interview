# Fields

_Fields_ are normal variable members of a class. Generally, you should declare your fields as private, then use _Properties_ to get and set their values. By this way you won’t affect their values them directly. This is common case practice since having public members violates the Encapsulation concept in OOP.

```
public class Student  
   {  
       private int _id;  
       private string _name;  
   }
```

# Properties

They are actually special methods called “_accessors_”. _Properties_ are called _accessors_ because they offer a way to get and set a field if you have a private field. They have two codes inside; _set{};_ and _get{};_ called “[_property accessors_](https://msdn.microsoft.com/en-us/library/aa287786(v=vs.71).aspx)”.


```
public class Student  
    {  
        private int _id;  
        private string _name;   
        public int Id { get { return _id; } set { _id = value; } }  
        public string Name { get { return _name; } set { _name = value; } }  
    }

```

_“value_” is a keyword, It refers to the assigned value, It’s like a parameter for the set method, The final code snippet will make it more obvious.

_Properties_ can be used to read only or write only other fields. This could be done by declaring only either _get{}_ or _set{}_. Also they can have access modifiers, like _private_, so you can only get or set their values inside their class.