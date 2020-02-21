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


