---
title: Classes
description: A reference page in my new Starlight docs site.
sidebar:
  order: 8
---

## Classes

```dart
void main() {
  var noodles = MenuItem("veg noodles", 9.99);
  print(noodles.title); // veg noodles
  print(noodles.price); // 9.99
}

class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);
}
```

> In the above code, we define a class called `MenuItem` with two properties: `title` and `price`.

> The constructor takes two parameters and assigns them to the properties.

> In Dart, to access a property in a class, we use the dot operator (`.`) followed by the property name.

### Methods

```dart
void main() {
  var noodles = MenuItem("veg noodles", 9.99);
  print(noodles.format()); // veg noodles --> 9.99
}

class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);

  String format() {
    return "$title --> $price";
  }
}
```

### Inheritance

```dart
void main() {
  var pizza = Pizza(
    ["mushrooms", "onions", "peppers"], "veg volcano", 15.99
);
  print(pizza.format());
}

class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);

  String format() {
    return "$title --> $price";
  }
}

class Pizza extends MenuItem {
  List<String> toppings;

  Pizza(this.toppings, String title, double price) : super(title, price);
}
```

### Shorthand Constructor

```dart
void main() {
  var pizza = Pizza(
    ["mushrooms", "onions", "peppers"], "veg volcano", 15.99
);
  print(pizza.format());
}

class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);

  String format() {
    return "$title --> $price";
  }
}

class Pizza extends MenuItem {
  List<String> toppings;

  Pizza(this.toppings, super.title, super.price);
}
```
