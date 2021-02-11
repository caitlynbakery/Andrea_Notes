# Basic Functions

Topics to Learn:

* positional arguments
* lexical scope
* inner functions
* global mutable state
* pure functions

## Argument vs Parameter

Function arguments are the value of the variables that are passed to the function.
Parameters are the variables defined at function declaration.

<img src="http://getkt.com/wp-content/uploads/2019/05/Parameters-vs-Arguments.jpg"
width=50% alt="argumentsvsparameters">

Function names are typically verbs while function parameters are nouns.

## Functions with Named arguments

Without Null Safety, arguments can be omitted and have a null value.
The null value may cause your program to break.

With Null Safety, there are three ways to handle function parameters.

1. make arguments nullable (ex: `{String? name}`)
2. make arguments non-nullable
    * use default value(ex: `{String name = 'Caitlyn'}`)
    * mark the argument as required(ex: `{required String name}`)

## Local & Global Scope

### Local Scope

Scope is block of code defined inside curly braces. It can contain multiple statements.
Variables defined inside the scope can't be accessed outside of the scope.

```dart
const a = 10;
  print(a);
  
  if(a > 5) {
    const a = 5;
    print(a);
  }
```

### Global Scope

Global scope is a variable that is assigned outside of the main function and can be accessed anywhere in the code.

```dart
const global = 15;

void main(){
    print(global);
}
```

## Global Mutable State

Global mutable state can lead to bugs and issues that cost a lot of time to fix.

A side effect is when a variable is modified outside of its scope.
The side effect is really bad because you don't want to change the variable in
another scope!

```dart
var counter = 1;

void main() {
    counter++;
    counter++;
}
```

In the example above, the global variable counter
is being modified which we should avoid.
