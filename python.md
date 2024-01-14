# Python

## Object-oriented programming (OOP) 
OOP is a programming paradigm that uses objects – which are instances of classes – to organize code. OOP is based on four main principles: encapsulation, inheritance, polymorphism, and abstraction. Let's delve into each of these concepts:

#### 1. Encapsulation:

Encapsulation is the bundling of data (attributes or properties) and methods (functions or procedures) that operate on the data into a single unit called a class.
The class serves as a blueprint for creating objects, and it hides the internal details of the implementation from the outside world.
Access to the data and methods is controlled through access specifiers (public, private, protected) to ensure proper encapsulation.

class Car:
    def __init__(self, brand, model):
        self.brand = brand  # public attribute
        self.__model = model  # private attribute

    def display_info(self):
        print(f"Car: {self.brand}, Model: {self.__model}")

my_car = Car("Toyota", "Camry")
my_car.display_info()
# Accessing public attribute
print(my_car.brand)
# Accessing private attribute (will result in an error)
# print(my_car.__model)
