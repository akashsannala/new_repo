Step-by-Step Implementation

Set dist[source]=0 and all other distances as infinity.
Push the source node into the min heap as a pair <distance, node> → i.e., <0, source>.
Pop the top element (node with the smallest distance) from the min heap.
For each adjacent neighbor of the current node:
Calculate the distance using the formula:
dist[v] = dist[u] + weight[u][v]
    If this new distance is shorter than the current dist[v], update it.
    Push the updated pair <dist[v], v> into the min heap
Repeat step 3 until the min heap is empty.
Return the distance array, which holds the shortest distance from the source to all nodes.