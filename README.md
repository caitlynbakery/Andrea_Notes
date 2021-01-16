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
  
### Increment & Decrement Operators

```
int x = 1;
int y = ++x;

// x = 2, y = 2

int z = 1;
int b = a++;

// a = 2, b = 1
```

++x is a prefix increment operator which means that x is incremented first. Then, y is assigned to x.
a++ is a postfix increment operator which means that b returns the value of z before z is incremented. 

### Hex Format
Dart uses the base16 notation which is digits from 0 to 9 and letters from A to F.
example: 
OxA = 10

### String escaping
To escape a symbol in Dart, we use the `\` symbol. 

```
int a = 10
print('$a')
print('\$a')
print('\$$a')

\\ prints: 10, $a, $10 
```
## Dart Type System

### final vs. const

final keyword is a run-time constant and can only be set once. Contrastly, the const keyword is a compile-time constant and needs to be used with compile-time functions. It is best to use const > final > var to make an efficient code.



