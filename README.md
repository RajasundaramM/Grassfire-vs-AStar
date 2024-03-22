# Grassfire vs A*
This python notebook creates a 2D-map with random start and end positions, and obtacles. The later blocks of code implement the Grassfire and the A* path finding algorithms and generates GIFs visualising these algorithms for comparison. 

## Grassfire Algorithm
Grassfire algorithm tries to reach the destination node by iteratively visiting new neighbouring nodes, assigning each new neighbouring node a value one greater than the current node, starting from the 'start' node with value=0. Visually Similar to how fire spreads from a point in a grass-lawn.

## A* Algorithm
Unlike the grassfire algorithm,this algorithm uses the knowledge of destination node's location to prioritise nodes that have high probability of being in the shortest path. Here, each node's value is the sum of distance from the start (value used in grassfire) and a heuristic distance (euclidean/manhattan) from the node's location to the destination node.
This sum is a heuristic estimate of the minimum path length through that node. 
In each iteration, the neighbours of the node with the smallest value is visited. New nodal values are computed (or better values are updated, if found). The procedure is repeated now for a larger list of nodes which includes the newly visited nodes. Algorithm is terminated once the destination is reached. 

## Comparison
The code was run for a 20x20 map and the following comparison was made. 

### _Grassfire_

 ![](https://github.com/RajasundaramM/Grassfire-vs-AStar/blob/main/Grassfire.gif) 

 
 
### _A*_
 
 ![](https://github.com/RajasundaramM/Grassfire-vs-AStar/blob/main/AStar.gif) 

As demonstrated above, the A* algorithm is more efficient than the Grassfire algorithm since it prioritizes certain nodes for exploration based on the location of the destination node. 
 Though the worst-case computational time complexity of both these algorithms in this problem is **O(n^2)**, where n is the side length of the grid, it is not too hard to observe and conclude that the A* algorithm would find the path quicker than the Grassfire algorithm in most cases. 
