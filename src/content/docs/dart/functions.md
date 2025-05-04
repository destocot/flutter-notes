---
title: Functions
description: A reference page in my new Starlight docs site.
sidebar:
  order: 4
---

## Functions

### Defining Functions

```dart
void main() {
}
```

> The `void` keyword indicates that the function does not return a value. The `main` function is the entry point of a Dart program.

```dart
void main() {
  final greeting = greet("naruto", 17);
  print(greeting);
}

String greet(String name, int age) {
  return "Hi, my name is $name and I am $age";
}
```

> The `greet` function returns a string that includes the name and age of the person.

> Positional parameters are defined in the function signature and are passed to the function in the order they are defined. In the example above, `name` and `age` are positional parameters.

### Named Parameters

```dart
void main() {
  final greeting = greet(age: 17, name: "naruto");
  print(greeting);
}

String greet({String? name, required int age}) {
  return "Hi, my name is $name and I am $age";
}
```

> Named parameters are defined in curly braces `{}` in the function signature. They can be optional or required. In the example above, `name` is optional and `age` is required.
