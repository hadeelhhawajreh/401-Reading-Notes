                                                                                                  
## Big O notation  is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.


![o](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSvhmflwpYAagTV4k3WKz3Lj3BH8i0pvc63jA&usqp=CAU)


1. **O(1)**

*O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.*
```
bool IsFirstElementNull(IList<string> elements)
{
    return elements[0] == null;
}
```
  
2. **O(N)**

*O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.*
```
bool ContainsValue(IList<string> elements, string value)
{
    foreach (var element in elements)
    {
        if (element == value) return true;
    }

    return false;
}
```

![o2](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRE-tjS6FtIhCG1ZDPckXhnZIOUVT_q4jWiGg&usqp=CAU)
3. **O(N2)**

*O(N2) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.*
```
bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++)
    {
        for (var inner = 0; inner < elements.Count; inner++)
        {
            // Don't compare with self
            if (outer == inner) continue;

            if (elements[outer] == elements[inner]) return true;
        }
    }

    return false;
}
```

4. **O(2N)**

*O(2N) denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically. An example of an O(2N) function is the recursive calculation of Fibonacci numbers:*
```
int Fibonacci(int number)
{
    if (number <= 1) return number;

    return Fibonacci(number - 2) + Fibonacci(number - 1);
}
```


![o3](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3StSPOeFJD8OosriZGSuzx2BAYnRxn-L9TQ&usqp=CAU)
  
