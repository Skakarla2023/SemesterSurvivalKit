# GRU

- GRU (Gated Recurrent Unit) is a type of Recurrent Neural Network (RNN) used in deep learning.
- It is used to remember important information from previous inputs and forget unnecessary information.
- GRU is similar to LSTM, but it has a simpler architecture and uses only two gates.

eg:

```
Suppose you are reading a paragraph. You remember important information from previous sentences and use it to understand the next sentence.

GRU works similarly by remembering useful information and forgetting unnecessary information.
```

### Why do we need GRU?

- Normal RNNs find it difficult to remember information for a long time.
- They suffer from the Vanishing Gradient Problem.
- GRU helps overcome this problem by controlling the flow of information using gates.

### Architecture of GRU

<img width="801" height="626" alt="image" src="https://github.com/user-attachments/assets/46c5c3d5-99ca-4131-81af-57865c8fa0b7" />


Important components:
- Hidden State: Stores information from previous inputs and passes it to the next time step.
- Update Gate: Decides how much previous information should be remembered and how much new information should be added.
- Reset Gate: Decides how much previous information should be forgotten.

**1. Update Gate**

- Decides how much old information should be retained and how much new information should be added.
- Helps GRU remember important information for a long time.
- Uses the Sigmoid activation function.

Example: Remembers important information from previous sentences.

**2. Reset Gate**

- Decides how much previous information should be forgotten.
- Helps the network ignore unnecessary past information.
- Uses the Sigmoid activation function.

Example: Forgets old information that is not useful for understanding the current sentence.


### Working of GRU

1. Input: Receives the current input and previous hidden state.
2. Reset Gate: Decides what previous information to forget.
3. Candidate Hidden State: Creates new information using the current input and selected past information.
4. Update Gate: Decides how much old and new information should be used.
5. Final Output: Produces the updated hidden state and passes it to the next step.


### Applications

- Speech Recognition: Converts speech into text.
- Machine Translation: Translates one language into another.
- Text Prediction: Predicts the next word in a sentence.
- Sentiment Analysis: Identifies positive and negative feelings in text.
- Time Series Prediction: Predicts future values using past data.
