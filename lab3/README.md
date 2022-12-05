# Lab 3 (Nim)
## Create an agent that exploit evolving rules (3.2)
### Parameters evolution
The evolution of parameters, it's implemented using a classic genetic algorithm.
<br/>We start with an initial population randomly initialized, and at each iteration (generation) 
parameters are tweaked by increasing or decreasing their value of small steps. The fitness is represented by a winning rate over N matcher (set to 100). At the end of the generation step, the best individuals are selected.</br>
### Paramenter choice
After defining a set of possible moves (more or less reasonable), I tried to parametrize this fixed rules.
I used as parameter the probability of pick a rule instead of another, tring also to combine them. 
<br/>Apart from some simple rules results are quite poor.</br>
<br/>For this reason I move the attention on find a sort of function that exploit one or more parameter to made a choice on the next move.</br>
After some blind trials I "found" the following function:
<br/>sum - n_r / sum < t</br>
<br/>
* sum is the number of total element before the current move.
* n_r is the number of elements removed taking into consideration the ith available rows (that consequently define the move to do).
* t simply represent a threshold and is our parameter to tweak.
</br>
<br/>The normalization is made in order to squash t between 0 and 1.
Finally, from the set of possible moves found we pick the one that maximize the number of elements removed. If there are no possible move that satisfies the constrain a random row is choosed.</br>

### Conclusion
Using this approach I obtain a win rate between 0.6 and 0.75 against the random strategy.
However I'm not sure about the goodness of my solution.


