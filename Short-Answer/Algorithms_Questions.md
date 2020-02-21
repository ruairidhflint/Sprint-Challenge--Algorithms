# Analysis of Algorithms

## Exercise I

Give an analysis of the running time of each snippet of
pseudocode with respect to the input size n of each of the following:

```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n


Answer = O(n) 
Reasoning = Initially, seeing a loop as well as multiple instances of n multipling itself, one could be tricked
into thinking that it is a more complex algorithm than it really is. 

The important part is that whilst we are competing against n * n * n, on each iteration a is increased by n * n, which cancels
out the while loop essentially to just increasing by n. 

An example would be, assuming n is 5...the while loop runs on the condition that a is less than 125 (5*5*5). Each time
the loop runs, a is increased by 25 (5*5).

If we increase n to say, 10, the while loop runs on the condition that a is less than 1000 (10 * 10 * 10). Whilst that is a big increase
from 5, we also incrememnt by 100 each time, taking just ten iterations, therefore making this algorithm linear time. 
```


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)

Answer = O(n) 
Reasoning: As a recursive function, the function inside will continually be called until the base case is met, meaning
the amount of calls is directly dependent on the input of n, making it linear time. 
```

## Exercise II

Suppose that you have an n-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. Devise a strategy to determine the value of f such that the number of dropped + broken eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode AND give the runtime complexity of your solution.
