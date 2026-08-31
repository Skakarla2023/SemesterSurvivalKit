## Self Attention

- It is a mechanism that helps AI understand a word by looking at other words in the same sentence.
- In self attention, words in a sentence look at words in the same sentence to understand their meaning.

### Unmasked Self Attention

- In unmasked self-attention, a word can attend to all the words in the sequence, including words that come after it.
- There is no restriction on looking at future tokens.
- In unmasked self attention attending past words, current wor and future words is allowed.

**Example**

Sentence:

> I love eating pizza

When processing "love", it can look at:

> I, love, eating, pizza

#### Uses

- It is commonly uses in encoder-based transformers, such as **BERT**, where the model needs to understand the complete input sequence.
- For better understanding of context.
- understands complete sentences.


### Masked Self Attention

- In masked self-attention, a word can attend only to:
  - Previous words
  - Its own position
- It cannot look at future words.
- A mask is applied to hide the future tokens.

**Example**

Suppose the sentence is:

> I love eating pizza

When processing each word:

| Word   | Can attend to          |
| ------ | ---------------------- |
| I      | I                      |
| love   | I, love                |
| eating | I, love, eating        |
| pizza  | I, love, eating, pizza |

#### Uses:

- Used for auto-regressive models such as GPT.
- Maintains correct sequence.
- Used for text generation.
