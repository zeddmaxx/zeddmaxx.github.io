---
layout: post
title: Adventures with NetworkX
---
I was wanting to do some network analysis and stumbled upon this gem of a library! Well, any manipulation of any sort, you name it, Networkx has it!

In case you’re looking for automated tools that do stuff for you or if you’re too lazy to code, check out Gephi, its really cool(like really).

Otherwise Networkx is our Go-to guy(/girl! Calm down you people! :P )

I am no expert but here are some of the things that wowed me the first time I encountered them :

Brilliant support for Bipartite Graph : Networkx provides brilliant support of functions and iterators for Bipartite graphs. Even though there is no separate class for Bipartite graphs, but you could try out the following and witness the magic unfold :



<code> import networkx as nx
  
<code> from networkx.algorithms import bipartite
  
<code> X = nx.DiGraph()

<code> X.add_nodes_from(<list-of-nodes-Type-1>, bipartite = 0)
  
<code> X.add_nodes_from(<list-of-nodes-Type-2, bipartite = 1)

<code> """ If you don’t believe that the above 4 lines created a bipartite graph see for yourself """

<code> print(bipartite.is_bipartite(X)) 


Haha so now, all you need to do is add edges and visualize this graph using Matplotlib or any other great plotting library.

Random Graphs : If you’ve heard about the Preferential Attachment Model and the Small World Theory, you’ll know what I’m talking about. Networkx allows us to work with random models like Erdos Renyi, Barabasi Albert, Watts-Strogatz and many more. So, its great if you’d like to experiment with random graphs and models.
Network Statistics : From the usual network stats like Centrality, Clustering, Connectedness to complex ones like HITS, Adamic-Adar, Jaccard Coefficient, Page Rank etc; Networkx makes life easy for you!
Support for Classical Algorithms like Dijkstra, Minimum Spanning Tree, DFS, BFS and many more.
