# DemoDAG

Appropriate comments are added at each method level and at the flow

Following is complete algorithm for finding longest distances. 

Initialize dist[] = {NINF, NINF, ….} and dist[s] = 0 where s is the source vertex. Here NINF means negative infinite. 
Create a topological order of all vertices. 
Do following for every vertex u in topological order. 
..Do following for every adjacent vertex v of u 
……if (dist[v] < dist[u] + weight(u, v)) 
………dist[v] = dist[u] + weight(u, v) 
