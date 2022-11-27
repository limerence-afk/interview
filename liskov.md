Классическим примером нарушения принципа подстановки Барбары Ли-  
сков может служить известная проблема квадрат/прямоугольник (рис 9 2).

![[Pasted image 20221125114423.png]]

В этом примере класс Square (представляющий квадрат) неправильно  
определен как подтип класса Rectangle (представляющего прямоугольник),  
потому что высоту и ширину прямоугольника можно изменять независимо;  
а высоту и ширину квадрата можно изменять только вместе Поскольку  
класс User полагает, что взаимодействует с экземпляром Rectangle, его легко  
можно ввести в заблуждение, как демонстрирует следующий код:  
Rectangle r = ...  
r.setW(5);  
r.setH(2);  
assert(r.area() == 10);  
Если на место ... подставить код, создающий экземпляр Square, тогда  
проверка assert потерпит неудачу Единственный способ противостоять  
такому виду нарушений принципа LSP — добавить в класс User механизм  
(например, инструкцию if), определяющий ситуацию, когда прямоуголь-  
ник фактически является квадратом Так как поведение User зависит от ис-  
пользуемых типов, эти типы не являются заменяемыми (совместимыми)


