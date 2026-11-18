# LSTM 

- LSTM stands for long short term memory.
- LSTM (Long Short-Term Memory) is a special type of Recurrent Neural Network (RNN) used in deep learning.
- It is used to remember important information for a long time and forget unnecessary information.


Eg:

```
Consider the sentence:

"Ravi went to school. He studied well. He returned home."
```

- While reading this sentence, we remember that 'He' refers to Ravi.
- Similarly, LSTM remembers important information from previous inputs and uses it to understand the current input.


### Why do we need LSTM

- Normal RNNs cannot remember information for a long time.
- It may lose important information while processing long sequences.
- This problem is called the **vanishing gradient problem**.
- LSTM solves this problem by using a special mechanism called the **cell state**.


### Architecture of LSTM
Example: Removes unnecessary old information.

**b. Input Gate**
- Decides what new information should be stored in memory.
- Uses Sigmoid and Tanh activation functions.

Example: Stores new and important information.

**c. Output Gate**
- Decides what information should be given as output.
- Uses Sigmoid and Tanh activation functions.

Example: Retrieves the required information from memory.


### Wokring of LSTM

1. Input: Takes the current input and previous memory.
2. Forget Gate: Forgets unnecessary information.
3. Input Gate: Selects new information to remember.
4. Cell State Update: Updates the memory.
5. Output Gate: Selects information to give as output.
6. Final Output: Produces the output and passes the updated memory to the next step.


### Applications

- Speech Recognition: Converts speech into text.
- Machine Translation: Translates one language into another.
- Stock Prediction: Predicts stock prices using previous data.
- Weather Forecasting: Predicts future weather conditions.
- Sentiment Analysis: Identifies positive and negative emotions in text.
