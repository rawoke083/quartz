---
title: Classes & Objects (OOP)
---


## OOP Quick Review !

> [!note]
> **Classes:** The written down RECIPE of how to bake a CAKE (no actual cake exists yet)
>  
> **Objects:** When a *"Class Comes To Live !"*.  
> * An actual life instance (Object/Cake) of the class.<br />
> * Each instance (Cake) can have different properties (state) like type, color, and frosting
>


<br />

>[!info] Why OOP and What Problem Does It Solve? <br />
> 
> OOP came as a solution to handle complexity by allowing developers to
> 
> #### TLDR: Grouping Data ``properties`` (color, name, age) and behavior ``methods()`` bark(), dance(), run(), sayHello() 
> 
> * Organize: Code in a more structured and manageable way. <br/>
> * Reuse: Code through inheritance, reducing redundancy.
> * Modularize: Code for easier troubleshooting and maintenance.
> * Hide Complexity: Through abstraction, making systems easier to use and develop.
>


> [!example] PHP Class & Object Example
> 

```php
<?php
// Define a class
class Car {
    // Properties
    private string $color;
    private string $make;
    private string $model;

    // Constructor
    public function __construct(string $color, string $make, string $model) {
        $this->color = $color;
        $this->make = $make;
        $this->model = $model;
        echo "Car object created.\n";
    }

    // Destructor
    public function __destruct() {
        echo "Car object destroyed.\n";
    }

    // Method
    public function getDescription(): string {
        return "This is a " . $this->color . " " . $this->make . " " . $this->model;
    }
}

// Create an object (instance of the class)
$myCar = new Car("red", "Toyota", "Camry");

// Access properties and call methods
echo $myCar->getDescription(); // Output: This is a red Toyota Camry

```


<br />


> [!faq] Python Class & Object Example
> 

```python 
# Define a class
class Car:
    # Constructor
    def __init__(self, color: str, make: str, model: str):
        self.color = color  # Properties
        self.make = make
        self.model = model
        print("Car object created.")

    # Destructor
    def __del__(self):
        print("Car object destroyed.")

    # Method
    def get_description(self) -> str:
        return f"This is a {self.color} {self.make} {self.model}"

# Create an object (instance of the class)
my_car = Car("blue", "Honda", "Civic")

# Access properties and call methods
print(my_car.get_description())  # Output: This is a blue Honda Civic
```


## Summary

| Feature             | PHP                                              | Python                                           |
|---------------------|--------------------------------------------------|--------------------------------------------------|
| **Class Definition**| `class ClassName { ... }`                        | `class ClassName: ...`                           |
| **Constructor**     | `public function __construct() { ... }`          | `def __init__(self): ...`                        |
| **Properties**      | Typed properties (from PHP 7.4)                  | Type hints (from Python 3.5) for documentation   |
| **Instantiation**   | `$object = new ClassName();`                     | `object = ClassName()`                           |
| **Inheritance**     | `class ChildClass extends ParentClass { ... }`   | `class ChildClass(ParentClass): ...`             |
| **Access Modifier** | `public`, `protected`, `private`                 | All public, use `_` for protected, `__` for private conventions |
| **Static Methods**  | `public static function methodName() { ... }`    | `@staticmethod` decorator                        |
| **Abstract Classes**| `abstract class ClassName { ... }`               | `from abc import ABC, abstractmethod`            |
| **Interfaces**      | `interface InterfaceName { ... }`                | Python uses abstract base classes (ABCs)         |



## 4 Pillars Of OOP

> [!tip] 1. Encapsulation: Restrict Access to private members and inner workings of class/objects
> 
> Encapsulation is the concept of bundling data and methods together within a class, and controlling access to the class members from outside the class. This helps in maintaining data integrity and code organization.
> It means you can only access the private members of an object via a method (regulated access)
>
> Analogy: Think of a TV remote control as an encapsulation. You have buttons (methods) to change the channel or volume (data), but you can't directly access the internal circuitry (implementation details).

```php 
class BankAccount {
    // Because $balance is "private" you can't do:
    // JoeAccount = new BankAccount(100);
    // JoeAccount->balance = 10000
    // That be a violation since it's private only the CLASS/OBject can access it via this or _self in python
    //
    // You HAVE to go via a method
    //
    // JoeAccount->deposit(10000)

    private float $balance; // Encapsulated property


    public function __construct(float $initialBalance) {
        $this->balance = $initialBalance;
    }

    // Public method to deposit money
    public function deposit(float $amount): void {
        if ($amount > 0) {
            $this->balance += $amount;
            echo "Deposited: $amount\n";
        }
    }
}

$account = new BankAccount(100); // Starting with $100
$account->deposit(50); // Depositing $50

```

<br />

> [!tip] 2. Abstraction:
>
>Abstraction is the process of hiding unnecessary details and exposing only the essential features of an object. It helps in creating a simplified and more generalized representation of complex systems


<br />

> [!tip] 3. Inheritance: Make children classes from parent classes and keep some of the DATA and BEHAVIOR
> What is the same ? (parent class)
>
> What needs to be added or changed (children class)
>


```php
// PHP
class Animal {
    private $name;

    public function makeSound() {
        echo "The animal makes a sound.";
    }
}

class Dog extends Animal {
    public function makeSound() {
        echo "The dog barks.";
    }
}
```
<br />

```python
# Python
class Animal:
    def __init__(self, name):
        self.name = name

    def make_sound(self):
        print("The animal makes a sound.")

class Dog(Animal):
    def make_sound(self):
        print("The dog barks.")
```



<br />

> [!tip] 4. Polymorphism:
>
>Polymorphism allows objects of different classes to be treated as objects of a common superclass.
> 


<br />

```php 
// PHP
class Animal {
    public function makeSound() {
        echo "The animal makes a sound.";
    }
}

class Dog extends Animal {
    public function makeSound() {
        echo "The dog barks.";
    }
}

class Cat extends Animal {
    public function makeSound() {
        echo "The cat meows.";
    }
}

$animals = [new Dog(), new Cat()];
foreach ($animals as $animal) {
    $animal->makeSound();
}
```
