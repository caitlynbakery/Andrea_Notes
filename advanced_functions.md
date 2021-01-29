## Advanced Functions

### Anonymous Functions

An anonymous function is a function that doesn't have a name.  

```dart
final sayHi = (String name) => 'Hi, $name';
```

### Function Types

A type is part of the function call. You can pass in arguments. The type is typedef and it is easy to implement. 

```dart
typedef Greet = String Function(String);

void welcome(Greet greet, String name){

}
```

### Closures

A closure is an anonymous function that uses variables defined outside of its own scope. For example, the multiplier variable is outside the scope of the anonymous function. 

```dart
const multiplier = 10;
  const list = [1,2,3];
  final result = list.map((x) {
return x * multiplier;
  } );
```