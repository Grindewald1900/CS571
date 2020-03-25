## CS571 - Graph Theory and Algorithms
### Assignment 3
### Group members :
### Yi Ren (002269013)&ensp;&ensp;    Wentao Lu (002276355)  

**5. Devise an algorithm for constructing Euler circuits in directed graphs.**  
&ensp;(1) Loop all the vertices in graph G(V,E).  
&ensp;(2) If there exists a vertex whose in-degree is inequal to its out-degree, graph G doesn't have an Euler circuit.  
&ensp;(3) Else, an Euler circuit should exist.  
&ensp;(4) Start at any vertex, then select one edge to begin.  
&ensp;(5) Loop: choose the edges successively and remove the choosen edge from edge set E, Until E is empty.


**7. Fleury's algorithm, published in 1883, constructs Euler circuits by first choosing an arbitrary vertex of a connected multigraph, and then forming a circuit by choosing edges successively. Once an edge is choosen, it is removed. Edges are chosen successively so that each edge begins where the last edge ends, and so that this edge is not a cut edge unless there is no alternative.**  
**&ensp;(a)Express Fleury's algorithm in pseudocode.**  

&ensp; &ensp; pseudocode in natural language:
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/2.png" width="60%" height="60%"></div>  
</br>

&ensp; &ensp; pseudocode in C language:  

<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/1-1024x717.png" width="90%" height="90%"></div>  
</br>

**(b)Use Fleury's algorithm to find an Euler circuit in the graph in Figure 3.9.**
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-1.png" width="40%" height="30%"></div>  
</br>
(1) Select f as the first vertex.  
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-2.png" width="40%" height="30%"></div>  
</br>
(2) Choose (f,c).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-3.png" width="40%" height="30%"></div>  
</br>
(3) (c,b) is a cut edge, so we choose (c,d).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-4.png" width="40%" height="30%"></div>  
</br>
(4) Choose (d,e).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-5.png" width="40%" height="30%"></div>  
</br>
(5) Choose (e,c).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-6.png" width="40%" height="30%"></div>  
</br>
(6) Choose (c,b), because it is the only choice.
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-7.png" width="40%" height="30%"></div>  
</br>
(7) Choose (b,a).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-8.png" width="40%" height="30%"></div>  
</br>
(8) Choose (a,f).
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-9.png" width="40%" height="30%"></div>  
</br>
So here's the Euler circuit: f -> c -> d -> e -> c -> b -> a -> f
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-10.png" width="40%" height="30%"></div>  
</br>

**8. Show that the Petersen graph in Figure 3.10, does not have a Hamilton circuit, but that the subgraph obtained by deleting a vertex v, and all edges incident with v, does have a Hamilton circuit.**  
&ensp;&ensp;We can choose any vertex in the Petersen graph to remove, because every vertex has the same degrees. If one of the vertices is removed, there remain 3 vertices with 2 degrees and 6 vertices with 3 degrees.  
&ensp;&ensp;One interesting fact is that we can find 3 vertex pair among the 3-degree vertices. If we remove one edge between each vertex pair, all the vertices will remain 2 degrees, which means the edges remained will form a circuit.

Example  

<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-11.png" width="40%" height="30%"></div>  
</br>
<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-13.png" width="40%" height="30%"></div>  
</br>

**9. Can you find a simple graph with n vertices with n > 3 that does not have a Hamilton circuit, yet the degree of every vertex in the graph is at least (n — 1)/2?**

<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-14.png" width="40%" height="30%"></div>  
</br>


**11.Show that a bipartite graph with an odd number of vertices does not have a Hamilton circuit.**  
&ensp;&ensp;Suppose bipartite graph G has n vertices where n is an odd number, and the number of vertices in two subsets A and B are respectively a and b, so we will have
&ensp;<center>**a + b = n**</center>  
&ensp;&ensp;Let a < b (or b < a), note that a and be should be inequal because n is odd, so  
&ensp;<center>**a <= (n-1)/2**</center>  

 &ensp;&ensp;If we pick up two vertices V1,V2 from subset B, it's obviously that the degree of any vertex in B is no larger than a, so  
 <center>**deg(V1) + deg(V2) <= 2a <= n-1** </center>  
&ensp;&ensp;We will have
&ensp;<center> **deg(V1) + deg(V2) <= n** </center>  
&ensp;&ensp;which violates the Ore's theorem.

<div align=center><img src="http://15.222.11.163/wp-content/uploads/2020/03/3-16.png" width="40%" height="30%"></div>  
</br>
