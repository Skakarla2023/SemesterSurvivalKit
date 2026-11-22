# NER

- NER stands for named entity recognition.
- Named-Entity Recognition (NER) is a Natural Language Processing (NLP) task used to identify important words or phrases in a sentence and classify them into predefined categories called entity types.
- It helps computers understand who, where, when, and what is mentioned in a sentence.
- NER is a sequence labelling task, because each token in a sentence is assigned a label based on what it represents.

**Common entity categories**

|Entity	|Meaning|	Example|
|----|---------|---------|
|PERSON	|Name of a person|	Maarten, Rahul|
|ORGANIZATION|	Company or institution	|Google, Microsoft|
|LOCATION	|Geographical place	|New York, Hyderabad|
|DATE|	Date	|22 November 2026|
|TIME|	Time |expression	10:30 AM|
|MONEY	|Monetary value|	₹500, $100|


**Example**

Sentence:
```
Maarten lives in New York.
```

|Token	|Entity Label|
|----|-------|
|Maarten	|PERSON|
lives	|O (No entity)|
|in	|O (No entity)|
|New	|LOCATION|
|York	|LOCATION|

NER identifies Maarten as a person and New York as a location.


### NER Fine Tuning

- Fine-tuning is the process of taking an already pretrained language model, such as BERT, and training it further on a labelled dataset for a specific task.
- In NER fine-tuning, a pretrained BERT model is adapted to recognize entities such as people, locations, organizations, dates and other entity types.
- Instead of training a language model from scratch, we use the knowledge already learned by BERT and teach it to identify entities in text.

**Why Fine-Tuning is used?**

- BERT already understands language and word context.
- We need to train it specifically to identify entities.
- Fine-tuning requires less training than building a model from scratch.
- It improves the model's ability to identify and classify entities in a particular dataset.


<img width="395" height="218" alt="image" src="https://github.com/user-attachments/assets/2abe4300-e59e-4918-b469-52e54f67c54a" />

### Working

<img width="600" height="242" alt="image" src="https://github.com/user-attachments/assets/9effda99-0b3b-4bee-b354-f1ac6f614cc5" />

- [CLS] – special token placed at the beginning of the input.
- [SEP] – special token used to mark the end of the input sequence.
- The other tokens represent the words in the sentence.

<img width="607" height="254" alt="image" src="https://github.com/user-attachments/assets/e644459d-8be4-4f32-a254-c1631dba2db0" />

<img width="611" height="200" alt="image" src="https://github.com/user-attachments/assets/07c2bfae-228b-44a7-8c96-9d4f9d572441" />

<img width="598" height="260" alt="image" src="https://github.com/user-attachments/assets/35cdd35f-e613-4ed3-b6c0-478d432c2b5b" />

<img width="639" height="131" alt="image" src="https://github.com/user-attachments/assets/4393b031-2204-4393-884e-7256aafd5b48" />

<img width="582" height="208" alt="image" src="https://github.com/user-attachments/assets/e9b178b7-1d2b-4551-a10f-56c318657b81" />

<img width="655" height="80" alt="image" src="https://github.com/user-attachments/assets/a0923cc1-0a95-41f8-8a78-bfd885aff757" />

### Numerical example of fine tuning

<img width="562" height="260" alt="image" src="https://github.com/user-attachments/assets/64494ba9-3295-44eb-9500-3087d5442112" />

<img width="533" height="163" alt="image" src="https://github.com/user-attachments/assets/b55b9ca9-590e-4992-a40d-5086cf6bfb43" />

<img width="584" height="291" alt="image" src="https://github.com/user-attachments/assets/6d365153-b8f5-4fc0-8f41-13dc1f94636c" />

