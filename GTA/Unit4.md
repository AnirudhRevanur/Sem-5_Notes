# Unit 4

## Lesson 1: Bottom Up Approach- Clique, N-Clique, K-Clique, K-Clan,K-Plex

- Clique is a complete sub-graph
    - every member is connected to each other
    - any two vertices are adjacent
- Maximal sub-graph - no extra node can be added without disturbing clique property
- Maximum clique - clique with largest number of vertices
- Maximal cliques are np hard problems
- Issues with cliques
    - Above definition is very rigid
- Two approaches to fix this
    - N clique/N-Clan - link between members
    - k-plex/k-core no of members a member is connected with
- N-Clique/ K-clique
    - few members dont know each other
    - path of {u,v} $\lt$ k
    - n=2 means max path between 2 nodes is 2
- K Clan
    - Diameter of graph is $\lt$ k
    - All paths must be through members of the group
- K plex
    - k-plex of size n means each vertex is connected to **at least** n-k other vertices
    - Can be overlapping
- K-core
    - Each node has at least a degree k
        - 0-kore is a full graph with no restrictions
        - 1-kore means every node has at least one edge (there are no isolated nodes)
        - 2-kore ever graph has at least 2 edges (there are no pendulum vertices)
        - **Cannot be overlapping**
    - Finding k-core
        1. Remove all nodes with degree less than k
            - Some nodes may have less neighbours after trimming,  remove them too
        2.  Remaining nodes form the k-core
    - K-crust 
        - What is left of the graph after removing k-core
        - In a k-core, the subgraph where every node has k neighbours is _k-corona_

## Lesson 2: Community detection, Cluster vs. Community

### Clique Percolation Method (CPM)

- Input parameter is a clique of size k and the network

- Steps
    1. Find all cliques of size k in the graph
    2. Create a set of all cliques that have k-1 nodesi n common
    3. Those nodes become communities
- It is computationally expensive so usually a _small value of k is chosen_

- CPM can return **Overlapping Communities**

### Overlapping communities

- Given a value of k find all of the maximal cliques with at least k nodes

- Matrix method - refer to slides

## Lesson 3: Girvan Newman

TBD


## Lesson 5: Generative Models

- It is difficult to analyze real life networks like social media networks because of the complexity of connections and nodes

- In order to make accurate predictions we simulate smaller graphs that are similar to larger graphs


- Empirical Network 
    - Power-law
    - Small average distance (graph diameter)
    - Large clustering coefficient
    - Giant connected component
    - Scale free nature
- Models
    - Random Graph models (Erdos & Renyi)
    - "Small World Model" (Watts & Strogatz)
    - Prefential Attachment Model(Barbasi & Albert)
    - Myopic Search

### Network Properties

- Started with **Bacon number**: nobody in Hollywood is more than 6 hops away from actor Kevin Bacon

- **Erdos number**: Connecting scholars to Erdos. Erdos has 1500+ papers with 507 co-authors

- **Stanley Milgram's Experiment**: People in Nebraska were told to send a letter to a stock broker in Boston. They could only send to someone they knew on a first name basis

- Average path length was _6_

#### Empirical Network

5 characteristics an Empirial Network should have:

1. Giant component
2. Large Local Clustering Coefficient
3. Power Law
4. Scale-free network

- **Giant Components** : There is one large component which covers more than 90% of all nodes. Rest of the network is divided into smaller nodes

- **Large Local Clustering Coefficient**: In real world friendships are highly transitive (A friend of my friend is also my friend)

- **Power Law**
    - Power Law refers to _skewed popularity_
    - Examples of power law
        - Many individuals with few friends, few individuals with thousands of friends
        - Many sites get visited few times a day, few sites get visited millions of times a day

    ![Normal Distribution] (Normal_Distribution.png "Normal Distribution")

    - In normal distribution, probability decreases as you move further away from the mean. This is not good for modelling degree distribution

    - In power law Probability (x) = 1/x<sup>b</sup>

        - Taking log on both sides log(probability(x)) = blog(x) which is a straight line
        - Expressing power law in graph theory, let p(k) denote the fraction of people having degree k (they are connected to k people)
            - p<sup>k</sup>=ak<sup>-b</sub>
            - ln p<sub>k</sub>= -bln k + ln a
            - b is **power-law exponent** usually in the range [2,3]
            - a is the **power law exponent**
        - To check for power law in a graph, take any popularity measure, compute the results and plot the logarithmic equation, if it is a straight line then power-law distribution exists

- **Scale-Free Networks**
    - Scale free networks are those networks with a power-law degree distribution.
    - If you rescale the variable k (k becomes ck where c is some constant) then the network remains unchanged other than that multiplicative factor c
    -Scale free networks have **large hubs**
    - Heavy Tails/ Fat tails: In normal distributions, tails are thin, in scale free networks the tails are heavy meaning that outliers are allowed and in fact expected in these networks









