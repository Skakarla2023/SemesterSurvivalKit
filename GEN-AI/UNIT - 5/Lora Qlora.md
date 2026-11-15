# Full Fine tuning vs LoRA vs QLoRA

- These are the techniques used to adapt a pretrained large language model(LLM) to a specific task using task-specific data.
- They mainly differ in number of parameters updated, GPU memory used, training time and computational cost.

## 1. Full Fine Tuning

Full Fine-Tuning is a technique in which all the parameters of a pretrained model are updated using a task-specific dataset.

### Working

1. Load the pretrained LLM.
2. Prepare task-specific data.
3. Perform forward propagation and calculate loss.
4. Use backpropagation to calculate gradients.
5. Update all model weights using an optimizer such as AdamW.
6. Save the fine-tuned model.


**Example**: A pretrained Llama model with 7 billion parameters is trained on medical question-answer data by updating all 7 billion parameters.

**Advantages**: High flexibility and potentially excellent task-specific performance.

**Limitations**: High GPU memory, computational cost, training time and storage requirements. May cause catastrophic forgetting.


## 2. LoRA (Low-Rank Adaptation)

LoRA is a Parameter-Efficient Fine-Tuning (PEFT) technique that freezes the original model weights and introduces two small trainable matrices (A and B) into selected layers.

### Working:

1. Load the pretrained LLM and freeze its original weights.
2. Insert small trainable matrices A and B into selected layers.
3. Train only these matrices using task-specific data.
4. Save the trained LoRA adapters.

**Example**: A 7-billion-parameter Llama model is adapted for medical question answering by training only small LoRA matrices instead of updating all 7 billion parameters.

**Advantages**: Faster training, fewer trainable parameters, less GPU memory and storage.

**Limitations**: Performance depends on rank and selected layers. The original pretrained model is still required.

## 3. QLoRA (Quantized Low-Rank Adaptation)

QLoRA is an extension of LoRA that combines 4-bit quantization and low-rank adaptation to reduce GPU memory requirements.

### Working:

1. Load the pretrained LLM.
2. Convert its weights into 4-bit precision using NF4.
3. Freeze the quantized weights.
4. Insert trainable LoRA adapters.
5. Train only the LoRA adapters.
6. Save the trained adapters.

**Example**: A 7-billion-parameter Llama model is stored using 4-bit quantization and adapted for medical question answering by training small LoRA adapters.


**Advantages**: Very low GPU memory requirements, efficient training and supports fine-tuning large models on smaller GPUs.

**Limitations**: Quantization may introduce small numerical errors and requires compatible hardware and libraries.
