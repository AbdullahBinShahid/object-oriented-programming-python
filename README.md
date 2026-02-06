 # **1. What is OOP?**

Object-Oriented Programming (OOP) is a programming paradigm that organizes software design around objects and classes, rather than functions and logic. An object is an instance of a 
class, which is a blueprint for creating objects. OOP focuses on modeling real-world entities and their relationships in a more intuitive and structured way.

For example, if you’re building a car simulation, you might create a Car class. Each car in your program would be an object (instance) of that class, with attributes like color, speed, and model, and behaviors like accelerate() or brake().

## **Why use OOP?**

Modularity: OOP allows you to break down complex problems into smaller, reusable components (objects).

Reusability: Classes and objects can be reused across different parts of a program or in entirely different programs.

Maintainability: Code is easier to maintain and update because it’s organized into logical units.

Scalability: OOP makes it easier to scale and extend programs as requirements grow.

Real-world modeling: OOP closely mirrors real-world entities, making it easier to understand and design systems.

## **4 pillars of OOP**

OOP is built on four fundamental principles:

1.Encapsulation
2.Abstraction
3.Inheritance
4.Polymorphism

## **🔐 Encapsulation**

Wraps data and methods into a single unit (class).
Restricts direct access to internal data (using private/protected attributes).
Helps maintain control, security, and integrity of the data.

## **🎭 Abstraction**

 Hides complex implementation details from the user.
Shows only the essential features and relevant information.
Makes the interface simple while managing complexity behind the scenes.

## **🧬 Inheritance**

Allows a class (child) to inherit properties and behaviors from another (parent).
Promotes code reusability and hierarchical classification.
hild class can override or extend parent functionality.

## **🔁 Polymorphism**

Lets one interface be used for different underlying data types or classes.
The same method name can behave differently based on the object.
Supports flexibility and scalability in code design.

## **What is a Class?**

A class is a blueprint or template for creating objects. It defines the attribute (data) and methods (functions) that the objects created from the class will have. Think of a class as a cookie cutter, and the objects as the cookies made from it.

For example, if you’re creating a program to manage vehicles, you might define a Vehicle class with attributes like color, speed, and model, and methods like accelerate() and brake().

## **What is an Object?**

An object is an instance of a class. It’s a specific realization of the class, with its own unique data. For example, if Vehicle is a class, then my_car and your_car could be objects (instances) of that class, each with its own color, speed, and model. 
   
     #class
     class Car:
    def __init__(self,color,speed,interior):
        self.color=color  # u1-red - u2-white -u3-black
        self.speed=speed
        self.interior=interior


    def accelerate(self):
     self.speed += 10
     print(f"accelerating new speed {self.speed} km/h")

    def brake (self):
     self.speed -= 10
     print(f"accelerating new speed {self.speed} km/h)


    "object"
    my_car = Car("red",10,"white")
    print(my_car)


    car2 = Car("orange",12,"beige")
    print(car2)


    car2.accelerate()
    

## **Explanation of the Code**

Class Definition: The Vehicle class is defined with the class keyword. It has a constructor (init), two methods (accelerate and brake), and a method to display details (display).

Attributes: The color and speed attributes are initialized in the constructor using the self keyword.

Methods: The accelerate and brake methods modify the speed attribute, while the display method prints the current state of the object.

Object Creation: An object my_car is created from the Vehicle class with the color "Red" and speed 60.

Accessing Attributes and Methods: Attributes are accessed using dot notation (my_car.color), and methods are called using parentheses (my_car.accelerate(20)).



## **Defining Attributes and Methods**

Attributes are variables that belong to an object. They represent the object’s state or properties.
Methods are functions that belong to an object. They define the object’s behavior.
For example, in a Vehicle class, color and speed could be attributes, and accelerate() and brake() could be methods

## **The self Keyword**

The self keyword refers to the current instance of the class. It’s used to access attributes and methods of the object within the class. It’s always the first parameter of any method in a class.

##  **What is a Constructor?**

A constructor is a special method that is automatically called when an object of a class is created. It’s used to initialize the object’s attributes or perform any setup required for the object.

## **The __init__ Method**

The __init__ method is the most commonly used constructor in Python. It’s called whenever a new instance of a class is created. You can define this method to initialize the object’s attributes or perform other setup tasks.

In Python, the constructor method is named __init__

## **The __del__ Method (Destructor)**

A destructor is a special method that is called when an object is about to be destroyed. In Python, the destructor method is named __del__. It’s used to perform cleanup tasks, such as releasing resources or closing files.

Syntax:


    class Car:
        # Parameterized constructor
          def __init__(self, brand, model):
             self.brand = brand
             self.model = model

    # Destructor
    def __del__(self):
        print(f"The {self.brand} {self.model} has been destroyed.")


    # Create an object of the Car class
    my_car = Car("Toyota", "Corolla")
    # Explicitly delete the object (triggers the destructor)
    del my_car  # Output: The Toyota Corolla has been destroyed.
    
**Key Takeaways**

1. A class is a blueprint for creating objects.

2. An object is an instance of a class.

3. Attributes define the state of an object, and methods define its behavior.

4. The self keyword is used to refer to the current instance of the class.

5. Objects are created by calling the class name like a function.
     
# ADVANCED OOP:

## **The Four Pillars of OOP**

To fully master OOP, you need to understand its four foundational principles, often called the “Four Pillars.” These pillars are the core of writing clean, reusable, and secure code.

The four pillars of Object-Oriented Programming (OOP) are:

1️⃣ Encapsulation
2️⃣ Inheritance
3️⃣ Polymorphism
4️⃣ Abstraction

 ## **1.🛡️ Encapsulation (The Safety Vault)**
 
Encapsulation is the practice of bundling data (attributes) and the methods (functions) that operate on that data into a single unit (the class), and then restricting direct access to some of the object’s components.

Goal: Data hiding. It protects the data inside the object from being accidentally or maliciously changed from the outside.
Car Example: Think of the internal engine components and the oil level. You don’t directly manipulate the engine’s data. You use the key (start_engine() method) to interact with it, and the oil level is checked through the dipstick (a controlled method). The engine’s inner workings are encapsulated and protected.

##  **2. 🔎 Abstraction (The Simple Interface)**
Abstraction means showing only the essential information to the user and hiding the complex, underlying implementation details.

Goal: Simplicity and clarity. The user only needs to know what the object can do, not how it does it.
Car Example: When you press the brake pedal, you activate the brake() method. You don't need to know about the physics of friction, brake fluid pressure, or rotor rotation. All that complexity is abstracted away, leaving you with a simple action.

## **3. 🌱 Inheritance (The Parent-Child Relationship)**
Inheritance is a mechanism where a new class (the child or subclass) can reuse the properties and behaviors of an existing class (the parent or superclass).

Goal: Code reusability. You define common features once in the parent class, and all child classes automatically get those features.
Car Example: If you create a parent class called Vehicle. It will have methods like refuel() and attributes like wheels. Now, Sedan, Truck, and Motorcycle can all inherit from Vehicle. They instantly get the refuel() method without you having to write it for each one.

## **4. 🎭 Polymorphism (Taking Many Forms)**

Polymorphism literally means “many forms.” It is the ability of an object or method to take on multiple forms or to operate on objects of different types in a uniform way.

Goal: Flexibility. You can use the same method name, but it performs differently depending on the specific object it is called on.
Car Example: Imagine you have a method called make_noise().
If you call it on a Sedan object, it might play a gentle vroom.
If you call it on a Truck object, it might play a loud HONK.
The same command (make_noise()) results in a different, appropriate action for each type of object.

