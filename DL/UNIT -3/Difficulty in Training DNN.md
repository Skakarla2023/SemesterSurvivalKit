## Difficulty of Training Deep Neural Networks


### 1. Learning as Optimization

- Training a deep neural network means finding suitable values of weights that minimizes the error/ loss in the training dataset.
- Therefore, training DNN can be viewed as an **optimization problem**.


### 2. Challenging Optimization

- If training is just optimization, then why is training difficult?
- Because training a DNN is very complicated, it is not a simple bowl, finding the best point is difficult as it contains hills and valleys.
- So training DNN is a non-convex optimization problem.
- Stoichotic gradient descent(SGD) along with backpropagation of error is used to update the weights.

<img width="421" height="194" alt="image" src="https://github.com/user-attachments/assets/5e8696ca-7501-44e6-a136-8330f0433889" />

<img width="436" height="194" alt="image" src="https://github.com/user-attachments/assets/59de0710-ec3f-4498-8ec5-2edaf224ce19" />

### 3. Features of the Error Surface

- DNN optimization is difficult because error surface is non-convex.
- There are three important features that makes this error surface difficult:

**1.Local Minima**

- A local minimum is a valley where the loss is relatively low compared with its surrounding region.
- However, another valley may have an even lower loss. Therefore, the optimization algorithm may stop at a local minimum instead of reaching the global minimum.
- The **global minimum** is the lowest point in the entire error landscape.
- One classical method for dealing with local minima is multiple restarts.

<img width="381" height="273" alt="image" src="https://github.com/user-attachments/assets/6a6c24f0-08b4-4ac9-8875-426b48a2d7f0" />

**2. Saddle points**

- A saddle point is a point where the gradient is zero.
- When the gradient is zero, the optimization algorithm does not know which direction to move to improve the model.
- Gradient = 0 → no clear direction for updating weights.

<img width="338" height="209" alt="image" src="https://github.com/user-attachments/assets/a0f49d4d-ff15-461e-a4c7-bdd22e2efbd0" />

**3. High Dimensional**

- DNNs contain a large number of weights, making the optimization problem high-dimensional.
- As the number of dimensions increases, the search space increases dramatically.
- This difficulty is called the curse of dimensionality.
