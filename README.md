# Smart-Cargo-Loading-Plan-Using-GA-Optimization-
The loading plan involves loading the shipment items, each of which weighs a different amount, into the available containers such that the weights of the items are distributed evenly between containers.  For example, if there are six items with weights as follows: item1=17kg, item2=12kg, item3=19kg, item4=6kg, item5=4kg and item6=28kg and they are placed into three containers as follows:
(container1: item1, item3) (container2: item4) (container3: item2, item5, item6).

In this case, container1 weights 36kg (17+19), container2 weights 6kg, and container3 weights 44kg (12+4+28). The difference between these containers is large, so this is a poor loading plan. A much better plan in this instance would be: 
(container1: item1, item2) (container2: item3, item4, item5) (container3: item6).

this project builds a genetic algorithm solution to optimize this container-loading plan. The code works by asking the user to enter the number of containers (c), the number of items (n), and one of the following options to set the weights of the items:
Option 1: The weight of item 𝑖 (where 𝑖 starts at 1 and finishes at n) will be  i/2.
Option 2: The weight of item 𝑖 (where 𝑖 starts at 1 and finishes at n) will be i^2/2.

solution representation: 
a user input population size that consists of chromosomes (each chromosome is an array of items), 
the chromosome consists of genes (each gene represents an item, an item’s value represents the container it’s assigned to). 
In the beginning, the user is asked to input the number of containers, number of items and an option 
for the weight of items which can be either 1 or 2, and insert the population size and mutation 
operator. Once the values are input, then the chromosomes will be generated then the fitness 
function will be applied on them. 
Fitness Function:
The weights of items should be distributed evenly between containers. So, the fitness function 
calculates the difference between biggest total weight and the smallest total weight of containers,
and for the best optimization the fitness value must be as small as possible. Hence, the best fitness 
value would be 0, which means that the item’s weights are distributed evenly and there’s no 
difference.
