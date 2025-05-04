---
title: Basics
description: A reference page in my new Starlight docs site.
sidebar:
  order: 2
---

## Dart Basics

###### Example

```dart
void main() {
    for (var i = 0; i < 3; i++) {
      print('hello ${i + 1}');
    }
}
```

```
hello 1
hello 2
hello 3
```

###### Example

```dart
void main() {
    var name = "Naruto";
    name = "Sasuke";
    print(name); // Sasuke
}
```

## Final vs Const Variables

```dart
void main() {
    final age = 17;      // run-time constant
    const pi = 3.14;     // compile-time constant
}
```

### Final

- Think of `final` as "write-once, read-many"
- Value can be determined at runtime
- Perfect for:
  ```dart
  final currentTime = DateTime.now();     // OK - runtime value
  final userInput = getUserInput();       // OK - runtime value
  ```

### Const

- Must be known at compile time
- Value has to be fixed before the program runs
- Perfect for:
  ```dart
  const maxAttempts = 3;         // OK - fixed value
  const apiVersion = "v1";       // OK - fixed value
  const now = DateTime.now();    // ERROR - not known at compile time
  ```

**Quick Rule**: Use `const` for values you know at coding time, use `final` for values that will be determined when the app runs.

## Math

```dart
void main() {
    final age = 17;
    print(age + 10); // 27
    print(age - 10); // 7
    print(age * 10); // 170
    print(age / 5);  // 3.4
}
```

## String Interpolation

```dart
void main() {
    var name = "Naruto";
    print("Welcome, ${name}!"); // Welcome, Naruto!
}
```

## Comments

```dart
void main() {
    // This is a single-line comment
    print("Hello, World!"); // This prints to the console

    /*
    This is a multi-line comment
    It can span multiple lines
    */
    print("Goodbye, World!");
}
```
