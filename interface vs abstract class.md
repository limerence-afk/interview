The short answer: An abstract class allows you to create functionality that subclasses can implement or override. An interface only allows you to define functionality, not implement it. And whereas a class can extend only one abstract class, it can take advantage of multiple interfaces.

## C# abstract class explained

An abstract class is a special type of class that cannot be instantiated. An abstract class is designed to be inherited by subclasses that either implement or override its methods. In other words, abstract classes are either partially implemented or not implemented at all. You can have functionality in your abstract class—the methods in an abstract class can be both abstract and concrete. An abstract class can have constructors—this is one major difference between an abstract class and an interface. You can take advantage of abstract classes to design components and specify some level of common functionality that must be implemented by derived classes.

## C# interface explained

An interface is basically a contract—it doesn’t have any implementation. An interface can contain only method declarations; it cannot contain method definitions. Nor can you have any member data in an interface. Whereas an abstract class may contain method definitions, fields, and constructors, an interface may only have declarations of events, methods, and properties. Methods declared in an interface must be implemented by the classes that implement the interface. Note that a class can implement more than one interface but extend only one class. The class that implements the interface should implement all its members. Like an abstract class, an interface cannot be instantiated.

С ключевым словом abstract можно объявлять:

-   методы;
-   свойства;
-   индексаторы;
-   события.

Нельзя объявить абстрактное поле (переменную) класса.


#####  Различия между абстрактными классами и интерфейсами

Между интерфейсами и абстрактными классами были замечены следующие различия:

-   в интерфейсе нельзя объявлять реализации методов, свойств и т.п. В абстрактном классе допускается объявлять реализации его элементов;
-   интерфейс не может иметь конструкторов. Абстрактный класс может иметь конструкторы;
-   интерфейс не может содержать поля данных. Абстрактный класс допускает использование внутренних полей данных;
-   элементы интерфейса по умолчанию (без модификатора доступа) считаются public. В абстрактных классах элементы по умолчанию считаются private;
-   элементы интерфейса не должны содержать модификатора доступа (иначе, компилятор выдаст сообщение об ошибке). В абстрактных классах допускается наличие любого модификатора доступа в объявлении элемента класса;
-   производный класс может наследовать только один абстрактный базовый класс. В случае использования интерфейсов производный класс может наследовать любое количество интерфейсов. Таким образом, интерфейс – это альтернатива абстрактного класса, с помощью которой можно осуществить множественное наследование.