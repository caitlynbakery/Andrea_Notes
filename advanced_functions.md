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

### forEach method

The forEach method in Dart can be used as an anonymous function to loop through every item in a list. It has the same functionality as the for in function. Another way to implement the forEach method is by passing it an existing name function. For example, the print method can be passed as an argument into the forEach method to print all the items in the list. 

```dart
const list = [1,2,3];
list.forEach((x) => print(x)); //anonymous function
  list.forEach(print); //implicitly passing argument
```

### map method

The map method takes in a list and preforms a transformation on each value. 

```dart
final doubles =  list.map((value) => value * 2);
```

### Iterable

 An iterable is a collection of elements that can be accessed sequentially. In Dart, lists and sets are both iterable types. The map method returns a lazy iterable. A lazy iterable is when an anonymous function is not evaluated until the result is used. When we print an iterable, it appears inside round brackets. If we want the map method to return a list instead of an iterable, then we should use `.toList()`. 

 ```dart
  final List<int> doubles =  list.map((value) => value * 2).toList(); //returns a list
 ```

 ### Generics

 We can use function arguments and generics to reuse code and make it more organized. Type T is generic type, while Type R is a return type. In the function below, I transform a list of generic items into a list of return types. One of the paramters in transform() is also a generic function, so I can perform different functions on a list.

 ```dart

 void main() {
       final doubles = transform<int, int>(list, (x) => x * 2);
  final rounded = transform<double, int>(list2, (x) => x.round());
 }
 
List<R> transform<T, R>(List<T> items, R Function(T) f) {
  var result = <R>[];
  for (var x in items) {
    result.add(f(x));
  }

  return result;
}
 ```