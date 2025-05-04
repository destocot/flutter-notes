---
title: Type Annotations
description: A reference page in my new Starlight docs site.
sidebar:
  order: 3
---

## Type Annotations

### Explicit Types

```dart
void main() {
  String name = "naruto";

  int age = 17;

  bool isOpen = true;

  double averageRating = 7;
  averageRating = 7.5;
}
```

### with const and final

```dart
void main() {
  const String name = "naruto"; // compile-time constant
  final int age = 17; // runtime constant
}
```

### Nullable Types

```dart
void main() {
  int? point; // nullable int
}
```
