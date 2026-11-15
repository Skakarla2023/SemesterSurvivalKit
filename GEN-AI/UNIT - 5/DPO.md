# DPO

- DPO stands for direct preference optmization.
- DPO is a preference-based fine-tuning technique used to train an LLM using preferred and rejected responses.
- In simple words, it teaches the model which answers are better and which answers should be avoided.
- The following are the main components in DPO:
  - Pretrained language model : the original model with general language knowledge
  - Policy model : a trainable model that learns human preferences
  - Reference model : a frozen model that is used as reference during training
  - Human preference dataset : contains pairs of responses
    - chosen response : preferred answer
    - Rejected response : less preferred answer

## Working of DPO

1. Provide chosen and rejected responses to both the trainable policy model and frozen reference model.
2. Calculate the log probabilities of both responses (how likely the model is to generate each response).
3. Calculate the DPO loss by comparing the relative probabilities of chosen and rejected responses.
4. Use backpropagation to update the policy model. The reference model remains frozen.

### Objective
The main objective is to:
- Increase the probability of the chosen response.
- Decrease the relative probability of the rejected response.
- Avoid unnecessary deviation from the reference model.
- 
