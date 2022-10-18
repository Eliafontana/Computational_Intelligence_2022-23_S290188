# Lab01
The solution proposed is based on a greedy tree search algorithm.<br/>
The code structure of the algorithm is taken from 
https://github.com/squillero/computational-intelligence/tree/master/2022-23/min-sum.ipynb.
In my solution instead of using a LIFO or FIFO like for the DF and BF I used a priority queue.<br/>
State are added to queue base on a priority take into consideration a cost, whose computation partially inspired by 
https://www.geeksforgeeks.org/set-cover-problem-set-1-greedy-approximate-algorithm/.
In this solution, given a state, the cost of pick a subset is computed taking into consideration 
the number of new elements added to the solution.
The fuction that I used to compute cost, consider also the number of unique elements that are already part of the solution.<br/>

Collaborators: Lorenzo Bellino
