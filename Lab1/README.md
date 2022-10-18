# Lab01
The solution proposed is based on a greedy tree search algorithm.<br/>
The code structure of the algorithm is taken from 
https://github.com/squillero/computational-intelligence/tree/master/2022-23/min-sum.ipynb.
In my solution instead of using a LIFO or FIFO like for the DF and BF I used a priority queue.<br/>

State are added to queue base on a priority, whose cost computation is partially inspired by 
https://www.geeksforgeeks.org/set-cover-problem-set-1-greedy-approximate-algorithm/.
In this solution, given a state, the cost of pick a subset is computed taking into consideration 
the number of new elements added to the solution.
The queue proposed by the solution exploit 2 priority: 
* the first one is computed counting the number of new elements added to the solution and the one alredy part of the solution (so the total number of elements of witch the solution is composed). 
* the second one, takes into consideration the number of elements, from the subset to add, repeated inside the actual solution <br/>

In this way solution with minor repetition becomes more relevant. <br/>

Collaborators: Lorenzo Bellino