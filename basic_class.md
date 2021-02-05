# Basic Class

## What I will learn

1) Create Classes
2) Constructors
3) Member variables & methods
4) Getters & Setters
5) Static keyuword
6) making things private

## Constructors

Constructors are methods inside of a class that
have the same name and are used for initializing parameters.
The `this.` is used inside of the constructor body. this.balance is different from
balance because balance is an argument while this.balance is the variable inside
the class.

 ```dart
class BankAccount {
  BankAccount(double balance) {

  this.balance = balance;}}
 ```

There are two ways to utilize constructor initilization. One way
is by using initializer list and the other way is using the `this.`
shorthand.

The initializer list looks like this.

```dart
BankAccount({
    required String accountHolder,
    double balance = 0,
}) : accountHolder = accountHolder, 
balance = balance,
```

Comparatively, the shorthand constructor uses the `this.` argument to shorten
the code and make it easier to read.

```dart
 BankAccount({required this.accountHolder,  this.balance = 0});
```

The constructor comes before the variable declaration.

## Immutable

Immutable variables do not change state and can
be initialized with final property.

## Const constructor

Constructors should be initialized with const when all the arguments
are immutable. Thus, when I declare the class in the main method, I can use const.
This makes the code run faster and more efficient.

```dart
class Complex {
const Complex(this.re, this.im);
 final double re;
final double im;
}
```

## Named Constructor

A named constructor is a constructor with a name. For example,
`Complex.zero()` is a named constructor. The named
constructor can initialize different variables
and take in different parameters. This allows for
the named constructor to be more unique and
specialized compared to a regular constructor.

```dart
Complex.zero() : re = 0, im = 0;
 final double re;
final double im;
...main(){
    final zero = Complex.zero();
```

This is an example of a named constructor
with a parameter and initializer.

```dart
Complex.real(this.re) : im = 0;
...main(){
    final real = Complex.real(3);
```

## Getter

The getter method gets a value. The
benefit of using a getter is that
you don't have to put round parenthesis
around the name of the value.

```dart
double get fahrenheit => celsius * 1.8 + 32;

...main(){
   print(temp.fahrenheit); 
```

In the class called Restaurant, I created a getter function called totalRatings
to return the length of a list called ratings. The purpose of a getter function
is to get values.

```dart
class Restaurant{
 ...
  int get totalRatings {
    return ratings.length;
  }
}

void main(){
var restaurant1 = Restaurant(name: 'Pizza', cuisine: 'Italian', 
ratings: [4.4, 3.3, 5.0]);
  print(restaurant1.totalRatings);
 }
```

## Setter

The setter method sets a value and is called through
an assignment in the main method.

```dart
set fahrenheit(double fahrenheit) => celsius = (fahrenheit - 32) / 1.8;

...main(){
temp.fahrenheit = 90;
```

## Static

Static variables/methods should be used when they are specific to a class.
The static const is a global constant that should belong to a class.
When I use the static variables in the main() method,
I don't have to instantiate the class.

```dart
class Strings {
static const welcome = 'Welcome';
  static const signIn = 'Sign in';
  static String greet(String name) => 'Hi, $name';
}

void main() {
print(Strings.welcome);
  print(Strings.signIn);
  print(Strings.greet('Apple'));
}
```
