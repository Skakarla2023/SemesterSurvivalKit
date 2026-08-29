# Perspectives and issues of Deep Learning

## Deep Learning

- It is a subset of machine learning, that uses neural networks to extract patterns from the data.
- It learns relationship between input and output, without needing humans to explicitly define the rules.
- It uses mathematical functions to map input to output.
- These functions extract useful patterns or information from the data.
- This process is called **training**.
- DL mainly uses artificial neural networks. 

<img width="292" height="195" alt="image" src="https://github.com/user-attachments/assets/2410d83f-f36a-4b87-8978-173fe00512c6" />

## Deep Learning Vs machine learning

| **Machine Learning (ML)**                                               | **Deep Learning (DL)**                                                 |
| ----------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Works well with **smaller datasets**.                                   | Works especially well with **large datasets**.                         |
| Requires more **human intervention** for preparing/extracting features. | Requires less human intervention for feature extraction.               |
| Generally works with carefully processed data.                          | Can process **unstructured data** such as images, text, etc.           |
| Uses different ML algorithms.                                           | Mainly uses **deep neural networks**.                                  |


## Neural Network

- It is a collection of interconnected artifical neurons/nodes.
- It is the heart of deep learning models, and was initially designed to mimic the working of neurons in the human brain.
- The neurons are interconnected and information passes from one layer to another

<img width="370" height="207" alt="image" src="https://github.com/user-attachments/assets/58e7b7f2-fc54-4999-a5df-90ea086eee4b" />

- The following are the types of neural networks:
  - Convolutional Neural Network
  - Recurrent Neural network
  - Generative Adverserial Network
 

### Convolutional Neural Network

- CNNs are mainly used for images and computer vision.
- They are very good at understanding spatial information in images — meaning they can identify patterns and features present in different parts of an image.
- For example, they can learn useful patterns from an image and use them for tasks like identifying what is in the image.
- Used for tasks such as image classification and object detection.

### Recurrent Neural network

- RNNs are mainly used when data comes in a sequence or order.
- The important thing is that the order of the data matters.
- RNNs are commonly used in tasks related to Natural Language Processing (NLP).


### Generative Adverserial Network

- A GAN is used to generate new data.
- It learns the structure and patterns of existing data and then uses what it has learned to create new examples that are similar to the original data.
- For example, if it learns from a dataset of images, it can learn the patterns in those images and generate new examples similar to them.



### Diadvantages of NN

**1.Data availability**

- Neural networks need a lot of data to learn properly.
- They need enough data to learn patterns, structure and representation of data
- If the available data is too small or not varied enough, the model may not learn properly on new/unseen data.
- This ability to perform well on unseen data is called **generalisation**.

**2. Complexity of a model**

- Choosing the right complexity for a neural network is difficult, it is a trial and error process.
  - simple model -> underfitting
  - complex model -> overfitting

**3. Incapable of Multitasking**

- A deep neural network is generally designed for a specific/targeted task.
- It learns from the type of data it is trained on.
- Eg: a model is trained to classify dogs and cats, it cannot automatically perform an unrelated task such as classifying a man and a woman.

### Applications of NN

1. Speech Recognition
2. Pattern Recognition
3. Natural Language Processing
4. Recommender Systems
5. Medical image analysis
6. Self driving cars
7. Crop monitoring
