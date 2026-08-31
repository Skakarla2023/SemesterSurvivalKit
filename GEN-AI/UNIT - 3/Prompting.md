# Prompting

- A prompt is a specific instruction or question or text input given to Artificial Intelligence, to direct its output.
- It is like a message or instruction that tells the AI what to create, how to behave and which context to consider.
- A prompt needs to be more clear and specific so that one gets a response closer to their expected response.

## Types of Prompting

- Prompting techniques or types of prompting are different ways of giving instructions to AI models, to get more desired output.
- The following are the different types of prompting:
  - Chain of thought prompting
    - Zero Shot Chain of thought prompting
    - Few Shot chain of thought prompting
    - Automatic chain of thought prompting
  - Role Prompting
  - Step back prompting

 
### 1. Chain of thought Prompting

- CoT prompting is used to instruct the LLM to use a logical step-by-step approach while generating responses.
- AI models can answer some direct questions in a simpler manner without thinking a lot.

**Eg**: What is the capital city of India

- But if you ask some logical questions like this,

**Eg:** if all roses are flowers and some flowers fade quickly, can we say that some roses fade quickly

- the model needs to think well before answering, in such cases it uses Chain of thought prompting.
- There are few ways of performing chain of thought prompting. They are:

**a) Zero shot prompting**

- In Zero-Shot Prompting, we ask the AI to perform a task without giving any examples.
- Example:
```
Prompt: "Translate this sentence into Telugu: I am going to college."
```
- The AI has to understand the task directly without seeing an example.

**b) Few Shot Prompting**

- In Few-Shot Prompting, we provide multiple examples before giving the actual task.

<img width="583" height="176" alt="image" src="https://github.com/user-attachments/assets/cdaa3672-e24f-4cff-825f-f8e4be30e49e" />

**c) Automatic CoT**

- This one is similar to few-shots CoT, but here the only difference is that the examples are not manually given, they are chosen from a collection of examples.
- Automatic CoT was giving the best results when compared to Zero shots or few-shots CoT.


### 2. Role Prompting

- Role prompting is a technique where you ask the AI to act like a person before answering, its like assigning a role to AI, so that it gives more context-specific answers.
```
Example:

"Act as a Java developer and explain inheritance to a beginner."
```
- The AI answers from the perspective of a Java developer and focuses on the user's level.

### 3. Step back prompting

- It is similar to CoT prompting.
- But here the first step is step-back - which means to generate more abstract and general information about the topic, and then try to solve it.
- Step back prompting is a technique where you ask the AI to think about the general idea behind the problem, before solving a specific problem.

Eg:

**Normal Prompt**

> Why does a metal spoon become hot in soup?

**Step-back Prompt**

> What physical principle explains heat moving between objects? Now use that principle to explain why a metal spoon becomes hot in soup.

