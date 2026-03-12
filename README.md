# Catch Me If You Can Network Analysis

## Authors

- Giorgio Vanini
- Arianna Cambi
- Sofia Capriolo
- Andrea Cipollo
- Maiia Kopalina

## Project Overview

This project applies Social Network Analysis to the movie *Catch Me If You Can*. The analysis is implemented in Python and documented in the notebook [`Catch_me_if_you_can_weeks.ipynb`](/Users/mayako/Desktop/SNA_Project/Catch_me_if_you_can_weeks.ipynb).

The selected network is a movie character network:

- **Network:** *Catch Me If You Can* movie network
- **Type:** undirected, weighted social network
- **Meaning of nodes:** characters
- **Meaning of edges:** two characters appear in the same scene
- **Meaning of weights:** number of shared-scene appearances

**Source:** J. Kaminski et al., *Moviegalaxies - Social Networks in Movies*, Harvard Dataverse, V3 (2018).

## Project Files

- [`Catch_me_if_you_can_weeks.ipynb`](/Users/mayako/Desktop/SNA_Project/Catch_me_if_you_can_weeks.ipynb): main notebook with the full analysis
- [`datasets/nodes.csv`](/Users/mayako/Desktop/SNA_Project/datasets/nodes.csv): node list
- [`datasets/edges.csv`](/Users/mayako/Desktop/SNA_Project/datasets/edges.csv): edge list
- [`datasets/gprops.csv`](/Users/mayako/Desktop/SNA_Project/datasets/gprops.csv): graph metadata

## Assignment Tasks

### Weeks 1-2-3

#### Week 1

a) Pick a social network among the ones proposed on `luiss.learn`.

b) Implement it in Python.

c) Draw the graph.

d) Compute the number of nodes, edges, average degree, and density. Comment on the results.

Be careful whether the selected network is directed or not.

#### Week 2

While considering the largest connected component of the network:

a) Design a function computing the clustering at every node and another one computing the average clustering.

b) Compare the custom implementation to the built-in functions. Compute average clustering and transitivity.

#### Week 3

a) Compute the cumulative distribution of the clustering.

b) Define for every node the average clustering of its neighbors and compute its cumulative distribution.

c) Compare the two distributions.

### Weeks 5-6-7

#### Week 5

1. Depending on what seems more relevant in the graph, pick two of the following notions:

- Decay centrality
- Betweenness centrality
- Closeness centrality
- Any other notion that you invent
- PageRank

2. Identify the most central nodes.

#### Week 6

Treat the graph as undirected and unweighted. Delete loops and work on the resulting largest connected component.

Implement two of the following three techniques for community detection:

- bridge removal, selecting the partition with the highest modularity
- modularity optimization
- label propagation

In this case, built-in functions from NetworkX are allowed.

Discuss which method seems best and why.

Provide a visualization for the partition considered best using [Gephi Lite](https://gephi.org/gephi-lite/).

#### Week 7

Treat the graph as undirected and unweighted, work on the resulting largest connected component, and delete loops.

Create a function computing Common Neighbors (`CN`) and one of the following topological indices:

- Jaccard Index (`JI`)
- Preferential Attachment (`PA`)
- Adamic-Adar (`AA`)
- Resource Allocation (`RA`)

The function should return a pandas DataFrame where each row is a missing link and each column is an index. Built-in functions from NetworkX may be used for computing individual indices.

Create a third score by adding a column with the sum of the two indices.

Note: the arithmetic mean should be computed after rescaling each column between 0 and 1.

For each of the three scores, identify the node pairs yielding the top 5 or 10 values as missing links, and briefly comment on the results.

## Notes

- The notebook should be executed and saved with outputs if graphs must be visible directly on GitHub.
- If dependencies are missing, install them in the active virtual environment before running the notebook.
