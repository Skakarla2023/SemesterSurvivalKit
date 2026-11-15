# CLIP

- CLIP stands for contrastive language image pretraining.
- It is a multimodal language embedding model developed by openAI.
- Its main purpose is to understand the relationship between images and natural language.
- It uses 2 encoders:
  - Image encoder : understands images
  - Text encoder : understands text
- Both encoders convert their input into numerical vectors in the same embedding space.
- The image encoder converts the photograph into a numerical vector.
- The text encoder converts the sentence into another numerical vector.
- CLIP compares these 2 vectors, if the image and text are semantically related, their embeddings should be close to each other.
- The pair of embeddings that are generated are compared through cosine similarity.

<img width="712" height="62" alt="image" src="https://github.com/user-attachments/assets/f32d6740-e160-4d3f-a5b2-9ee580d4b2d6" />


<img width="2162" height="762" alt="image" src="https://github.com/user-attachments/assets/4a42c008-8cf9-4236-91b8-2814231e060d" />

## Applications of CLIP

**1. Zero shot classification** : CLIP can classify images without training a seperate classifier for every new category.

**2.Clustering** : grouping similar data points together

**3.Search** : CLIP can be used to search for images using text and search for text using images.

**4.Generation** : multimodal embeddings can also guide image-generation systems.


> OpenCLIP is an opensource implementation of the CLIP approach.
