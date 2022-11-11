# Lab 2
## Set covering solved using Genetic algorithm 
The base idea of a genetic algorithm is to create an initial population where each element is created randomly.
Subsequentally, over n genetation (meaning iteration on the population), mutation and crossover manipulation are applied on the population. Given and element of the population, called genome, mutation sightly modifies it. Instead crossover, given 2 or more genomes, recombine different section of these elements in order to create a new genome.
Finally, once offspring are generated, the best elements of the whole population (old population + offspring) are choosed. The choise is made through a fitness.
<br>
Settings:
* Fitness based on a priority tuple (num. of elements covered, - num. of repetitions), with equal  number of elements covered, the more repetitions, the lower is the fittness
* Parent selection: tournament selection, in which the best of n elements picked from the population is selected
* Mutation: both replacement and removing of a random locus (the mutation type is selected randomly)
* Crossover: single cut point for each of the 2 genome selected
</br>
