---
layout: splash
title: "Graph Analyser"
date: 2020-5-23
author_profile: false
tags: [java, graphs, algorithm, topological ordering, cycles]
header:
excerpt: "Graph Analyser"
---
# Graph Analyser Assignment

This assignment was actually one that I did for my algorithms paper at university.
It involved the implementation of a few algorithms that I had been learning in Java.
These algorithms centered around using modified versions of the DFS and BFS algorithms
in digraphs in order to check whether they had cycles or were in topological order.

This also involved being able to manipulate read data into the algorithm. This was
through an adjusted adjacency list.

An example of the analysis can be see with this exemplar graph:

<img src="{{ site.url }}{{ site.baseurl }}/images/graph/graph1.JPG" alt="">

The output of the code when entering this code after input is:

<img src="{{ site.url }}{{ site.baseurl }}/images/graph/output1.JPG" alt="">

1. The first line is representative of the two nodes on the directed graph that have
the same in and out degrees - which are node 1 and node 5.
2. The second line shows the average in and out degrees of the nodes
3. The third line scans the graph with a DFS algorithm to detect whether it has
cycles, and since it doesn't it outputs Order:
4. The fourth line hence outputs the topological ordering of the graph
5. The last line checks if the graph has at most three cycles or not, and since it
has a topological ordering and no cycles, this is true


Another example of a digraph with cycles can be seen below:

<img src="{{ site.url }}{{ site.baseurl }}/images/graph/graph2.JPG" alt="">

The output of the code when entering this code after input is:

<img src="{{ site.url }}{{ site.baseurl }}/images/graph/output2.JPG" alt="">

The line representation is the same as the graph first shown. The difference exists
from line 3 onwards:
3. As cycles exist in the current graph it displays cycle(s):
4. The graph outputs an example of a cycle, as there is a path from node 0 going
to itself, this is an example of a cycle
5. The algorithm also scans the graph and counts the number of cycles, as there is
at most three cycles in this graph it shows Yes


Overall this assignment was super rewarding to do. I learned a lot about implementation
of algorithms that I had merely written down on paper and gained a stronger understanding
of how they functioned in conjunction with the data structures that they were represented
in.
