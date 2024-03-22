# Grassfire vs A*
This python notebook creates a 2D-map with random start, end positions and random obtacles. The later blocks of code implement the Grassfire and the A* path finding algorithms and generates GIFs visualising these algorithms for comparison. 

## Grassfire Algorithm
Grassfire algorithm tries to reach the destination node by iteratively visiting new neighbouring nodes, assigning the new neighbour node's 'value' as one greater than current node's value, starting from the 'start' node with 0 value. Visually Similar to how fire spreads from a point in a grass-lawn.

## A* Algorithm
Unlike the grassfire algorithm,this algorithm uses the knowledge of destination node's location to prioritise nodes that have high probability of being in the shortest path. Here, each node's value is the sum of distance from the start (value used in grassfire) and a heuristic distance (euclidean/manhattan) from the node's location to the destination node.
This sum is a heuristic estimate of the minimum path length through that node. 
In each iteration, the neighbours of the node with the smallest value is visited. New nodal values are computed (or better values are updated, if found). The procedure is repeated now for a larger list of nodes which includes the newly visited nodes. Algorithm is terminated once the destination is reached. 

## Comparison
The code was run for a 20x20 map and the following algorithm performance comparison was made. 
