## CS571 - Graph Theory and Algorithms
### Take Home Final Exam
### Yi Ren (002269013)

**1. Show that in every simple graph there is a path from every vertex of odd degree to
some other vertex of odd degree**  

Suppose simple graph G (V,E), a vertex u$\in$V with odd degree. And u is not isolated since deg(u) > 0.  
In the component containing u, there must exist at least two vertices with odd degree, because the number of vertices with odd degree should be even. In other words, there should be at least one odd-degree vertex in the same component with u. In this way, these odd-degree vertices could be connected by different paths.


**2.Let G be a simple graph with n vertices with n ≥ 3 and such that the degree of every
vertex in the graph is at least (n - 1)/2.**  
**(a) Show that G has a Hamilton circuit when n is even.**  
When n is even, (n - 1)/2 will not be an integer.   
Hence, the degree of every vertex in the graph should be at least n/2, which is the smallest integer larger than (n - 1)/2.  
According to the Dirac's Theorem, G has a Halmilton circuit.  

**(b) Does G have a circuit when n is odd? If not show at least one counter example.**  
When n is odd, G may not have a Hamilton circuit.  
For example, in figure a below, n is 5 and every vertex in G has at least 2 degrees, however, G only have Hamilton path but not circuit.
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-14.png" width="40%" height="30%"></div>  
</br>
<center>Figure a </center>
</br>

**3. Show how DFS works on the graph of Figure 1. Assume that the for loop of lines 6-10
of the DFS procedure considers the vertices in alphabetical order, and assume that
each adjacency list is ordered alphabetically. Show the discovery and finishing times
for each vertex, and show the DFS forest.**  

We got two DFS trees in this graph, one tree with root a contains 4 vertices a,b,e and d, the other tree with root c contains the rest vertices of graph.  
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/1.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/2.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/3.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/4.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/5.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/6.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/7.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/8.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/9.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/10.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/11.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/12.png" width="40%" height="30%"></div>  
</br>

**4. Show that every DAG must have at least one vertex with no outgoing edges and at
least one vertex without incoming edges.**  

Suppose that DAG G has n vertices(n >= 2), and every vertex in graph G has outgoing edges.  

We start to traverse graph G from an arbitrary vertex, define S to be the Set for all of the discovered vertices. When we choose the next vertex v, it should be a vertex out of Set S, to ensure a cycle wouldn't be formed with vertex v selected. Unfortunately, if vertex v is the last undiscovered vertex, it's impossible to choose a vertex out of Set S, which means a cycle will be formed with an outgoing edge of the last vertex.
Hence, every DAG must have at least one vertex with No outgoing edges.  

For the same reason(we need to change the traverse direction), if every vertex in graph G has incoming edges, a cycle must be formed. So every DAG must have at least one vertex with No incoming edges.

**5. Another way to perform topological sorting on a DAG G = (V, E) is to repeatedly find
vertices of in-degree 0 (see previous question) and store them in a list (or queue) Lin,
and as long as Lin is not empty, remove a vertex from Lin and add it to the front of a
list Lout, and then remove it and all of its outgoing edges from the graph. Then, insert
into Lin any vertex without incoming edges in the obtained subgraph. The list Lout
will store all the vertices of G in a topological sorted order. Write the pseudocode of
the algorithm that implements this idea and analyze its computational cost.**
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/a.png" width="50%" height="50%"></div>  
</br>

The computational cost:  
SPACE: 4|V| + |E|  
We defined 4 variables V,Q1,Q2 and S1, each of them need |V| space. Also the edge set of graph G needs |E| space.  

TIME: $\theta$(|E||V| + |V|)  
In the outer while loop, every iteration will find the vertices of in-degree 0，which need to check all the edges of E. In this way, we need |V|* |E| time for degree checking.   
Then, we need to do ENQUEUE, DEQUEUE and REMOVE for every vertex, so these operations will need 3|V| time.  

**Show how the procedure STRONGLY-CONNECTED-COMPONENTS works on the
graph of Figure 2. Specifically, show the finishing times computed in line 1 and
the forest produced in line 3. Assume that the loop of lines 6-10 of DFS considers
vertices in alphabetical order and that the adjacency lists are in alphabetical order.**
The finishing time is labeled on the vertices, and we got two trees in this graph. One with root q contains 8 vertices q,s,t,v,w,x,y and z, the other tree with root r contains the rest vertices of graph.  
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/21-1024x495.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/22-1024x497.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/23-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/24-1024x496.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/25-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/26-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/27-1024x494.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/28-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/29-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/30-1024x497.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/31-1024x493.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/32-1024x502.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/33-1024x501.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/34-1024x494.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/35-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/36-1024x500.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/37-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/38-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/39-1024x497.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/40-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/40.5-1024x496.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/41-1024x495.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/42-1024x503.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/43-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/44-1024x495.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/45-1024x500.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/46-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/47-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/48-1024x498.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/49-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/50-1024x494.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/51-1024x503.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/52-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/53-1024x494.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/54-1024x502.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/55-1024x493.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/56-1024x494.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/57-1024x499.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/58-1024x495.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/59-1024x497.png" width="60%" height="60%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/04/60-1024x496.png" width="60%" height="60%"></div>  
</br>
