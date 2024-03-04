# Number of Subgraphs

Total number of subgraphs = Subgraphs with 1 isolated vertex + Subgraphs with 2 isolated vertices + ... + Subgraphs with n isolated vertices

## Subgraphs with k isolated vertices

We select all combinations of k vertices from the set of all vertices ($\binom{v}{k}$) and for each k-combination we have  $2^{\text{edges from G-\{k vertices\}}}$ subgraphs.

Now, this has turned into another subproblem: to calculate the number of edges not connected to a specific k-vertex subgraph

### Edges in G-{k vertices}

Total number of edges - edges connected to each of the k vertices + edges amongst each of the k vertices 

(adding the last term to avoid double conting)

$=e-\sum\limits_{v\in \text{K vertices}}\deg(v)+\text{edges in K vertices}$

# Formula

Let there be v number of vertices and e number of edges in a graph V.

$$
\sum\limits_{k=0}^{v}\left[\sum\limits_{i\in C(v,j)}2^{e-\sum\limits_{a\in i}\deg(a)+\sum\limits_{b\in C(i,2)}\exists(\text{edge}(b))}\right]
$$

where C(x,y) is a function that takes a set x and a number y and returns combinations of elements of x of size y.
$\exists \text{edge}$ returns 1 if edge exists between a pair of vertices and 0 otherwise.
