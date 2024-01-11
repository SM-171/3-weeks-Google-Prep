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


## Algos for Finding Shortest Path
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
      - Relax all edges **(N - 1) times**, N is number of nodes,  sequentially.__
        **RELAXATION:**__
        ```
        if(dist[u] + wt < dist[v]) {
            dist[v] = dist[u] + wt;
        }
        ```
      - Why exactly (N - 1) iterations?__
      Ans: Since, in a graph of N nodes, in worst case, you will take N-1 edges to reach from the first to the last, thereby we iterate for N-1 iterations.

      - How to detect -ve cycle?__
      Ans: If in the Nth iteration, relaxation is done and values are updated (because we have proved at max N-1 iterations are needed) then, negative cycle exists. 


