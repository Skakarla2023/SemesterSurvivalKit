# BLIP

- BLIP stands for Bootstrapping language image pretraining.
- It is a multimodal AI designed to connect visual information with language.
- Its main purpose is to enable LLM understand images and generate meaningful text from them.


### Why do we need BLIP?

We have two different models:
1. Vision Transformer (ViT): Understands images and extracts visual features.
2. Large Language Model (LLM): Understands language and generates text.

- The problem is that these models work with different types of representations.
- This is called the Modality Gap.
- Modality Gap: The difference between how different types of data, such as images and text, are represented and processed by AI models.
- For example:
  - A vision model understands a cat through visual features.
  - A language model understands a cat through words and language representations.
- We need something that connects these two representations.

#### Why not build a multimodal model from scratch

- Building a multimodal model from scracth is a big task.
- BLIP solves this problem by using an already pretrained models instead of solving everything from scratch.
- It introduces a new component called **Q-former**, also called as querying transformer, it acts  as a bridge between image encoder and the LLM.


## Stages of BLIP Training

There are 2 stages of BLIP Training, they are:
1. Training Q-former using 3 tasks.
2. Connecting Q-former using LLM.

### 1. Training Q-former using 3 tasks

**1. Image text Matching(ITM)** : Checks whether an image and its text description match (positive pair) or do not match (negative pair).

**2. Image-Text Contrastive Learning (ITC)** : Brings matching image-text embeddings closer and pushes unrelated embeddings farther apart.

**3. Image-Grounded Text Generation (ITG)** : Trains the model to generate meaningful text based on information extracted from an image.


### 2. Connecting Q-former using LLM

1. Q-Former embeddings are passed to the LLM as soft visual prompts to provide image information.
2. A Fully Connected Layer adjusts the embedding dimensions to match the LLM.
3. The LLM uses this information to generate text.
