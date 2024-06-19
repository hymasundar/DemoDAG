# DemoDAG

Appropriate comments are added at each method level and at the flow.

Tested with a sample test data DemoDAG file by adding edges. The addition of edges can be changed specific to the given problem. This is a generic solution should work for all DAG's in finding the longest path.

Following is complete algorithm for finding longest distances. 

Initialize dist[] = {NINF, NINF, ….} and dist[s] = 0 where s is the source vertex. Here NINF means negative infinite. 
Create a topological order of all vertices. 
Do following for every vertex u in topological order. 
..Do following for every adjacent vertex v of u 
……if (dist[v] < dist[u] + weight(u, v)) 
………dist[v] = dist[u] + weight(u, v) 

Time Complexity: Time complexity of topological sorting is O(V+E). After finding topological order, the algorithm process all vertices and for every vertex, it runs a loop for all adjacent vertices. Total adjacent vertices in a graph is O(E). So the inner loop runs O(V+E) times. Therefore, overall time complexity of this algorithm is O(V+E).

Space complexity : O(V + E), where V is the number of vertices and E is the number of edges in the graph. 
