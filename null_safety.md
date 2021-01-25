## Null Safety

### Nullable vs Non-nullable

Null safe means that variables can't be set to null, unless you use a question mark to explicity set the variable to null. Dart is moving to null safe by default. In earlier versions of Dart, nullable variables can be set to null and added with an integer. The error is displayed at run-time, while non-nullable variables display the error at compile-time.

The example below shows a nullable variable that shows an error at run-time.

```dart
int a;
  int b = 2;
  print(a+b);
```

The other example shows a non-nullable variable that shows the error at compile-time.

```dart
int? a;
  int b = 2;
  print(a+b);
```

### Flow anaylsis: Definite Assignment

In null safety versions of Dart, a variable can be declared and checked with if statements to be assigned a new value. 

```dart
 int x = 10;
  int sign;
  if (x >= 0) {
    sign = 1;
  } else {
    sign = -1;
  }
  print(sign);
```

### Assertion Operator

A non-nullable variable cannot normally be assigned to a nullable variable. However, if we are sure that a nullable variable will have a non-nullable value, then we can use an assertion operator. The assertion operator assigns a nullable value to a non-nullable variable. 

```dart
int x = -2;
  int? maybeValue;
  if (x > 0) {
    maybeValue = x;
  }
  int value = maybeValue!;
  print(value);
```