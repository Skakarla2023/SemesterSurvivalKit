### What is a Representation Model?

- A representation model is an AI model that converts text into numerical representations (vectors or embeddings) that capture the meaning and context of the text.
- Computers cannot directly understand human language. So, text is converted into numerical vectors that models can process.
- These vectors represent the meaning of words or sentences. Similar meanings are represented by vectors that are closer to each other in the vector space.

For example:
- "I love this movie."
- "This film was amazing."

Although the words are different, their meanings are similar. A good representation model can place these sentences close to each other in the embedding space.

But:
- "I love this movie."
- "The food was terrible."

These sentences have different meanings and sentiments, so their representations may be farther apart.

<img width="380" height="286" alt="image" src="https://github.com/user-attachments/assets/dca95247-93ae-4953-9628-c3b419ab6b7c" />

## Important terms in Representation Models

### 1. Tokenization

Tokenization is the process of dividing text into smaller units called tokens. These tokens can be words, subwords or characters.

Example:
```
I love NLP.
```

Possible tokens:
```
[I] [love] [NLP] [.]
```

### 2. Token IDs
After tokenization, each token is mapped to a numerical ID using the model's vocabulary.

For example (illustrative IDs only):
|Token	|Token ID|
|--------|-------|
|I|	101|
|love	|2567|
|movie	|3185|

These IDs help the computer identify tokens, but the IDs alone do not contain semantic meaning.


### 3. Embeddings

- Embeddings are dense numerical vectors that represent the meaning of tokens or text.
- For example, a word can be represented as a vector with hundreds of dimensions such as 768 dimensions.
- Embeddings help models understand semantic similarities and relationships between words.

### 4. Contextual Embeddings

Contextual embeddings represent words according to the context in which they are used.

For example:
- "I deposited money in the bank."
- "I sat near the river bank."

The word bank has different meanings in these sentences.

### 5. Transformer

- A Transformer is a neural network architecture that uses attention mechanisms to understand relationships between tokens in a sequence.
- It helps the model identify which words are important and how they are related to other words.


### 6. Self-Attention

- Self-attention allows each token to focus on other relevant tokens in the same sentence to understand its meaning.

For example:
```
The movie was not good.
```

The model needs to pay attention to the word not to understand that the sentence expresses a negative opinion.


### 7. Bidirectional Context

- Representation models such as BERT use bidirectional self-attention.
- This means a word can consider both the words before it and the words after it when understanding its context.


### 8. Classification Head
A classification head is an additional layer attached to a pretrained representation model to predict the required class.

For example, for movie sentiment classification, it predicts one of the following:
- Positive
- Negative
- Neutral
The classification head typically produces class scores or probabilities.

### 9. Fine-Tuning

- Fine-tuning is the process of training a pretrained model further on a smaller, task-specific dataset.
- For example, BERT is initially pretrained on large amounts of text. We then fine-tune it using labelled movie reviews so it learns to classify movie reviews as positive or negative.


## Representation Model Architecture for Classification

- A commonly used representation model is BERT (Bidirectional Encoder Representations from Transformers).
- BERT uses a Transformer Encoder to understand the input text.

<img width="381" height="256" alt="image" src="https://github.com/user-attachments/assets/64ef2bb7-e5a8-4459-bf0f-3da5859139fa" />

