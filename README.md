# Dart Language Notes

## Dart Basics

### Initilization vs Assignment

When declaring a variable, we can assign it to a value using the equals sign. Declaration is calling the variable type and name. 

This is initilization :) 

```
String name = "Caitlyn";
```

This is declaration

```
String cake
```

This is assignment

```
cake = "Strawberry"; 
```

### Logical & Relational operators

logical operators compare between expressions and return a boolean value. 
Examples of logical operators include: 

```
   ==
   !=
   >=
   >
   <=
 ```
 
relational operators compare logical operators.
Examples of relational operators include:
  * ||
  * &&

## Dart Type System

### final vs. const

final keyword is a run-time constant and can only be set once. Contrastly, the const keyword is a compile-time constant and needs to be used with compile-time functions. It is best to use const > final > var to make an efficient code.



