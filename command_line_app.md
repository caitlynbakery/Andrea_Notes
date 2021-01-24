## Command Line App

### Use of Input and Output

`stdout` and `stdin` control the inputs and outputs of a dart application. `stdout` is an ouput, while `stdin` is an input. I first used `stdout` to display a piece of text in the console. Next, I used `stdin` to wait for an input by the user and read in their response. 

```dart
import 'dart:io';
...

while (true){
  stdout.write('rock, paper or scissors? (r/p/s) ');
  final input = stdin.readLineSync();
  
  if(input == 'r' || input == 'p' || input == 's'){
    ...
  }
```

### Random Number

Dart can generate random numbers with the `Random().nextInt()` function from dart:math. The parameter passed into `nextInt()` is the range in which a random number is selected.

```dart
import 'dart:math';
...
final rng = Random();
...
final random = rng.nextInt(3);
```
