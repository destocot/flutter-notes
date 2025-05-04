---
title: Maps
description: A reference page in my new Starlight docs site.
sidebar:
  order: 7
---

## Maps

```dart
void main() {
  var planets = {};
}

```

> The type of the map planets is `Map<dynamic, dynamic>`, which is a map with dynamic keys and values. You can also specify the types of the keys and values explicitly.

```dart
void main() {
  var planets = {
    "first": "mercury"
  };
}
```

> The type of the map planets is inferred to be `Map<String, String>`. The keys and values are both strings.

```dart
void main() {
  var planets = {
    1: "mercury",
  }
}
```

> The type of the map planets is inferred to be `Map<int, String>`. The keys are integers and the values are strings.

### Explicitly Typed Maps

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };
}
```

### Accessing Map Elements

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  print(planets["first"]); // mercury
}
```

### Updating Map Elements

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  planets["first"] = "potato";
  print(planets["first"]); // potato
}
```

### Adding Elements to a Map

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  planets["fourth"] = "potato";
  print(planets); // {first: mercury, second: venus, third: earth, fourth: potato}
}
```

### Contains Key

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  print(planets.containsKey("first")); // true
  print(planets.containsKey("fourth")); // false
}
```

### Contains Value

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  print(planets.containsValue("mercury")); // true
  print(planets.containsValue("potato")); // false
}
```

### Removing Elements from a Map

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  String? removed = planets.remove("first");
  print(removed); // mercury
  print(planets); // {second: venus, third: earth}
}
```

### Get All Keys

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  print(planets.keys); // (first, second, third)
}
```

### Get All Values

```dart
void main() {
  Map<String, String> planets = {
    "first": "mercury",
    "second": "venus",
    "third": "earth",
  };

  print(planets.values); // (mercury, venus, earth)
}
```
