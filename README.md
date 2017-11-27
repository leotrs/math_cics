# Mathematics for Complex Interconnected Systems

This is a list of mathematical concepts that have been applied to the study
of Complex Interconnected Systems (CICS). Here, by CICS we mean systems
that have been modeled in the literature as either networks (directed,
weighted, multi-layered, hyperedges, etc) or, more recently, as simplicial
complexes.

The purpose is to gather in one place a list of mathematical objects and
techniques that authors have used to study CICS. Usually, presentations of
the mathematical techniques involved in CICS is either delimited to graph
theory, or some technique is presented isolated of all others. Here, we try
to categorize these mathematical objects by the branch of mathematics they
stem from, as well as what is the primary use of each object.

The following list is broken down into sections, one for each broad
mathematical field. Note that many of the concepts in the list could be
categorized under two or more sections. Each item is further labeled with
one of the following labels:

+ `rep`: representation. Mathematical objects that can be used to represent
  CICS. For example, a graph is an `obj` that represents a CICS.
+ `msr`: measure. A concept or algorithm that summarizes a CICS into a
  single number. For example, average degree is a `msr` that summarizes a
  CICS to a real number.
+ `app`: application. A method or technique applying some concepts in order
  to study CICS. For example, spectral clustering is an `app` that uses the
  Laplacian matrix (`rep`) of a graph (`rep`) in order to find communities.
+ `rel`: relation. An object whose purpose is to establish a relationship
  or equivalence between two other objects. For example, graph isomorphism
  is a `rel` that leaves average degree (`msr`) invariant.
+ `obj`: object: other mathematical concepts that do not fit in the
  categories above.

This categorization is completely arbitrary and the authors of the list do
not claim that it is complete or rigorously correct beyond intuition. This
categorization is done due to the fact that there are commonalities in the
study of mathematical objects according to the label attached to an
object. That is, given an object, we can ask the following questions
according to its label.

+ `rep`
  - How much information does this `rep` contain and how does it compare to
    other `rep`s of the same CICS?

+ `msr`
  - What is the range of this `msr`?
  - How efficiently can we compute or approximate this `msr`?
  - Does this `msr` discriminate well between different types of CICS?
  - Is there a `rel` that leaves this `msr` invariant?

+ `app`
  - What is the computational pipeline we need to implement in order to use
    this `app`?
  - Why is this a good way of studying a CICS? What does this `app` tell us
    about the CICS?

+ `rel`
  - Which properties of CICS are fixed by this `rel`? That is which `msr`s
    are invariant under this `rel`?
  - How difficult is it to determine that two CICS are equivalent using
    this `rel`?


# The List

## Graph Theory

### Colorings and homomorphisms `rel`

