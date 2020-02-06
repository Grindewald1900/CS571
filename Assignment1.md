Title         : Welcome
Author        : YRen19
Logo          : True

# CS571 Assignment1

## Authors

Yi Ren  (002269013)

YREN19@UBishops.ca


Wentao Lu (002276355)

WLU19@UBishops.ca

## Exercises

### 1.Does there exist a graph with the following specified properties? Justify
&emsp;**(a)A simple graph with 5 vertices and 12 edges.**  

&emsp;&emsp;&emsp; No, there doesn't exist such a graph.   

&emsp;&emsp;&emsp; Proof：  
&emsp;&emsp;&emsp; The complete graph K<sub>5</sub> has the most edges for a graph with 5 vertices.  
The number of edges for K<sub>5</sub> is 10, which is less than 12.
&emsp;&emsp;&emsp;<center> _e(K<sub>5</sub>) = (5 $\times$ 4)&nbsp;/&nbsp;2 = 10_ </center> 
  
**&emsp;(b)A simple graph in which each vertex has degree 3 and which has exactly 6 edges.**

&emsp;&emsp;&emsp; Yes, there does.   

&emsp;&emsp;&emsp; Proof：  
&emsp;&emsp;&emsp; Suppose that G = (V,E) has n vertices, according to The Handshaking Theorem:
&emsp;&emsp;&emsp;<center> _2 $\times$ e &nbsp; =&nbsp; 3 $\times$ n_  </center>  
&emsp;&emsp;&emsp; In this case,&ensp; e = 6 ,&ensp; n = 4.  
&emsp;&emsp;&emsp; Actually, that is a 4 vertices complete graph.

**&emsp;(c)A simple graph with five vertices with degrees 2, 3, 3, 3, and 2.**  

&emsp;&emsp;&emsp; No, there doesn't exist such a graph.   

&emsp;&emsp;&emsp; Proof：  
&emsp;&emsp;&emsp; Suppose that graph G has 5 vertices with degrees 2, 3, 3, 3, and 2.  
&emsp;&emsp;&emsp; The number of edges for G is 6.5,&ensp;which is not an integer,&ensp;and that is not possible.
&emsp;&emsp;&emsp; <center> _e(G) = (2+2+3+3+3)/2 = 6.5 _ </center>   
&emsp;&emsp;&emsp; Also we can prove it according to Corollary 1.12：  
&emsp;&emsp;&emsp; _An undirected graph has an even number of vertices of odd degree. _  
&emsp;&emsp;&emsp; The number of vertices with odd degree in this graph is 3，which is obviously contrary to the corollary.



### 2.Does there exist a simple graph G with 28 edges and 12 vertices, each of degree 3 or 4?

&emsp;&emsp;&emsp; No, there doesn't exist such a graph.  

&emsp;&emsp;&emsp; Proof：  
&emsp;&emsp;&emsp; Suppose that G = (V,E) has 12 vertices, and every vertex has 4 degrees, the number of edges of graph G will be maximum.
&emsp;&emsp;&emsp;<center> _e(G) = (12 $\times$ 4)/2 = 24 _  </center>  
&emsp;&emsp;&emsp; Obviously , 28 is larger than 24，so it's impossible for graph G to have 28 edges.
&emsp;&emsp;&emsp;
### 3.Does there exist a simple graph G with 28 edges and 12 vertices, each of degree 3 or 6?
### 4.Prove that a graph that contains a triangle cannot be bipartite.
### 5.Must a subgraph of a bipartite graph be bipartite? Would your answer change if, in the definition of a bipartite graph, bipartition sets were required to be nonempty?
### 6.Prove that the number of edges in a bipartite graph with n vertices is n2 at most $\frac{n^2}{2}$_text_
### 7.How many complete bipartite graphs have n vertices?
### 8.Let V = {1, 2,...,n}.
**&emsp;(a)How many simple graphs are there with vertex set V?**  
**&emsp;(b)How many of these graphs contain the triangle 123?**  
**&emsp;(c)What is the total number of triangles in all the graphs with vertex set V?**  
**&emsp;(d)On average, how many triangles does a graph on n labeled vertices contain?**  
### 9.What is the largest possible number of vertices in a graph with 35 edges, all vertices having degree at least 3?
### 10.Suppose all vertices in a graph G have odd degree k. Show that the total number of edges in G is a multiple of k.
### 11.Can there exist a graph with 13 vertices, 31 edges, 3 vertices of degree 1, and 7 vertices of degree 4? Justify.




[reference manual]: http://research.microsoft.com/en-us/um/people/daan/madoko/doc/reference.html  "Madoko reference manual"
