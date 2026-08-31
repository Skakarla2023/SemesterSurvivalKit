## Tokenisation

- An AI model cannot directly process a sentence like humans do. It works with numbers.
- So, before text is given to an LLM, the text is broken into smaller pieces called tokens. This process is called tokenisation.
- A token can be:
  - A complete word
  - A part of a word
  - A character
  - Sometimes punctuation or a special symbol

For example:

> "I love programming."

It could be divided into:

> `I` | `love` | `programming` | .


- We need tokenization because the model needs a numerical representation of text.

### Types of Tokenisation

<img width="604" height="170" alt="image" src="https://github.com/user-attachments/assets/58324524-d49d-4397-a516-e5d0ddc00281" />

<img width="623" height="196" alt="image" src="https://github.com/user-attachments/assets/410ce4ff-6d94-4127-8cc2-28fd653d35b3" />

<img width="653" height="292" alt="image" src="https://github.com/user-attachments/assets/00ad8c7e-d76f-4c61-a2fc-3797c13ebcac" />

### BPE(Byte Pair Enoding)

- Byte Pair Encoding (BPE) is a subword tokenisation algorithm.
- Start with small units and repeatedly combine the most frequently occurring pair of units.
- The goal is to create a useful vocabulary of subwords.


<img width="605" height="254" alt="image" src="https://github.com/user-attachments/assets/363670b8-aeed-4366-887e-121ad3b65f77" />

<img width="634" height="245" alt="image" src="https://github.com/user-attachments/assets/a81a9489-6636-4516-9cb4-c1135371047c" />

<img width="560" height="121" alt="image" src="https://github.com/user-attachments/assets/e2fddb8a-fc36-4a89-a37b-80b0cd39b53f" />

<img width="624" height="221" alt="image" src="https://github.com/user-attachments/assets/77ca3dd3-4677-458d-b0cf-bbc4e0827292" />

<img width="640" height="146" alt="image" src="https://github.com/user-attachments/assets/22e0684b-ceb6-4fa2-a2db-673cfde551e2" />

<img width="641" height="197" alt="image" src="https://github.com/user-attachments/assets/8aa5b897-7f6d-4ea5-892a-1243f378c8f2" />

<img width="661" height="148" alt="image" src="https://github.com/user-attachments/assets/8d935048-386d-4632-ac18-eea0d5235f6a" />
