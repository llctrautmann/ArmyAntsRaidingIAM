# Raid Pattern Model of Army Ants Species
The raid of army ant species is one of the most interesting self-organising phenomena within the family of ants. Thousands of ants leave their nest to swarm huge areas of land and raid other ants' nests or other arthropods to obtain resources and expand their population and territory. This simulation uses data form previous research to model this behaviour. In addition, differences in terrain as well as differences in food availability and pheromone evaporation rates are also modelled. 

# Method
	The current paper created a model following the paper by Deneubourg and colleagues (1989). The model consists of two major components. Firstly, the nodes and secondly the ants that can travel between the nodes. The nodes will be described first. 

## The nodes and the ants
The nodes constitute a class and hold and return different parameter values. In particular, the nodes hold information on their geographic location, connected nodes that are geographically more distant from the origin, connected nodes that are geographically closer to the origin, the level of food, the level of pheromones, a maximum capacity for ants on each node, and a current capacity counter (for a full list see the supplementary code). Every parameter listed above can be updated and returned to facilitate the progress of the model. 
	The ants in the model also constitute a class and have three internal parameters. The location of the ant in the network, the level of food held by the ant, and an identifier. 

## The Model
	The model implementation follows the analytical work laid out in Deneubourg et al (1989). It is designed as a Markov model in which the ants in the network act and move through the network deterministically following probabilities calculated from the level of pheromones on the preceding nodes, the capacity of each node and an evaporation rate for the pheromones trails in the network. Each node

Initially, at each time step in the model, the level of pheromones available is depreciated by an evaporation rate of 1/30. In addition, the following steps occur for all ants that are populating the network of nodes at a given time. Initially, a selected ant checks whether it holds food. As determined by the result there are two paths an ant can take. If it does not hold food, it will travel further away from the next in the network. 
 
## Experiments in this paper
This study conducted four experiments. Initially, the results from the original paper by Deneubourg and colleagues (1989) are replicated. Furthermore, the model is extended to show the effects of three different kinds of terrain changes on the foraging patterns of army ants. Firstly, the effect of random noise is demonstrated. Secondly, the effect of larger impenetrable objects in the pathway of the ants is demonstrated. Lastly, non-random Perlin noise is used to construct more realistic terrain. The resulting terrain is used to demonstrate its effects on the foraging patterns in the ant simulation.
