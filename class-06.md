### Random Module in Python

**When to use it?**
We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. When making your password database more secure or powering a random page feature of your website.

Random functions

The Random module contains some very useful functions.

+ Randint
    If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.
    ```
    import random
    print random.randint(0, 5)
    ```
     > This will output either 1, 2, 3, 4 or 5.

Random
If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:
```
import random
random.random() * 100
```
+ Choice
  Generate a random value from the sequence sequence.
  
> random.choice( ['red', 'black', 'green'] ).
  The choice function can often be used for choosing a random element from a list.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

+ Shuffle

The shuffle function, shuffles the elements in list in place, so they are in a random order.

```from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```
#### Risk Analysis in Software Testing

![r](https://www.vatikagroup.com/blog/wp-content/uploads/risk-management.png)

Why use Risk Analysis?

In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.


There are different sets of risks included in the risk identification process. Those are as follows:

*Business Risks:* This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

*Testing Risks:* You should be well acquainted with the platform you are working on, along with the software testing tools being used.

*Premature Release Risk:* a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

*Software Risks:* You should be well versed with the risks associated with the software development process.

Risk Assessment
![r](https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/08/Picture1-768x422.png)

*Effect* – To assess risk by Effect. In case you identify a condition, event or action and try to determine its impact.

*Cause *– To assess risk by Cause is opposite of by Effect. Initialize scanning the problem and reach to the point that could be the most probable reason behind that.

*Likelihood* – To assess risk by Likelihood is to say that there is a probability that a requirement won’t be satisfied.
