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
