###### Readings: Testing and Modules

**Unit tests** are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.
But *Test-Driven Development*
is a strategy to think (and write!) tests first.

*A convention widely used is the AAA: Arrange, Act and Assert.*
+ Arrange: you need to organize the data needed to execute that piece of code (input);

+ Act: here you will execute the code being tested (exercise the behaviour);

+ Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

The cycle is made by three steps:

🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

✅ Write the feature and make the test pass! (you can dance after that)

🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)

**TDD is not about the money/tests**
More than any checking, we need to think about our software design first.

One of the things that amaze me about TDD is how we can grow our software design consciously and well, just building what is needed to make the test pass.
When we are writing tests we are forced to think about the design first and how we can break it into small pieces.

![img](https://miro.medium.com/max/875/1*dTd_0x8gdefpRt9tUtekPQ.png)

# Recursion

+ *What is Recursion?*
   The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.
   Using recursive algorithm, certain problems can be solved quite easily. 


```
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```
+ *What is base condition in recursion? *
   In the recursive program, the solution to the base case is provided and the solution of the bigger problem is expressed in terms of smaller problems. 
   
   
