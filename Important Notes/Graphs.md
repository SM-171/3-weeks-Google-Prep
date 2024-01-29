## Main Algorithms in Graphs

1) BFS and DFS Traversal

2) Topological Sort 
   - Linear ordering of vertices such that if there is an edge between u & v, **u** appears before **v** in the ordering
   - Possible only for DAGs (Directed Acyclic Graphs)

   - **Kahn's Algorithm** 
      - For Topo sort using BFS
      - Finds the linear ordering for topo sort using **indegree**.

   - **Important Questions**
     - [Alien Dictionary](https://www.geeksforgeeks.org/problems/alien-dictionary)


## Algos for Finding Single Source Shortest Path
1) Dijkstra's Algorithm
   - Greedy Algorithm
   - Given a source node (starting point) to every node, find the shortest possible path.

   - 3 methods of implementation: Go through all 3 implementations and clear understanding
      - Priority Queue__
         - T.C. = O(E * logV)
         - [Derivation for Time Complexity Analysis is IMP!](https://www.youtube.com/watch?v=3dINsjyfooY&list=PLgUwDviBIf0rGEWe64KWas0Nryn7SCRWw&index=21)
      - Queue
      - Set: More focus to clear how data structure works

2) Bellman Ford Algorithm
   - Relax all edges **(N - 1) times**, N is number of nodes,  sequentially.</br>
   **RELAXATION:**
        ```
        if(dist[u] + wt < dist[v]) {
            dist[v] = dist[u] + wt;
        }
        ```
   - Why exactly (N - 1) iterations?</br>
   Ans: Since, in a graph of N nodes, in worst case, you will take N-1 edges to reach from the first to the last, thereby we iterate for N-1 iterations.

   - How to detect -ve cycle?</br>
   Ans: If in the Nth iteration, relaxation is done and values are updated (because we have proved at max N-1 iterations are needed) then, negative cycle exists. 

## Multi-source Shortest Path Algorithm
1) Floyd Warshal Algorithm
   - It is more of a brute force approach where all the combinations of paths have been tried to get the shortest paths.

   - How to detect a negative cycle?</br>
   Ans: check if the ```cost[i][i] < 0``` then, negative cycle will exist.

   - If the graph is known to not contain a -ve cycle then, we can also apply Dijktra's Algo for each node individually which will have a time complexity of **O(V x E logV)**.

## Spanning Trees
   - Given an undirected, weighted and connected graph G = (V, E), a spanning tree of G is a tree that spans G (includes every vertex of G) and is a subgraph of G.
   - Connected all vertices with minimum no. of edges (N nodes, N - 1 edges) 
   - Cannot be cyclic
   
   ### Minimum Spanning Trees
   - The **cost** of a spanning tree is the sum of weights of all the edges in the tree.
   - **MST** is the spanning tree with the minimum cost among all possible spanning trees of a graph.
   - There can be **more than 1** possible MSTs (eg. if all the weights are the same)

1) Prim's Algorithm
   - Find the cost of MST and all the edges in an MST.

## Strongly Connected Components
   - In a strongly connected component, any two nodes have a path between them i.e. U ---> V and V ---> U is always possible.
   - SCCs are valid only for directed graphs.
   - Two types of questions:
      - Count number of SCCs
      - Print SCCs in order
   
   1) Kosaraju's Algorithm
   - Basic Algorithm
   ```
   1) Sort all the edges according to finishing time [This is done so that we can find the starting node of component 1]
   2) Reverse the graph
   3) DFS on reversed graph [No of DFS rounds gives no. of SCCs in graph]
   ```
   
