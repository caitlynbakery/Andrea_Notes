# Advanced Classes

## Stuff I will Learn

1. subclassing(inheritance)
2. super constructor
3. overriding methods
4. abstract classes
5. implements vs extends
6. base object class
7. toString(), == operator, hashCode
8. equatable package
9. generics with classes
10. composition vs inheritance
11. factory constructors
12. copying objects with copyWith
13. cascade operator(..)

## Subclassing

Subclassing extends the functionality of an existing class and increases
code reuse. When I extend an existing class, it is called
subclassing or inheritance. Inheritance allows for a class to inherit
all of the functionality from the parent class.

```dart
class Animal {
  void sleep() => print('sleep');
}
class Dog extends Animal {
  void bark() => print('bark');
}
```

## Super constructor

The super constructor
is the constructor from the parent class. When I extend sub classes from the
parent class, the super constructor is not inherited. In my subclass,
I create a constructor that initializes a new  `int age` variable.
The subclass constructor links the super constructor from
the parent class and I pass in the `age` parameters.

```dart
class Animal {
  const Animal({required this.age});
  final int age;
  void sleep() => print('sleep');
}

class Dog extends Animal {
  Dog({required int age}) : super(age: age);
  void bark() => print('bark');
}
```

It's not possible to instantiate instances of the parent class,
`Animal` without creating a constructor in the subclasses. The
super constructor is not passed to the subclasses. In this case
the `Animal` constructor requires the parameter `age`. If you try
to instantiate the class `Dog` without passing in `age`, the progam
will fail. Also, if you pass in `age` when you instantiate a subclass
without making a constructor, the progam will fail.

## override

The override keyword is used when a subclass makes a copy of the methods in the
parent class, enabling the programer to make changes to it. I
use the override to change the contents of the method and make
it more unique to the subclass. If I want to access the methods from the superclass,
I use the `super.` convention in the subclass.

```dart
class Dog extends Animal {
 @override
  void sleep() {
super.sleep();
print('sleep some more');
  }
  }
```

## abstract classes

Abstract classes are classes that are classes that
cannot be instantiated. They are implemented
 by subclasses. The abstract class is
very powerful because it separates the code interface
and implementation. What this means is that when we can call a
method `printArea()`, we don't have to
specifiy the area calculations for each subclass.
The `printArea()` method only needs a
Shape argument with an area property.
Each subclass is of type Shape,
so when we pass in a `Circle` subclass into `printArea`,
the code works!

```dart
abstract class Shape {
  double get area;
}

class Circle extends Shape {
  Circle(this.radius);
  final double radius;

  @override 
  double get area => pi * radius * radius;
}

void printArea(Shape shape){
  print(shape.area);
}

void main(){
final Shape circle = Circle(6);
  printArea(circle);
}
 
```

## Differences between implements & extends

### multiple class inheritance

An important difference between `implements` and `extends`
is that `implements` can inherit multiple classes, while
`extends` can only inherit one class.

```dart
abstract class InterfaceA {
  void a();
}

abstract class InterfaceB {
  void b();
}

class AB implements InterfaceA, InterfaceB {
  @override 
  void a(){
  }
  @override 
  void b(){
  }
}
```

### override requirement

Another difference is that when you implement a method
inside of an abstract class, you don't have to override
it in the subclass. However, if a method is not
implemented in the abstract class, then it is an abstract
method and needs to be overriden.

```dart
abstract class Base {
  void foo();
  void bar() => print('bar');
}

class Subclass extends Base {
  @override 
  void foo() => print('foo');
}
```
