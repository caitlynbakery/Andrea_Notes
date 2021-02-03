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
