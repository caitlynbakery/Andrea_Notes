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
