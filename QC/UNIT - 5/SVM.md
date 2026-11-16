# QSVM

- QSVM stands for quantum support vector machine.
- It is a machine learning algorithm that uses quantum computing to classify data into different categories.
- SVM is a machine learning algorithm that is mainly used for classification.

```
  suppose you have information about fruits, and we have to classify them as apples and oranges.
  - class A contains apples
  - class B contains oranges

  SVM finds the best possible boundary between these two classes.
  This boundary is called hyperplane.
```

<img width="360" height="273" alt="image" src="https://github.com/user-attachments/assets/1e889a35-e966-45f2-9bbf-19240a7b5c83" />

- The green line separates the two classes.
- But how does SVM decide which line is the best one?
- It chooses the line that creates the maximum possible distance between the two classes.

### 1. Hyperplane

A Hyperplane is a decision boundary that separates data points belonging to different classes.
- In 2D (two dimensions), it is a line.
- In 3D (three dimensions), it is a plane.
- In higher dimensions, it is called a hyperplane.
Example: A line separating apples from oranges.

### 2. Support Vectors

- Support Vectors are the data points that are closest to the decision boundary.
- They are very important because they help determine the position of the hyperplane.
- Support vectors are the closest data points that decide where the separating boundary should be placed.

### 3. Margin

- Margin is the distance between the hyperplane and the nearest data points from both classes.
- SVM tries to find the hyperplane with the maximum margin.
- A larger margin generally helps the model classify new, unseen data more reliably.

<img width="388" height="269" alt="image" src="https://github.com/user-attachments/assets/4ad5b6df-5804-4da5-a3ac-36e15e6efad7" />

### 4. Kernel

- Sometimes, data cannot be separated using a straight line.
- For example, imagine one class of points is surrounded by another class.
- A straight line cannot separate them properly.
- To solve this problem, SVM uses a Kernel Function.
- A kernel helps SVM handle complex, non-linear data by measuring similarity between data points in a transformed feature space.


### 5. Classification

- Classification means assigning data to a particular category.

```
Example:
- Email → Spam
- Email → Not Spam
```

<img width="387" height="284" alt="image" src="https://github.com/user-attachments/assets/45cbc5e5-e9eb-4499-ba63-c679c4f48ffb" />

## Working

### 1. Classical Input Data

- We provide the fruit details to the system.
```
Example:
- Weight = 150 grams
- Colour = Red
This is our normal input data.
```

### 2. Quantum Encoding

- The classical data (weight and colour) is converted into quantum information using qubits.
- In simple words, we convert the fruit's details into a format that a quantum computer can process.

### 3. Quantum Feature Map

- The quantum circuit transforms the encoded data into a quantum state.
- Why? To represent the data in a different feature space so that different fruit categories may become easier to distinguish.

### 4. Quantum Kernel

- Now, the system compares the quantum states of different fruits.
- For example:
  - How similar is our new fruit to an apple?
  - How similar is it to an orange?
- It calculates the similarity between the data points.

### 5. Classical SVM

- The similarity values are given to the classical SVM algorithm.
- It identifies the best separating boundary (hyperplane) using support vectors and maximum margin.
- This helps it distinguish apples from oranges.

### 6. Classification Result

- Finally, the system predicts the category of the new fruit.

```
Input: 150 grams, Red colour
Output: Apple
```