1. Definition of homomorphism.
   [ref](https://en.wikipedia.org/wiki/Graph_homomorphism)

2. Constraint satisfaction problems can be encoded as graph homomorphism
   problems. [ref](http://www.maths.qmul.ac.uk/~pjc/csgnotes/hom1.pdf)

3. Subgraph frequencies can be counted using homomorphism
   theory. [ref](https://arxiv.org/abs/1304.1548)

4. Manuscript with a short review on results from homomorhpism
   theory. [ref](https://arxiv.org/abs/0902.0132)

### Isomorphisms `rel`

1. Deciding if two graphs are isomorphic is NP but unknown if it's
   NP-complete. [ref](https://en.wikipedia.org/wiki/Graph_isomorphism)

### Graphic matroid `obj`

1. The graphic matroid is a matroid whose independent sets are the forests
   in a given undirected graph.
   [ref](https://en.wikipedia.org/wiki/Graphic_matroid)

### Centrality `msr`

1. Centrality is an indicator of how important an element of CICS
   is. [ref](https://en.wikipedia.org/wiki/Centrality)

2. Many different centrality measures can be studied under the same
   unifying framework. [ref](https://arxiv.org/abs/1312.6722)


## Algebra

### Matrices: adjacency `rep` and Laplace `obj` `rep`

1. These matrices define linear transformations over the set of
   node-functions.

2. One can also multiply these matrices by an arbitrary linear
   transformation. Thus, if the adjacency matrices of two graphs are
   related by a linear operator $L$, we can say that $L$ defines a `rel`
   between them. Eigenvalues are `msr`s held constant by these linear
   `rel`s.

### Spectral Clustering `app`

1. Spectral Clustering is an algorithm that uses the Laplacian Matrix `rep`
   of a graph to find communities (or 'clusters').
   [ref](https://dl.acm.org/citation.cfm?id=2980649)

### The trace monoid of graph walks `obj`

1. 'Walks on graph obey a semi-commutative extension of number-theory. This
   insights raises the possibility of using number-htoeretic sieves to
   count combinatorial objects in graph theory. In particular, the problems
   of counting cycle double covers and simple cycles/paths on a graph are
   both amenable to semi-commutative generalisation of the Selberg
   sieve. My current research aims at exploiting this observation to obtain
   a tractable bound on the asymptotic growth of the number of simple
   cycles on regular lattices.'  [ref](
   https://www.researchgate.net/profile/P-L_Giscard)

### An Hopf algebra for finding simple cycles `obj`

1. [ref](https://hal.archives-ouvertes.fr/hal-01341208v1/document)

### Cycle Space `obj`

1. The set of eulerian subgraphs generates a vector space.
   [ref](https://en.wikipedia.org/wiki/Cycle_space)

### Graphs of groups `obj`

1. [ref](https://en.wikipedia.org/wiki/Graph_of_groups)


## Topology

### Homeomorphism `rel`

1. Leaves invariant all topological `msr`s. The operations of sub-divisions
   and smoothening create homeomorphic graphs.
   [ref](https://en.wikipedia.org/wiki/Homeomorphism_(graph_theory))

### Covering Space `obj`

1. Used in algebraic topology to simplify the study of certain topological
   spaces.
   [ref](http://www3.cs.stonybrook.edu/~gu/lectures/lecture_7_topological_algorithm.pdf)

### Topological Data Analysis `app`

1. [ref](https://www.nature.com/articles/srep01236)

### Embeddings `app`

1. Traditionally, mathematicians tried to draw graphs over the plane or
   other surfaces.
   [ref](https://en.wikipedia.org/wiki/Topological_graph_theory)

2. However, now some authors relax the conditions and try to find
   approximate embeddings (or 'drawings').
   [ref1](https://arxiv.org/abs/1607.00653)
   [ref2](https://www.nature.com/nature/journal/v489/n7417/full/nature11459.html)
   [ref3](https://www.nature.com/articles/srep00793)

### Simplicial complexes `rep`

1. A higher-dimensional way to represent interactions in a CICS.
   [ref](https://en.wikipedia.org/wiki/Simplicial_complex)

### Homotopy and the Fundamental Group `obj`

1. Homotopy-equivalence is a `rel` that is less strict than
   homeomorphism. [citation needed]

2. Homotopy groups contain more information than homology groups.
   [ref](https://en.wikipedia.org/wiki/Hurewicz_theorem)

3. Embeddings vs Homotopy: in embeddings, one tries to place the
   network/CICS as neatly as possible onto a surface or other space. With
   homotopy, one tries to place other spaces (say, a circumference) as
   neatly as possible on the graph.

4. Graph Homotopy: [ref](http://www.sciencedirect.com/science/article/pii/S0012365X01001157)

### Labeling Schemes `app`(?)

1. A labeling scheme on a topological space is an assignment of a label to
   each of its elements. The purpose is to quotient the space by
   identifying the elements with the same label. For example, one can label
   the sides of a polygon, to then identify them and construct the quotient
   space [ref](https://en.wikipedia.org/wiki/Surface_(topology)#Construction_from_polygons).

2. Labeling schemes can be used to study the fundamental group of the
   quotient space
   [ref](https://en.wikipedia.org/wiki/Seifert–van_Kampen_theorem).

3. Can labeling schemes tell us anything about graph homotopy? Read
   [ref](https://www.amazon.com/Topology-2nd-James-Munkres/dp/0131816292)
   ch. 80, sec. "cutting and pasting".

4. An example application using "cutting and pasting", covering spaces, and
   other topological concepts, see
   [ref](https://link.springer.com/chapter/10.1007/978-3-642-40328-6_20).

### Homology `obj` `app`

1. "Two's company, three is a simplex" [ref](https://link.springer.com/article/10.1007/s10827-016-0608-6)

2. "Homological algebra and data"
   [ref](https://www.math.upenn.edu/~ghrist/preprints/HAD.pdf)

3. "Local homology and stratification" [ref](https://arxiv.org/pdf/1707.00354.pdf)

4. A Course on "Toplogy and its Applications" [ref](http://www.chadgiusti.com/math567.html)

### Persistent Homology `app`(?)

1. [citation needed]


## Geometry

### Networks of Manifolds `obj` `rep`(?)

1. [ref](http://emis.ams.org/journals/SIGMA/2015/022/sigma15-022.pdf)

### Curvature `msr`

1. [ref](https://www.mis.mpg.de/de/publications/preprints/2017/2017-34.html)

2. [ref](https://www.nature.com/articles/srep12323)

### volume entropy `msr`

1. [ref](https://arxiv.org/abs/math/0506216)

### Cone over a graph `obj`

1. [ref](https://arxiv.org/pdf/1605.05432.pdf)

### Other references

1. [Thirty essays in Geometrig Graph Theory](https://books.google.com/books?id=2MrOsL7PYn8C&pg=PA554&lpg=PA554&dq=graph+shaving&source=bl&ots=InFJXu8HyD&sig=1JBbIlOy8ntA-r-F9LXAn0Vl_u0&hl=en&sa=X&ved=0ahUKEwic2a2238DWAhUBWBQKHTeIChMQ6AEIQjAH#v=onepage&q=graph%20shaving&f=false)


## Game Theory

1. Evolutionary Dynamics
   [ref](https://www.amazon.com/Evolutionary-Dynamics-Exploring-Equations-Life/dp/0674023382)

2. Games on Graphs
   [ref](https://www.ems-ph.org/journals/show_abstract.php?issn=2308-2151&vol=1&iss=1&rank=3)

3. Evolutionary Games on Graphs
   [ref](https://arxiv.org/abs/cond-mat/0607344)


## Analysis


### Graph convergence `app`(?)

1. [ref1](https://arxiv.org/abs/1401.2906)
   [ref2](https://arxiv.org/abs/1408.0744)

### Graphons `obj` `rep`(?)

1. They are the limiting object of a sequence of dense graphs.
   [ref](https://en.wikipedia.org/wiki/Graphon)

### Modulus `msr` `obj`

1. Provides a generalization of several standard graph-theoretical `msr`s
   that deal with distance.  [ref](https://arxiv.org/abs/1504.02418)


## Probability

### Wasserstein Space `obj` `rep`(?)

1. The space of probability measures over (a.k.a. the Wasserstein Space of)
   a metric space characterizes the space [citation needed]. We can then
   convert the graph/CICS into a metric space and study its Wasserstein
   space.

2. The eigenvalues of the adjacency matrix of a random undirected graph are
   distributed as a semi-circle in the limit of large number of
   nodes. [ref](https://www.jstor.org/stable/1970008)
