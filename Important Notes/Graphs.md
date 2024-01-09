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

3) Dijkstra's Algorithm 
   - Most important for solving - shortest path from A->B
   - Greedy Algorithm
   - Given a source node (starting point) to every node, find the shortest possible path.

   - 3 methods of implementation
      - Priority Queue
      - Queue
      - Set

