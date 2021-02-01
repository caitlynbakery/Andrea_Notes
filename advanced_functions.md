# Advanced Functions

In this section I covered these functional operators:

* forEach
* map
* where
* firstWhere
* reduce

## Anonymous Functions

An anonymous function is a function that doesn't have a name.  

```dart
final sayHi = (String name) => 'Hi, $name';
```

## Function Types

A type is part of the function call. You can pass in arguments. The type is typedef and it is easy to implement.

```dart
typedef Greet = String Function(String);

void welcome(Greet greet, String name){

}
```

## Closures

A closure is an anonymous function that uses variables defined outside of its own scope. For example, the multiplier variable is outside the scope of the anonymous function.

```dart
const multiplier = 10;
  const list = [1,2,3];
  final result = list.map((x) {
return x * multiplier;
  } );
```

## forEach method

The forEach method in Dart can be used as an anonymous function to loop through every item in a list. It has the same functionality as the for in function. Another way to implement the forEach method is by passing it an existing name function. For example, the print method can be passed as an argument into the forEach method to print all the items in the list.

```dart
const list = [1,2,3];
list.forEach((x) => print(x)); //anonymous function
  list.forEach(print); //implicitly passing argument
```

## map method

The map method takes in a list and preforms a transformation on each value.

```dart
final doubles =  list.map((value) => value * 2);
```

## Iterable

 An iterable is a collection of elements that can be accessed sequentially. In Dart, lists and sets are both iterable types. The map method returns a lazy iterable. A lazy iterable is when an anonymous function is not evaluated until the result is used. When we print an iterable, it appears inside round brackets. If we want the map method to return a list instead of an iterable, then we should use `.toList()`.

 ```dart
  final List<int> doubles =  list.map((value) => value * 2).toList(); //returns a list
 ```

## Generics

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

## where and firstWhere function

 The where and firstWhere functions are used to filter and find items inside a collection. They take in an anonymous function that returns a boolean. This function is called a predicate. The where function returns an iterable, but can return a list using `.toList()`.  

 ```dart
  const list = [1,2,3,4];
  final even = list.where((value) => value % 2 == 0); 
  print(even);
  final value = list.firstWhere((x) => x == 4, orElse: () => -1);
 ```

## where function exercise

 In this exercise, I created my own where function that utilizes generic type and returns a generic typed list. My where function first accepts a generic typed list called values and a function called equation. It then runs the equation on every value in my list and adds the value to a empty list. I can call the where function by passing in a list and an anonymous function.

 ```dart
void main() {
 var numbers = [1,2,3,4];
  var result = where<int>(numbers, (x) => x % 2 == 1); 
  print(result);
}

List<T> where<T> (List<T> values, bool Function(T) equation){
  var result = <T>[];
for(var value in values){
  if (equation(value)) 
    result.add(value);
}
  return result; 
}

 ```

## firstWhere function exercise

 In this exercise, I created a firstWhere function from scratch with generic types. The firstWhere function runs the equation function on every value in my list. It then returns value. Else, the firstWhere function returns the orElse function.

 ```dart
var result2 = firstWhere(numbers, (x) => x == 5, orElse: () => -1);
print(result2);

T firstWhere<T> (List<T> values, bool Function(T) equation, {required T Function() orElse}){
 
  for(var value in values){
    if (equation(value)){
       return value;
      } 
  }  
  return orElse();
}

 ```

## reduce method

 This method combines all the items inside a list and produces a single result. In the example below, the items in the list are combined together and produce a single value.

 ```dart
const list = [1,2,3,4];
  final sum = list.reduce((value, element) => value + element);
  print(sum);
 ```

 The first time the function runs, value equals 1 and element equals 2. The two variables are added together and value equals 3. Element also equals 3 and then value equals 6.

## functional programming vs imperative programming

 Functional programming works best when manipulating collections, like lists. Functional style can make code easier to read and write. Whereas, imperative style is a sequence of steps and control flow statements which can get to be a long block of code.

 ```dart
 const emails = [
'abc@abc.com',
  'caitlynisgreat@gmail.com',
  'fathertime@yahoo.com',
  ];
  const knownDomains = ['gmail.com', 'yahoo.com'];

Iterable<String> getUnknownDomains(List<String> emails, List<String> knownDomains) => emails.map((email) => email.split('@').last).where((domain) => !knownDomains.contains(domain));
 ```

 In the example above, a map function and a where function are chained together because they both return iterables. The function first runs a map function to find the section of the String after the @ symbol. Next, it runs a where function to keep the items that are not in my `knownDomains` list.
