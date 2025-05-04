---
title: Control Flow
description: A reference page in my new Starlight docs site.
sidebar:
  order: 6
---

## Control Flow

### For Loop

```dart
void main() {
  for (int i=0; i<3; i++) {
    print("the current value of i is $i");
  }
}
```

```
the current value of i is 0
the current value of i is 1
the current value of i is 2
```

###### Example

loop through a list

```dart
void main() {
  List<int> scores = [50, 75, 20];

  for (int score in scores) {
    print("the score is $score");
  }
}
```

```
the score is 50
the score is 75
the score is 20
```

### If Statements

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];

  for (int score in scores) {
    if (score > 50) {
      print("the score is $score");
    }
  }
}
```

```
the score is 75
the score is 99
```

### Else Clause

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];

  for (int score in scores) {
    if (score > 50) {
      print("the score is $score");
    } else {
      print("score not high enough");
    }
  }
}
```

```
score not high enough
the score is 75
score not high enough
the score is 99
```

### List Where Method

```dart
void main() {
  List<int> scores = [50, 75, 20, 99];

  for (int score in scores.where((s) => s > 50)) {
    print("the score is $score");
  }
}
```
