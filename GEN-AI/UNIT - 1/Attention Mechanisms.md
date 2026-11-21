## Attention Mechanisms

- An attention mechanism is a tool that helps AI focus on the most important parts of input data instead of treating every piece of information equally.
- Instead of treating every word as equally important, the model looks at other relevant words and gives them different levels of importance.



**Eg:** 

> "The dog chased the cat because it was hungry."


### Self Attention

- Self-attention is a mechanism that allows an AI to understand a word by looking at all the other words in the same sentence.
- In self-attention, the words in a sentence look at other words in the same sentence to understand their meaning.
- Each word is converted into three representations:
  - Query (Q) → What information am I looking for?
  - Key (K) → What information do I contain?
  - Value (V) → What information should I provide?
- The model compares the Query of one word with the Keys of other words and calculates attention scores.
  - Higher score → more attention
  - Lower score → less attention
- The model then uses these scores to combine the Values and create a better representation of the word.

### Multihead Attention

- A sentence can have different types of relationships between words.
- So instead of using only one attention mechanism, the Transformer uses several attention mechanisms called heads.
- This is called Multi-Head Attention.

**How does it work?**

1. The input is given to multiple attention heads.
2. Each head performs its own attention calculation.
3. Different heads can learn different relationships or patterns.
4. The outputs of all heads are combined.
5. A final transformation produces the output.

> Multi-Head Attention = Multiple attention mechanisms working in parallel to capture different relationships in the input.

### Cross Attention

- In self-attention, information comes from the same sequence.
- In cross-attention, one sequence looks at another sequence.
- Think of translation:

```
English: "I love India."
```

- The model is generating the Telugu translation.
- While generating the output, it needs to look at the English input to decide what words to produce.
- So the output sequence attends to the input sequence.
- That's cross-attention.
- Cross-attention uses:
  - Query (Q) → comes from the current/output sequence
  - Key (K) → comes from the input sequence
  - Value (V) → comes from the input sequence
- Cross-attention = One sequence attends to information from another sequence.



<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/cd69ecdf-6fa5-4f8b-8640-42deb6a4784e" />
