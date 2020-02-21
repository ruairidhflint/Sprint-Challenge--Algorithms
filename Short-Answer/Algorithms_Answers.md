#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)

Answer = O(n) 
Reasoning = Initially, seeing a loop as well as multiple instances of n multipling itself, one could be tricked
into thinking that it is a more complex algorithm than it really is. 

The important part is that whilst we are competing against n * n * n, on each iteration a is increased by n * n, which cancels
out the while loop essentially to just increasing by n. 

An example would be, assuming n is 5...the while loop runs on the condition that a is less than 125 (5*5*5). Each time
the loop runs, a is increased by 25 (5*5).

If we increase n to say, 10, the while loop runs on the condition that a is less than 1000 (10 * 10 * 10). Whilst that is a big increase
from 5, we also incrememnt by 100 each time, taking just ten iterations, therefore making this algorithm linear time. 


b)
Answer = O(n^2) (probably)
Reasoning = My reasonins simply a loop within a loop gives us n * n. However I am slightly torn because
the j *= 2 means that the while loop is very efficient and runs far less than expected. Which means there
is a logarithmic aspect. Regardless, the larger n, the more times the loop will run, even if less than expected.


c)

Answer = O(n) 
Reasoning: As a recursive function, the function inside will continually be called until the base case is met, meaning
the amount of calls is directly dependent on the input of n, making it linear time. 

## Exercise II

This is an ideal example of a situation to implement a binary search. 

We set three values
- The lowest known  point
- highest known point
- The middle

Initially, the lowest point will be the ground floor, zero. The highest is the top floor and the middle is the top and bottom combined 
and divided by two. 

So in a building of 100 floors, the middle is 50. 

We drop the egg from the middle. Does it break? If yes, we know the lowest floor from which it is safe to drop from must be below
the 50th floor.

We adjust our three values by moving the high point to what was our middle, and the low point stays the same and the middle becomes
the new half way point between high and low. 

Alternatively, if the egg did not break, the high stays the same, the middle becomes the low and the new middle is the half way point again.

We repeat this process and very quickly and efficiently will reach the exact floor on which the egg does not break whilst barely wasting any eggs
at all. 

Time Complexity will equal O(log n) <-- Very good!
