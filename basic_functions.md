## Basic Functions

Topics to Learn:

* positional arguments
* lexical scope
* inner functions
* global mutable state
* pure functions

### Argument vs Parameter

Function arguments are the value of the variables that are passed to the function. Parameters are the variables defined at function declaration.

<img src="http://getkt.com/wp-content/uploads/2019/05/Parameters-vs-Arguments.jpg" width=50% alt="argumentsvsparameters">

Function names are typically verbs while function parameters are nouns. 

### Functions with Named arguments

Without Null Safety, arguments can be omitted and have a null value. The null value may cause your program to break.

With Null Safety, there are three ways to handle function parameters.

1. make arguments nullable (ex: `{String? name}`)
2. make arguments non-nullable
    
    * use default value(ex: `{String name = 'Caitlyn'}`)
    * mark the argument as required(ex: `{required String name}`)