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
