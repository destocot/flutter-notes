---
title: Method Overriding
description: A reference page in my new Starlight docs site.
sidebar:
  order: 9
---

## Method Overriding

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

  @override
  String format() {
    var formattedToppings = "Contains:";

    for (final t in toppings) {
      formattedToppings = "$formattedToppings $t";
    }

    return "$title -> \$$price \n$formattedToppings";
  }
}
```

> Here the `Pizza` class extends the `MenuItem` class and overrides the `format` method to provide a custom string representation that includes the toppings of the pizza.

### Override Built-in Methods

```dart
void main() {
  var pizza = Pizza(
    ["mushrooms", "onions", "peppers"], "veg volcano", 15.99
);
  print(pizza); //  Instance of 'Pizza'
}
```

> By default, when you print an object, it prints the instance of the class. To change this behavior, you can override the `toString` method.

```dart
class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);

  String format() {
    return "$title --> $price";
  }

  @override
  String toString() {
    return format();
  }
}

class Pizza extends MenuItem {
  List<String> toppings;

  Pizza(this.toppings, super.title, super.price);

  @override
  String format() {
    var formattedToppings = "Contains:";

    for (final t in toppings) {
      formattedToppings = "$formattedToppings $t";
    }

    return "$title -> \$$price \n$formattedToppings";
  }
}
```

> Now, when you print the `pizza` object, it will call the overridden `toString` method, which in turn calls the `format` method.

```dart
void main() {
  var pizza = Pizza(
    ["mushrooms", "onions", "peppers"], "veg volcano", 15.99
  );
  print(pizza);
}
```

```
veg volcano -> $15.99
Contains: mushrooms onions peppers
```

####### Example

> We are overriding the `toString` method in the parent class `MenuItem`.

> We can also override the `toString` method in the child class `Pizza`.

```dart
class MenuItem {
  String title;
  double price;

  MenuItem(this.title, this.price);

  String format() {
    return "$title --> $price";
  }

  @override
  String toString() {
    return format();
  }
}
class Pizza extends MenuItem {
  List<String> toppings;

  Pizza(this.toppings, super.title, super.price);

  @override
  String format() {
    var formattedToppings = "Contains:";

    for (final t in toppings) {
      formattedToppings = "$formattedToppings $t";
    }

    return "$title -> \$$price \n$formattedToppings";
  }

  @override
  String toString() {
    return "Instance of Pizza: $title, $price, $toppings";
  }
}
```

> Now, when you print the `pizza` object, it will call the overridden `toString` method in the `Pizza` class.

```dart
void main() {
  var pizza = Pizza(
    ["mushrooms", "onions", "peppers"], "veg volcano", 15.99
  );
  print(pizza);
}
```

```
Instance of Pizza: veg volcano, 15.99, [mushrooms, onions, peppers]
```
