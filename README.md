# ml-ds-engineering

### Deep Learning Concepts
Gradient Descent: https://www.ibm.com/topics/gradient-descent#:~:text=Gradient%20descent%20is%20an%20optimization,each%20iteration%20of%20parameter%20updates.

### CI/CD
Continuous Integration and Continuous Delivery (CI/CD) is a set of software development practices that aim to automate and streamline the process of building, testing, and delivering software. CI focuses on frequent code integration and automated testing, while CD extends this by automating the delivery and deployment of software changes. The goal is to achieve faster, more reliable, and consistent software releases through automation at various stages of the development lifecycle. CI/CD practices are crucial for modern software development, enhancing collaboration, reducing errors, and enabling rapid, high-quality releases.

### Toml
pyproject.toml is a configuration file used in Python projects to define various aspects of the project, including build system settings, project metadata, and configuration for tools like linters and build systems. It's part of the PEP 518 standard, which introduces a standardized configuration file for Python projects.
https://youtu.be/D_Jb52jw2HY?si=syq_jXqq7PT-Ku3p

### DVC (Data Version Control)
DVC, or Data Version Control, is an open-source tool designed for version control and management of large files and datasets in machine learning (ML) and data science projects. Key features include data versioning, reproducibility, integration with Git, support for parallel and distributed execution, compatibility with various remote storage solutions, and an extensible, open-source nature. DVC allows ML practitioners to track and version datasets efficiently, ensuring reproducibility and collaboration in ML workflows.
https://dvc.org/doc

### *args vs **kwargs
In Python, *args and **kwargs are used in function definitions to handle a variable number of arguments.

*args:

Stands for "arguments" and is used to pass a variable number of non-keyword (positional) arguments to a function.
It collects extra positional arguments into a tuple.
When defining a function, *args allows the function to accept any number of positional arguments.
def example_function(arg1, arg2, *args):
    print("arg1:", arg1)
    print("arg2:", arg2)
    print("Additional args:", args)

example_function(1, 2, 3, 4, 5)
# Output:
# arg1: 1
# arg2: 2
# Additional args: (3, 4, 5)


**kwargs:

Stands for "keyword arguments" and is used to pass a variable number of keyword arguments to a function.
It collects extra keyword arguments into a dictionary.
When defining a function, **kwargs allows the function to accept any number of keyword arguments.

def example_function(arg1, arg2, **kwargs):
    print("arg1:", arg1)
    print("arg2:", arg2)
    print("Additional kwargs:", kwargs)

example_function(1, 2, key1="value1", key2="value2")
# Output:
# arg1: 1
# arg2: 2
# Additional kwargs: {'key1': 'value1', 'key2': 'value2'}

Combining *args and **kwargs:

You can use both *args and **kwargs in a function definition to accept any combination of positional and keyword argument

def example_function(arg1, arg2, *args, **kwargs):
    print("arg1:", arg1)
    print("arg2:", arg2)
    print("Additional args:", args)
    print("Additional kwargs:", kwargs)

example_function(1, 2, 3, 4, key1="value1", key2="value2")
# Output:
# arg1: 1
# arg2: 2
# Additional args: (3, 4)
# Additional kwargs: {'key1': 'value1', 'key2': 'value2'}

### @classmethod decorator
The @classmethod decorator in Python is used to define a class method. A class method is a method that is bound to the class and not the instance of the class. It takes the class as its first parameter (usually named cls) rather than an instance.

Here's a simple example to illustrate the usage of @classmethod:
class MyClass:
    class_variable = "I am a class variable"

    def __init__(self, instance_variable):
        self.instance_variable = instance_variable

    @classmethod
    def class_method(cls):
        print("This is a class method")
        print(f"Accessing class variable: {cls.class_variable}")

# Creating an instance of MyClass
obj = MyClass("I am an instance variable")

# Calling the class method on the class itself
MyClass.class_method()

# Output:
# This is a class method
# Accessing class variable: I am a class variable



