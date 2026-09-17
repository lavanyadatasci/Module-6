#1. Python OOP: Abstract Class & Method Example

## AIM

To create an abstract class named `Shape` with an abstract method `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

## ALGORITHM

1. Import `ABC` and `abstractmethod` from the `abc` module.
2. Create an abstract class `Shape`.
3. Define the abstract method `calculate_area()`.
4. Create the `Rectangle` subclass and implement `calculate_area()`.
5. Create the `Circle` subclass and implement `calculate_area()`.
6. Create objects of `Rectangle` and `Circle`.
7. Call `calculate_area()` for both objects.
8. Display the calculated areas.

## PROGRAM

```python
from abc import ABC, abstractmethod
import math

class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass


class Rectangle(Shape):

    def __init__(self, length=10, breadth=5):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth


class Circle(Shape):

    def __init__(self, radius=7):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius * self.radius


rectangle = Rectangle()
circle = Circle()

print("Area of Rectangle:", rectangle.calculate_area())
print("Area of Circle:", circle.calculate_area())
```

## OUTPUT

```text
Area of Rectangle: 50
Area of Circle: 153.93804002589985
```

## RESULT

Thus, the Python program successfully demonstrates an abstract class and abstract method using `Shape`, `Rectangle`, and `Circle`.

#2. Python OOP: Encapsulation with Private Members

## AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with private member variables `__length` and `__breadth`.

## ALGORITHM

1. Define a class `Rectangle`.
2. Create two private attributes `__length` and `__breadth`.
3. Use the `__init__()` constructor to initialize the private attributes.
4. Print the private variables from inside the class.
5. Create an object of the `Rectangle` class.

## PROGRAM

```python
class Rectangle:

    def __init__(self, length, breadth):
        self.__length = length
        self.__breadth = breadth

    def display(self):
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)


rectangle = Rectangle(10, 5)
rectangle.display()
```

## OUTPUT

```text
Length: 10
Breadth: 5
```

## RESULT

Thus, the Python program successfully demonstrates **encapsulation** using private member variables `__length` and `__breadth`.

#3. Method Overriding - Fish and Shark Class Inheritance in Python

## AIM

To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## ALGORITHM

1. Define the `Fish` class with a method `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`.
3. Override the `type()` method in the `Shark` class to print `"shark"`.
4. Create an object of the `Fish` class named `obj_goldfish`.
5. Create an object of the `Shark` class named `obj_hammerhead`.
6. Use a `for` loop to iterate through both objects.
7. Call the `type()` method for each object.
8. Display the output.

## PROGRAM

```python id="f7k3mp"
class Fish:

    def type(self):
        print("fish")


class Shark(Fish):

    def type(self):
        print("shark")


obj_goldfish = Fish()
obj_hammerhead = Shark()

for obj in (obj_goldfish, obj_hammerhead):
    obj.type()
```

## OUTPUT

```text id="q2v8ld"
fish
shark
```

## RESULT

Thus, the Python program successfully demonstrates **method overriding** using inheritance between the `Fish` and `Shark` classes.

#4. Python OOP: Operator Overloading (Less Than `<`)

## AIM

To write a Python program that demonstrates operator overloading by overloading the **less than (`<`)** operator using a custom class.

## ALGORITHM

1. Create a class `A`.
2. Define the `__init__()` method to initialize the object with a value `a`.
3. Define the `__lt__()` method to overload the `<` operator.
4. Compare the values of two objects using `self.a < o.a`.
5. Create two objects `ob1` and `ob2` with values.
6. Use `print(ob1 < ob2)` to call the overloaded operator.
7. Display the result.

## PROGRAM

```python id="k8p4vz"
class A:

    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"


ob1 = A(2)
ob2 = A(3)

print(ob1 < ob2)
```

## OUTPUT

```text id="v3n7qx"
ob1 is less than ob2
```

## RESULT

Thus, the Python program successfully demonstrates **operator overloading** by overloading the less than (`<`) operator using the `__lt__()` method.

#5. Python OOP: Polymorphism with Classes

## AIM

To create two classes, `Beans` and `Mango`, and create a generic function that accepts any object and determines its type and color using polymorphism.

## ALGORITHM

1. Create the `Beans` class with `type()` and `color()` methods.
2. Create the `Mango` class with `type()` and `color()` methods.
3. Define a generic function `func(obj)`.
4. Call `obj.type()` and `obj.color()` inside the function.
5. Create objects of `Beans` and `Mango`.
6. Pass both objects to the `func()` function.
7. Display the output.

## PROGRAM

```python id="w3k9pt"
class Beans:

    def type(self):
        print("Vegetable")

    def color(self):
        print("Green")


class Mango:

    def type(self):
        print("Fruit")

    def color(self):
        print("Yellow")


def func(obj):
    obj.type()
    obj.color()


beans = Beans()
mango = Mango()

func(beans)
func(mango)
```

## OUTPUT

```text id="x6q2rm"
Vegetable
Green
Fruit
Yellow
```

## RESULT

Thus, the Python program successfully demonstrates **polymorphism** using the `Beans` and `Mango` classes with a generic function
