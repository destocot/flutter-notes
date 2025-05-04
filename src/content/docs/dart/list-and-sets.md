---
title: List and Sets
description: A reference page in my new Starlight docs site.
sidebar:
  order: 5
---

## List and Sets

### List

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  print(scores[0]); // 50

  scores[0] = 25;
  print(scores[0]); // 25
}
```

### Adding Elements

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  scores.add(100);
  print(scores); // [50, 75, 20, 99, 100]
}
```

### Removing Elements

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  scores.remove(20);
  print(scores); // [50, 75, 99]
}
```

####### Example
removing an element that has multiple occurrences

```dart
void main() {
  List<int> scores = [50, 75, 20, 99, 20];
  scores.remove(20);
  print(scores); // [50, 75, 99, 20]
}
```

> The `remove` method removes the first occurrence of the specified element from the list.

###### Example

removing the last element

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  scores.removeLast();
  print(scores); // [50, 75, 20]
}
```

### Length of List

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  print(scores.length);
}
```

### Shuffle List

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  scores.shuffle();
  print(scores);
}
```

### Index of Element

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];
  print(scores.indexOf(20)); // 2
  print(scores.indexOf(99)); // 3
}
```
