**Classes and Objects**

*Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects*

```
class MyClass:
    variable = "value"

    def function(self):
        print("This is a message inside the class.")

myobject = MyClass()
```

+ Accessing Object Variables
```
myobject = MyClass()

myobject.variable
```

```
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass()
myobjecty = MyClass()

myobjecty.variable = "yackity"

# Then print out both values
print(myobjectx.variable)
print(myobjecty.variable)
```
output for this code --->
```
blah
yackity
```


Another Exercise

```
# define the Vehicle class
class Vehicle:
    name = ""
    kind = "car"
    color = ""
    value = 100.00
    def description(self):
        desc_str = "%s is a %s %s worth $%.2f." % (self.name, self.color, self.kind, self.value)
        return desc_str
# your code goes here
car1=Vehicle()
car2=Vehicle()
# test code
print(car1.description())
print(car2.description())

```
output -->
```
  is a  car worth $100.00.
  is a  car worth $100.00.
 ```
 
 Thinking Recursively in Python


 ![thinking](https://files.realpython.com/media/Thinking-Recursively-in-Python_Watermarked.1825397c00ea.jpg)
 Problems (in life and also in computer science) can often seem big and scary. But if we keep chipping away at them, more often than not we can break them down into smaller chunks trivial enough to solve. This is the essence of thinking recursively, and my aim in this article is to provide you, my dear reader, with the conceptual tools necessary to approach problems from this recursive point of view.

Together, we’ll learn how to work with recursion in our Python programs by mastering concepts such as recursive functions and recursive data structures. We’ll also talk about maintaining state during recursion and avoiding recomputation by caching results. This is going to be a lot of fun. Onwards and upwards!

```
houses = ["Eric's house", "Kenny's house", "Kyle's house", "Stan's house"]

# Each function call represents an elf doing his work 
def deliver_presents_recursively(houses):
    # Worker elf doing his work
    if len(houses) == 1:
        house = houses[0]
        print("Delivering presents to", house)

    # Manager elf doing his work
    else:
        mid = len(houses) // 2
        first_half = houses[:mid]
        second_half = houses[mid:]

        # Divides his work among two elves
        deliver_presents_recursively(first_half)
        deliver_presents_recursively(second_half)
```

```
def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
```

![img](https://files.realpython.com/media/stack.9c4ba62929cf.gif)
