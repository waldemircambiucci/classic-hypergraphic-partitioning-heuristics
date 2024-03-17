[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/wcamb/)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/wcambiuc)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@waldemircambiucci)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/waldemircambiucci/)

# Classic Heuristics for hypergraphic partitioning
Hypergrafic partitioning of quantum circuits for distributed quantum computing.

During this research, we explorer different heuristics for hypergraphic partitioning, as:

FIDUCCIA,C.M., MATTHEYSES, R. M., "A Linear-Time Heuristic for Improving Network Partitions," 19th Design Automation Conference, 1982, pp. 175-181, doi: 10.1109/DAC.1982.1585498.
https://ieeexplore.ieee.org/document/1585498

Brian W KERNIGHAN and Shen LIN. An efficient heuristic procedure for partitioning graphs. The Bell system technical journal, 49(2):291–307, 1970
https://ieeexplore.ieee.org/document/6771089

STOER, M., WAGNER, F. (1997). "A Simple Min-Cut Algorithm." Journal of the ACM, 44(4), 585-591.
https://dl.acm.org/doi/10.1145/263867.263872

Hypergraph partitioning algorithms are widely used in various domains, including quantum computing, for optimizing the layout of circuits across multiple computational units. Here are the main concepts of some prominent hypergraph partitioning algorithms:

1. **Stoer-Wagner Algorithm**:
   - The Stoer-Wagner algorithm is primarily designed to solve the problem of graph min-cut, which involves finding a partition of the graph into two subsets with the minimum total weight of edges cut between them.
   - In the context of hypergraphs, where edges can connect more than two vertices, the algorithm can be adapted to find a partition that minimizes the hyperedge cut, i.e., the total weight of hyperedges cut between partitions.
   - The algorithm iteratively contracts the hypergraph by merging vertices until only two vertices remain. At each step, it computes the weight of edges connecting the contracted vertex with the rest of the hypergraph and selects the vertex with the maximum weight. This process continues until only two vertices remain, providing the optimal partition.

2. **Kernighan-Lin Algorithm**:
   - The Kernighan-Lin algorithm is a heuristic algorithm used for graph partitioning, initially proposed for bipartitioning regular graphs.
   - The algorithm iteratively improves an initial partition by iteratively swapping pairs of vertices between partitions to reduce the cut size.
   - It starts with an initial partition, and at each iteration, it selects pairs of vertices from different partitions and swaps them if the resulting partition improves the cut size. The process continues until no further improvement is possible.
   - The Kernighan-Lin algorithm aims to find a local optimum rather than guaranteeing the global optimum. However, it often produces high-quality partitions in practice with relatively low computational cost.

3. **Fiduccia-Mattheyses Algorithm**:
   - The Fiduccia-Mattheyses (FM) algorithm is another popular heuristic for hypergraph partitioning, focusing on optimizing the balance and cut size of partitions.
   - The algorithm starts with an initial partition and iteratively moves vertices between partitions to reduce the cut size while maintaining balance constraints.
   - It employs a gain function to prioritize vertex movements, where the gain represents the potential improvement in cut size by moving a vertex.
   - FM algorithm iterates until no further improvement in the partition is possible or a termination condition is met.
   - FM algorithm is particularly efficient for partitioning hypergraphs with irregular structures and is widely used in various applications, including quantum circuit partitioning.

In the context of quantum computing, these hypergraph partitioning algorithms can be used to optimize the distribution of quantum circuit operations across distributed quantum processors or qubits, aiming to minimize communication overhead and maximize parallelism for improved performance.
