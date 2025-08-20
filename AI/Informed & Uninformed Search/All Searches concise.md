## BFS:

- It is a search algorithm in AI, that explores all nodes in the current level before going to the next level.
- It follows FIFO.
- It explores nodes level by level.

### Characteristics:

1. Uses a queue (FIFO – First In First Out).
  
2. Always finds the shortest path in an unweighted graph.


```mathematica
        A
      /   \
     B     C
    / \   / \
   D   E F   G
```

Goal : F

| Step | Queue   | Parent | Neighbours of Expanding Node |
| ---- | ------- | ------ | ---------------------------- |
| 1    | A       | -      | B, C                         |
| 2    | B, C    | A      | D, E                         |
| 3    | C, D, E | B      | F                            |
| 4    | D, E, F | C      | -                            |
| 5    | E, F    | D      | -                            |
| 6    | F       | E      | -                            |
| 7    | -       | -      | Goal Found                   |


## DFS:

- Explore as deep as possible in one path before backtracking.
- Starts at the root.
- Picks a child, goes down as deep as possible until it finds leaf node.
- Now backtrack and explore other paths.

### Characteristics:

1. Uses a stack (LIFO – Last In First Out) or recursion.

2. Memory usage is lower than BFS.


For the same tree the dfs order is:

```
A → B → D → E → C → F → G
```

```mathematica
        A
      /   \
    B(1)   C(2)
   / \       \
 D(4)  E(2)   F(3)
```

Goal : F

| Step | Stack   | Parent | Neighbours of Expanding Node |
| ---- | ------- | ------ | ---------------------------- |
| 1    | A       | -      | B, C                         |
| 2    | B, C    | A      | D, E                         |
| 3    | D, E, C | B      | -                            |
| 4    | E, C    | D      | -                            |
| 5    | C, E    | E      | F                            |
| 6    | F       | C      | -                            |
| 7    | -       | -      | Goal Found                   |


## Uniform Cost Search:

- Expand the node with least cost from the start.
- Similar to BFS, but finds total cost on edges.

### Characteristics:

1. Uses a priority queue.

2. ALways finds the least cost path.

```mathematica
        A
      /   \
    B(1)   C(2)
   / \       \
 D(4)  E(2)   F(3)
```

Goal:F


| Step | Queue (Node + Cumulative Cost) | Expanding Node | Parent | Neighbours Added (with cumulative cost) |
| ---- | ------------------------------ | -------------- | ------ | --------------------------------------- |
| 1    | A(0)                           | A              | -      | B(1), C(2)                              |
| 2    | B(1), C(2)                     | B              | A      | D(5), E(3)                              |
| 3    | C(2), E(3), D(5)               | C              | A      | F(5)                                    |
| 4    | E(3), D(5), F(5)               | E              | B      | -                                       |
| 5    | D(5), F(5)                     | D              | B      | -                                       |
| 6    | F(5)                           | F              | C      | -                                       |
| 7    | -                              | -              | -      | Goal Found                              |


## Bidirectional Search

- Search from both start and goal at the same time.

- One search starts at the start node, another from the goal node.

- Stop when the two searches meet.

### Characteristics:

1. Can reduce search time drastically.

2. Requires memory for both searches.

3. Works best when you know the goa

## Iterative Deepening DFS

- IDDFS is like a combination of BFS and DFS.

- It tries to get the advantages of both:

  - DFS: uses less memory (stack-based).

  - BFS: finds the shortest path.

### How it works:
 
1. Start with a depth limit = 0.

2. Do a DFS but only go as deep as the limit.

3. If the goal isn’t found, increase the depth limit by 1 and repeat.

4. Repeat until the goal is found.


## Depth Limited Search

- Like DFS, but you limit the depth you explore.

- Only go up to a certain depth L.

- Avoids infinite paths in infinite graphs.

### Characteristics:

1. Uses stack/recursion.

2. May not find goal if it’s deeper than the limit.

3. Saves memory compared to BFS/DFS.

```mathematica
        A
      /   \
     B     C
    / \     \
   D   E     F
```

Goal: F
Depth Limit: 2
Start node: A

| Step | Stack / Node to Expand | Depth | Expanding Node | Neighbours Added (if depth < limit) |
| ---- | ---------------------- | ----- | -------------- | ----------------------------------- |
| 1    | A                      | 0     | A              | B(depth=1), C(depth=1)              |
| 2    | B, C                   | 1     | B              | D(depth=2), E(depth=2)              |
| 3    | D, E, C                | 2     | D              | - (depth = limit)                   |
| 4    | E, C                   | 2     | E              | - (depth = limit)                   |
| 5    | C                      | 1     | C              | F(depth=2)                          |
| 6    | F                      | 2     | F              | - (depth = limit) → Goal Found ✅    |



## Best First Search

- It is a heuristic based algorithm.

- Use a priority queue to pick node with lowest heuristic value.

- Always expands the node that seems closest to the goal.

```mathematica
        A
      /   \
     B     C
    / \     \
   D   E     F
```

Goal: F

| Step | Queue (Nodes by lowest h) | Expanding Node | Parent | Neighbours Added (with h) |
| ---- | ------------------------- | -------------- | ------ | ------------------------- |
| 1    | A(5)                      | A              | -      | B(4), C(2)                |
| 2    | C(2), B(4)                | C              | A      | F(0)                      |
| 3    | F(0), B(4)                | F              | C      | -                         |
| 4    | B(4)                      | -              | -      | Goal Found ✅              |
