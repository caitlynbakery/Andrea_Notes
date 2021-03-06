[Go back](README.md)

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

// z = 2, b = 1
```

++x is a prefix increment operator which means that x is incremented first. Then, y is assigned to x.

z++ is a postfix increment operator which means that b returns the value of z before z is incremented. 

### Hex Format
Dart uses the base16 notation which is digits from 0 to 9 and letters from A to F. Hex numbers are used to define colors in ARGB format. 

example for the color green: 

```
int green = 0xFF00FF00;
```

In the color green, the first set of FF represents the alpha channel, 00 represents red color, FF represents green color and 00 represents the blue color. 

### String escaping
To escape a symbol in Dart, we use the `\` symbol. 

```
int a = 10
print('$a')
print('\$a')
print('\$$a')

// prints: 10, $a, $10 
```

### Finding & Replacing Strings

There are different functions that we can use to alter strings. 

For example, we can use the contains() method to check to see if a String contains another String.

```
String lovePizza = "I love pizza"
print(lovePizza.contains('pizza'));

// returns true
```

The method replaceAll() replaces 'pizza' with 'pasta'.

```
String lovePizza = "I love pizza"
print(lovePizza.replaceAll('pizza', 'pasta')

// prints: I love pasta
```
