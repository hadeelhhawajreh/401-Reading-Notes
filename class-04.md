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
