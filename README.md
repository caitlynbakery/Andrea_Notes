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

## Dart Type System

### final vs. const

final keyword is a run-time constant and can only be set once. Contrastly, the const keyword is a compile-time constant and needs to be used with compile-time functions. It is best to use const > final > var to make an efficient code.

## Control Flow

### String multiplication
String multiplication concatenates a string a number of times. You can't multiply 'x' * 'x'. 

For example, 'x' * 2 equals 'xx'. 

'x' * 3 equals 'xxx'. 

### Modulo Operator
The modulo operator returns the remainder of a division equation and can be used to find an odd or even number.

```
5 % 3 // equals 2
10 % 2 // equals 0 
```

### Break & Continue
The break and continue keywords can be used to alter the flow inside for/while loops. The break keyword exists the loop's function and runs the next section of code. Contrastly, the continue keyword keeps the loop running.

```dart
 for(var i = 1; i <= 16; i++){
    if((i % 3 == 0) && (i % 5 == 0)) {
    print('fuzz buzz');
      break;
    } 
     if (i % 3 == 0){
    print ('fuzz');
    continue;
    }
```

### Switch Statements
The switch statement can be used in place of if/else statements. I use the switch function with multiple cases to control the behavior. At the end of each case, I write the break statement. The default statement runs when all the other cases are false. 

```dart
const pos = 'second';
  
  switch (pos) {
    case 'first':
      print('gold');
      break;
    default:
      print('no medal');
      break;
```

### Enum 
The enum type can be used to define values and organize the code. I first declare the values of an enum inside curly brackets. Then, I can access enum values inside my code by calling the name and value. 

In my example, the enum type is called Operation.

```dart
enum Operation {plus, minus, multiply, divide}

void main() {
  const a = 7;
  const b = 2;
  const op = Operation.multiply;
  
  switch(op){
    case Operation.plus:
      print('$a + $b = ${a + b}');
      break;
```
