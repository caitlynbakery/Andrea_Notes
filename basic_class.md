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
The this. is used inside of the constructor body. this.balance is different from
balance because balance is an argument while this.balance is the variable inside
the class.

 ```dart
class BankAccount {
  BankAccount(double balance) {

  this.balance = balance;}}
 ```
