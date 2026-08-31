## UMAP Architecture

- UMAP stands for uniform manifold approximation & Projection.
- It is a dimensionality reduction technique.
- Its main purpose is to take high-dimensional data and represent it in a lower-dimensional space, usually 2D or 3D, while trying to preserve the important relationship between data points.
- This is especially useful in AI, Machine Learning, NLP, and LLMs for visualizing things like embeddings.

<img width="451" height="229" alt="image" src="https://github.com/user-attachments/assets/894470cc-4d7d-4359-8149-05b21f4f1670" />

<img width="434" height="211" alt="image" src="https://github.com/user-attachments/assets/61a8bb2c-a649-4e53-82c0-dda40a07b943" />

## UMAP Working

1. High dimensional data
2. Build high dimensional graph
3. Create low-dimensional graph
4. optimize
5. low-dimensional representation


### 1. Input high dimensional data

<img width="389" height="257" alt="image" src="https://github.com/user-attachments/assets/0a84a434-ad19-4bb5-b2e0-09c298ed1c75" />
 

### 2. Nearest Neighbors

- UMAP looks at each data point and finds its nearest neighbors.
- A nearest neighbor is simply a data point that is similar or close to another point.
- For example:
> Cat → Dog, Tiger, Lion

- because these animals may have similar features.
- This helps UMAP understand the local structure of the data.
- **Local structure** means the relationships between a point and the points that are close to it.

### 3. build high-dimensional graph

- UMAP represents the relationships between neighboring points using a graph.
  - **Nodes** → Data points
  - **Edges** → Relationships between nearby points
  - **Edge strength/weight** → How strongly two points are related

For example:
```
Dog ●────● Cat
     \    /
      \  /
      ● Tiger
```

### 4. Create low-dimensional representation

- Now UMAP creates a representation of the data in a lower-dimensional space.
- For example:

> 100 dimensions → 2 dimensions

- Initially, the points may be placed somewhat randomly in the 2D space.
- The goal is to arrange them so that the important relationships from the original data are preserved.

### 5. Optimize low-dimensional representation

- UMAP compares high-dimensional relationships with low-dimensional relationships.
- it moves the points around to make the low-dimensional representation better match the original structure.
- If 2 points were close originally:
  - UMAP tries to keep them **close**.
- If 2 points were very different:
  - UMAP tries to keep them **apart**.
- This process is repeated through **Optimiation**.

### 6. Final low-dimensional output

- After optimization, UMAP produces the final lower-dimensional representation.
- These coordinates can then be plotted.
- The result may show different clusters.


```
     ● ● ●
    ● ● ● ●        ○ ○
     ● ●          ○ ○ ○

                     ▲ ▲
                    ▲ ▲ ▲
```

- Each cluster may represent a group of similar data points.
