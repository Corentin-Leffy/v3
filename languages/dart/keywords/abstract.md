# Abstract

The keyword `abstract` is used to define an *abstract class* - a class that can not be instantiate directly, which means
you can not create an object from it. Conversely, a class that can be instantiated directly is called a *concrete class*.

Abstract types can define interfaces which hide the implementation details and showing only functionality to the user. 
They let you focus on **what** the object does instead of **how** it does it.

```dart
// This class is declared abstract and thus
// can't be instantiated.
abstract class CoffeeMachine {
  //Body of abstract class
}

CoffeeMachine coffeeMachine = CoffeeMachine(); // Abstract classes can't be instantiated.
```

An abstract class can have constructors, fields, methods. Abstract methods define the class behaviour. They can only 
exist within an abstract class and are delimiting by a semicolon (;).

```dart
abstract class CoffeeMachine {
  void makeEspresso(); // Abstract method
  void makeCoffee() { // Normal method
    print("Making coffee");
  }
}
```

When concrete classes extend the abstract class, they have to override every abstract method. It is not mandatory to 
override normal method.

```dart
class SpecialCoffeeMachine extends CoffeeMachine {
  @override
  void makeEspresso() {
    print("Making a delicious espresso");
  }
}
```