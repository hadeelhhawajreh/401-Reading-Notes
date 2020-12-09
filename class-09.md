



![img](https://dbader.org/static/figures/python-classes-magic-methods.png)



### Enriching Your Python Classes With Dunder (Magic, Special) Methods



**What Are Dunder Methods?**

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term “dunder methods”, a short form of “double under.”

These “dunders” or “special methods” in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing “magical” about them.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). 

+ *Object Representation: __str__, __repr__*
It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1. __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

2. __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.



```
class Account:
    # ... (see above)

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)

```

+ *Iteration: __len__, __getitem__, __reversed__*
In order to iterate over our account object I need to add some transactions. So first, I’ll define a simple method to add transactions. I’ll keep it simple because this is just setup code to explain dunder methods, and not a production-ready accounting system:


```
class Account:
    # ... (see above)

    def __len__(self):
        return len(self._transactions)

    def __getitem__(self, position):
        return self._transactions[position]
```


+ *To iterate over transactions in reversed order you can implement the __reversed__ special method:*
```
def __reversed__(self):
    return self[::-1]

>>> list(reversed(acc))
[30, -20, 50, -10, 20]
```

+ *Operator Overloading for Comparing Accounts: __eq__, __lt__*

I use the functools.total_ordering decorator which allows me to take a shortcut, only implementing __eq__ and __lt__:

from functools import total_ordering
```
@total_ordering
class Account:
    # ... (see above)

    def __eq__(self, other):
        return self.balance == other.balance

    def __lt__(self, other):
        return self.balance < other.balance
```


**What is probability?
At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:
Flipping a heads
Flipping a tails**
 
